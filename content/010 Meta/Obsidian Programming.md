---
publish: true
created: 1969-12-31T18:00:00.000-06:00
modified: 2026/02/12 22:42
cssclasses: ""
---

*A place for all lessons and snippets of programming. This includes ***Templater, Linter, Dataview** and basically anything else that requires a PhD to understand

# Documentation
- [Templater](https://silentvoid13.github.io/Templater/introduction.html)
- [Dataview](https://blacksmithgu.github.io/obsidian-dataview/)
- [Obsidian](https://docs.obsidian.md/Home)
- [Mermaid Diagrams](https://mermaid.js.org/intro/syntax-reference.html)
- Latex
	- [Cheat sheet](https://kapeli.com/cheat_sheets/LaTeX_Math_Symbols.docset/Contents/Resources/Documents/index)
	- [Overleaf editor and templates](https://www.overleaf.com/)
- [Zotero](https://github.com/stefanopagliari/bibnotes#create-literature-notes)
- [Zotero Integration (powered by Nunjucks)](https://mozilla.github.io/nunjucks/templating.html)

# Learnings

### Dataview JS

> [!code]- List all system commands
> ```dataviewjs 
> dv.list(Object.keys(app.commands.commands))
> ```

> [!code]- Timecode gymnastics
> Contents
> dv.paragraph(`${l2.file.link}`)
> dv.paragraph(`${l2.file.link.length}`)
> dv.paragraph(`${l2.created}`)
> dv.paragraph(`${mom}`)
> `$= dv.date('today') + dv.duration('1 week')`
> `$= dv.date('today')`
> `$= dv.duration('1 week')`
> `$= moment(Date.now())
> `$= dv.luxon.DateTime.now().minus({weeks: 4 })`
> `$= moment().subtract(14, "days")`
> https://forum.obsidian.md/t/how-to-use-constants-and-compare-dates-in-dataviewjs/49073
> https://biscotty.online/blogs/dataviewjs-interactive-dynamic-tables
> https://www.reddit.com/r/ObsidianMD/comments/10n08lr/use_dataview_to_calculate_new_date_by_adding_a/
> https://forum.obsidian.md/t/dataviewjs-filtering-query-using-dates/72733

> [!code]- Search by tag and relative dates, return property
> `$= dv.pages("#application").where(t => t.Created && moment(t.Created).format('yyyy-MM-DD HH:mm') > moment(Date.now()).subtract(3, "months").format('yyyy-MM-DD HH:mm')).file.frontmatter["Role Title"]`

> [!code]- Return all info on a file
> *disabled via `` because this page has so much data on it from all the calls*
> $= dv.span(dv.current())

> [!code]- Search by tag, relative date, and group by specific property 
> ```var cutoff = moment(Date.now()).subtract(5, "months").format('yyyy-MM-DD HH:mm')
> let l1 = dv.pages("#Application and #industry").where(t => t.Created && moment(t.Created).format('yyyy-MM-DD HH:mm') > cutoff)
> let l2 = l1.groupBy(t => t.tags.filter(x => x.includes("industry")))```

### Dataview DQL

> [!code]- Group and count files by time interval, with ctime limit
> ```dataview
> TABLE length(rows) as Count 
> FROM #application 
> WHERE (file.ctime >= (date(today) - dur(12 week)))
> SORT file.ctime DESC
> GROUP BY dateformat(file.ctime, "DD") as day
> ```

> [!code]- Return list of tags
> *make sure you DO NOT include a target variable next to List. Apparently it will get added on its own when you declare as*
> ```dataview
> LIST
> FROM #Application 
> FLATTEN file.tags as tag
> GROUP BY tag
> WHERE icontains(tag, "#industry")
> ```

> [!code]- Search by certain tag, but omit other tags in results
> ```dataview
> TABLE WITHOUT ID file.link as Company, filter(file.etags, (x) => contains(x, "industry")) as
> Industry, Checked as Last_Checked
> FROM #newcompany and #industry/Materials   
> SORT Checked ASC
> ```

> [!code]- Search by other (text, binary) metadata
> *The 'sport_type' variable is a text field. To search for empy binarys use WHERE !complete*
> ```dataview
TABLE WITHOUT ID file.link as Link, distance as Dist  
FROM #Strava 
WHERE sport_type = "Run"
:> ```


### Mapview

> [!code]- old embedded map
> ```mapview
{"name":"Default","mapZoom":5,"centerLat":38.7837304,"centerLng":-100.445882,"query":"tag:#Application ","chosenMapSource":0,"autoFit":false,"lock":false,"showLinks":false,"linkColor":"red","markerLabels":"off","embeddedHeight":650}
> ```


### Templater 
*Note that the <% %> delimiters for Templater code break the callout block, so they have been omitted for visual clarity*

> [!code]+ Add frontmatter
>   > [!code]- Method 1: Declare together, anywhere in template
>   > companyname = await tp.system.prompt("Enter the company name")
>   > setTimeout(() => {
>   > app.fileManager.processFrontMatter(tp.config.target_file, frontmatter => { 
>   > frontmatter['Tags'] = [("company/" + companyname), ('Interviews')]
>   > })
>   > }, 200)
> 
>   > [!code]- Method 2: Declare individually, in template header
>   > ```templater
>   > <%* let company_name = await tp.system.prompt("Enter the company name") _%> 
>   > <% "---" %>
>   > Created: <% tp.date.now("YYYY-MM-DD") %>
>   > Tags: <% [("company/" + company_name), 'Interviews'] %>
>   > <% "---" %>

> [!Code]- Replace characters general variables 
> Let title = "{{title | replace(':', '') | replace('#', '') | replace('^', '') | replace('|', '') | replace('\[', '') | replace('\]', '') | replace('\\', '') | replace('/', '')}}";
> 

