How to remove a file from Git Repo w/o removing from the filesystem
===================================================================

This solution solves my problem when i want to remove my SQLite database from the repo, so i can upload the repo to github w/o the database
the command below assumes foofile.txt exists and in the log.

```bash
git rm --cached foofile.txt
```
