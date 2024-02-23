---
company: 
location: 
organization: 
title: 
email: 
aliases: 
publish: "false"
type:
  - person
---
# [[<% tp.file.title %>]]
<% await tp.file.move("/90 - People/" + tp.file.title) %>

## Meetings

```dataview
table summary as "Summary"
from [[<% tp.file.title %>]]
where contains(type, "meeting")
sort date desc
```

## Mentions

```dataview
LIST 
from [[<% tp.file.title %>]]
WHERE contains("aliases", [[<% tp.frontmatter.aliases %>]])
```
