---
date-created: <% tp.date.now("YYYY-MM-DD HH:MM") %>
type:
  - daily note
tags: []
---
# Daily Notes for<br><% tp.date.now("dddd, MMMM Do YYYY") %>

--- 
## Summary

> [!todo]- Today's TODO's
> ```dataview
> task
> where file = this.file
> ```

> [!info]- Metadata
> Path: <% tp.file.folder(false) %>/<% tp.file.title %>.md
> Tags: `= this.file.tags`

---

what's happening?

