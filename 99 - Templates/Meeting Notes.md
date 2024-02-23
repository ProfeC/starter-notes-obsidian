---
date: <% tp.date.now("YYYY-MM-DD") %>
time: <% tp.date.now("YYYY-MM-DD HH:MM") %>
summary: ""
type:
  - meeting
tags:
---

# [[<% tp.file.title %>]]

## Attendees
- [Lee C.](Lee%20Clark.md)
- 

## Agenda



## Notes



## Follow-Up Actions

- 

---

## Possibly Related

```dataview
table summary as "Summary", date as "Date", file.folder as "Folder", tags as "Tags"
where
  type = "meeting" 
  and contains(tags, this.tags)
  and file.folder != "99 - Templates"
  and file != this.file
sort time desc
```