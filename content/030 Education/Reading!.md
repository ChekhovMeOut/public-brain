---
publish: true
created: 1969-12-31T18:00:00.000-06:00
modified: 2025-09-12T23:40:16.000-05:00
cssclasses: ""
---


> [!context] 
> I was using [StoryGraph](https://app.thestorygraph.com/) to keep track of reading. It does a wonderful job with data and analytics. However, the note system is cumbersome. More importantly, there is no API and no way to sync any of that information with Obsidian. Additionally, it cannot address my interest in cataloging research and paper notes effecitively.

> [!decision] 
> Start to build out an effective means of taking notes on books for *retention* rather than *congratulatory statistics*. Use these native notes to link and inform your thinkin elsewhere, and review them as needed. 

- These notes are maintained using the [[010 Meta/📐Book]] and [[010 Meta/📐Literature]] templates
- However, I can't help myself from building at least a couple basic DV queries. 

## All books
```dataview
TABLE first-author As "Primary Author", Modified
FROM #book 
SORT Modified DESC
```

## All literature
```dataview
TABLE first-author As "Primary Author", Modified
FROM #paper 
```
