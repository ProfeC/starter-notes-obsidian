---
cssclasses:
  - cards
  - cards-cols-2
aliases:
  - GLC2
  - Lee
  - LC
  - Lee C.
  - gary.clark
  - clarkgar
tags:
---

# Lee Clark

Company:: #SetonHallUniversity 
Location:: South Orange, NJ
Organization:: TLTC/Web Development
Title::  Web Developement Manager
Email:: clarkgar@shu.edu
Work Phone:: +1 (973)275-2212 
Cell Phone::

## Assigned Tasks

```dataview
task
where !completed and assign = this.file.link
group by upper(priority)
sort file.cdate desc
```

## Meetings

```dataview
table summary as "Summary", file.ctime as "Created"
where type = meeting and !"99 - Templates" and this.file.inlinks
sort date desc
```

## Daily Note Mentions

```dataview
TABLE
FROM "00 - Daily Notes"
WHERE file.inlinks
SORT file.ctime DESC
```
## Note Mentions

```dataview
table file.mtime as "Last Modified"
from !"00 - Daily Notes" and !"90 - People"
where file.inlinks
sort date desc
```
