---
{"publish":true,"created":"2025-05-27T18:18:28.000-05:00","modified":"2025-09-12T23:28:37.217-05:00","cssclasses":""}
---


# Modification pace
Evaluation Error: SyntaxError: Invalid or unexpected token
    at DataviewInlineApi.eval (plugin:dataview:19027:21)
    at evalInContext (plugin:dataview:19028:7)
    at asyncEvalInContext (plugin:dataview:19035:16)
    at DataviewJSRenderer.render (plugin:dataview:19064:19)
    at DataviewJSRenderer.onload (plugin:dataview:18606:14)
    at DataviewJSRenderer.load (app://obsidian.md/app.js:1:1182416)
    at DataviewApi.executeJs (plugin:dataview:19607:18)
    at tryExecuteJs (plugin:quartz-syncer:19764:15)
    at eval (plugin:quartz-syncer:19678:38)
    at eval (plugin:quartz-syncer:20146:54)mermaid\n" + 
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

Evaluation Error: SyntaxError: Invalid or unexpected token
    at DataviewInlineApi.eval (plugin:dataview:19027:21)
    at evalInContext (plugin:dataview:19028:7)
    at asyncEvalInContext (plugin:dataview:19035:16)
    at DataviewJSRenderer.render (plugin:dataview:19064:19)
    at DataviewJSRenderer.onload (plugin:dataview:18606:14)
    at DataviewJSRenderer.load (app://obsidian.md/app.js:1:1182416)
    at DataviewApi.executeJs (plugin:dataview:19607:18)
    at tryExecuteJs (plugin:quartz-syncer:19764:15)
    at eval (plugin:quartz-syncer:19678:38)
    at async eval (plugin:quartz-syncer:20146:26)mermaid\n" + 
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

