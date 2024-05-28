---
Manager: 
aliases:
---
Members:

# Notes

[[<% (await tp.file.create_new("", tp.file.title + " Log", false, "Meeting Notes")).basename %>]]

# ToDos

## Team
```tasks
not done
description includes <% tp.file.title %>
```

## Manager

```tasks
not done
description includes <% tp.frontmatter.Manager %>
```
# Tickets

### CP My Tickets
```jira-search
query: project = <%tp.frontmatter.aliases[0]%> and creator = currentUser() and statusCategory != Done ORDER BY priority desc
columns: KEY, SUMMARY, PRIORITY, STATUS, ASSIGNEE, 
```


### CP In Progress

```jira-search
query: project =  <%tp.frontmatter.aliases[0]%> and statusCategory = "In Progress" and assignee is not empty ORDER BY priority desc
columns: KEY, SUMMARY, PRIORITY, STATUS, ASSIGNEE, 
```

### CP Recently Completed

```jira-search
query: project =  <%tp.frontmatter.aliases[0]%> and statusCategory = Done and status changed after -14d ORDER BY  resolved DESC
columns: KEY, SUMMARY, PRIORITY, STATUS, ASSIGNEE, 
```



