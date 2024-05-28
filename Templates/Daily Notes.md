# To Do

## Tasks

```dataview
task
where completion = this.file.cday or start = this.file.cday or scheduled=this.file.cday or created=this.file.cday or due = this.file.cday
```
# Notes Created Today
```dataview
table file.mday as "Modified", file.cday as "Created"
where  file.folder != "People" and file.cday = this.file.cday
sort file.mtime desc
```


# Log