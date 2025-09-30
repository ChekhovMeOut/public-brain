---
{"publish":true,"created":"2025-09-30T11:10:24.463-05:00","modified":"2025-09-30T11:11:11.148-05:00","cssclasses":""}
---


I want to see if writing the base code directly into a file can be rendered successfully. 

```base
formulas:
  Hash: (file.ctime.minute*100+file.ctime.second)*(now().second+now().minute*100)%1007
views:
  - type: table
    name: Table
    filters:
      and:
        - public == true
    order:
      - file.name
    sort:
      - property: formula.Hash
        direction: ASC
    limit: 5
```
