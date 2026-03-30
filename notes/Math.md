---
status: archive
category: math
---
```dataview
TABLE category AS "Category", dateformat(file.mtime, "yyyy-MM-dd HH:mm") AS "Last Modified", dateformat(file.ctime, "yyyy-MM-dd HH:mm") AS "Created"
FROM ""
WHERE parent = [[Math]]
SORT file.mtime DESC
```

