---
aliases: 
publish: false
tags: 
type:
  - person
cssclasses:
  - cards
  - cards-16-9
---

# [[<% tp.file.title %>]]
<% await tp.file.move("/90 - People/" + tp.file.title) %>

Company:: 
Location:: 
Organization::
Title:: 
Email:: 
Work Phone:: 
Cell Phone::

## Assigned Tasks

```dataview
task
where !completed and assign = this.file.link
    and !"99 - Templates"
group by upper(priority)
sort file.cdate desc
```

## Meetings

```dataview
table summary as "Summary", file.ctime as "Created"
from [[<% tp.file.title %>]]
where contains(type, "meeting") and !"99 - Templates"
sort date desc
```

## Daily Note Mentions

```dataview
TABLE
FROM "00 - Daily Notes" and !"99 - Templates"
WHERE file.inlinks
SORT file.ctime DESC
```
## Other Mentions

```dataview
table file.mtime as "Last Modified"
from !"00 - Daily Notes" and !"90 - People" and !"99 - Templates"
where file.inlinks
sort date desc
```
