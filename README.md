# Gitlet

A small version-control system in Java that works like a subset of Git. I built it in 2022 as a class project. It stores commits, blobs and branches in a `.gitlet` folder, using SHA-1 hashes and Java serialization.

## Commands

| Command | What it does |
| --- | --- |
| `init` | Create a new repository in the current folder |
| `add <file>` / `rm <file>` | Stage a file to be added or removed |
| `commit <message>` | Save a snapshot of the staged files |
| `log` / `global-log` | Show history for the current branch, or every commit |
| `find <message>` | List the commits with a given message |
| `status` | Show branches, staged files and untracked files |
| `checkout` | Restore a file, or switch to a branch |
| `branch <name>` / `rm-branch <name>` | Create or delete a branch |
| `reset <commit>` | Move the current branch to a commit |
| `merge <branch>` | Merge another branch into the current one, including conflicts |

## Run it

```bash
javac -d out Gitlet/gitlet/*.java
java -cp out gitlet.Main init
java -cp out gitlet.Main add hello.txt
java -cp out gitlet.Main commit "first commit"
java -cp out gitlet.Main log
```
