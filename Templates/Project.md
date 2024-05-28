---
Technical Owner: 
Business Owner: 
Target Date: TBD
tags:
  - active
Log: '[[<% (await tp.file.create_new("# Log", tp.file.title + " Log", false, "Project Logs")).basename %>|Log]]'
---
Project log: 
# Goal
# Stakeholders

# Tasks

```tasks
not done
description includes <%tp.file.title%>
```

# Tickets
# Links
- 

# Mentions
```query
<%tp.file.title%> -path:(Interview OR <%tp.file.path(true)%>)
```

# Log