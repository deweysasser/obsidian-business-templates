# Tickets

### <% tp.frontmatter.aliases[0] %> My Tickets
```jira-search
query: project = <% tp.frontmatter.aliases[0] %> and creator = currentUser() and statusCategory != Done ORDER BY priority desc
columns: KEY, SUMMARY, PRIORITY, STATUS, ASSIGNEE, 
```


### <% tp.frontmatter.aliases[0] %> In Progress

```jira-search
query: project = <% tp.frontmatter.aliases[0] %> and statusCategory = "In Progress" and assignee is not empty ORDER BY priority desc
columns: KEY, SUMMARY, PRIORITY, STATUS, ASSIGNEE, 
```

### <% tp.frontmatter.aliases[0] %> Recently Completed

```jira-search
query: project = <% tp.frontmatter.aliases[0] %> and statusCategory = Done and status changed after -14d ORDER BY  resolved DESC
columns: KEY, SUMMARY, PRIORITY, STATUS, ASSIGNEE, 
```
