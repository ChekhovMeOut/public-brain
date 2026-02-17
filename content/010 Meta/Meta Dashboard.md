---
publish: true
created: 2026-02-12
modified: 2026/02/12 22:41
cssclasses: ""
---

oh boy i haven't touched this in a minute
# Modification pace
```dataviewjs
var mom = moment(Date.now()).subtract(24, "months").format('yyyy-MM-DD HH:mm')
var count_max = 1

let l1 = dv.pages("")
let l2 = l1.where(t => t.Created && moment(t.Modified).format('yyyy-MM-DD HH:mm') > mom)
let l3 = l2.groupBy(t => moment(t.Modified).format('YY-MM'))
let time = l3.key

let count = [];
count.length = l3.values.length;
for (let i = 0; i < count.length; i++) {
	count[i] = l2.where(t => t.Modified && moment(t.Modified).format('YY-MM') == l3.key[i]).length;
	if (count[i] > count_max) {
		count_max = count[i]
		}
}

//let l4 = await dv.query('TABLE WITHOUT ID length(rows) as Count FROM #application WHERE (file.ctime >= (date(today) - dur(12 week))) GROUP BY dateformat(file.ctime, "DD") as Day SORT Day DESC')
//let cunt = l4.Count
//let tune = l4.Value
//console.log(dv.array(count))

dv.paragraph("```mermaid\n" + 
`---
config:
    xyChart:
         width: 1000
         height: 500
    theme: base
    themeVariables: 
        fontSize: 200px
        xyChart: 
            backgroundColor: "#00000000"
            plotColorPalette: "#6fad45"
---
xychart-beta
	x-axis "Date (YY-MMM)" ${time}
	y-axis "Files Modified" 0 --> ${count_max*1.2}
	bar [${count}]
` + "```")
```
# Creation pace

```dataviewjs
var mom = moment(Date.now()).subtract(24, "months").format('yyyy-MM-DD HH:mm')
var count_max = 1

let l1 = dv.pages("")
let l2 = l1.where(t => t.Created && moment(t.Created).format('yyyy-MM-DD HH:mm') > mom)
let l3 = l2.groupBy(t => moment(t.Created).format('YY-MM'))
let time = l3.key

let count = [];
count.length = l3.values.length;
for (let i = 0; i < count.length; i++) {
	count[i] = l2.where(t => t.Created && moment(t.Created).format('YY-MM') == l3.key[i]).length;
	if (count[i] > count_max) {
		count_max = count[i]
		}
}

//let l4 = await dv.query('TABLE WITHOUT ID length(rows) as Count FROM #application WHERE (file.ctime >= (date(today) - dur(12 week))) GROUP BY dateformat(file.ctime, "DD") as Day SORT Day DESC')
//let cunt = l4.Count
//let tune = l4.Value
//console.log(dv.array(count))

dv.paragraph("```mermaid\n" + 
`---
config:
    xyChart:
         width: 1000
         height: 500
    themeVariables: 
        xyChart: 
            backgroundColor: "#00000000"
            plotColorPalette: "#6fad45"
---
xychart-beta
	x-axis "Date (YY-MMM)" ${time}
	y-axis "Files Created" 0 --> ${count_max*1.2}
	bar [${count}]
` + "```")
```

