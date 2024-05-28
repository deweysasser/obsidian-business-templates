
# PRs
```github-query
outputType: table
queryType: pull-request
org: actblue
query: "is:pr author:<% tp.frontmatter.GitHubName %> org:actblue is:open"
columns: [number, title, repo]
per_page: 20
```

# Tickets
## In Progress

```jira-search
query: assignee = "<% tp.file.title %>" and statusCategory != Done order by priority desc, status, created desc
columns: KEY, SUMMARY, PRIORITY, STATUS, 
```
## Recently Completed
```jira-search
query: assignee = "<% tp.file.title %>" and statusCategory = Done  and status changed after -14d order by priority desc, status, created desc
columns: KEY, SUMMARY, PRIORITY, STATUS, 
```