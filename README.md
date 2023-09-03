# clone-tabnews
A clone of the tabnews project (curso.dev)

## Install NVM and NodeJS specific version
```sh
nvm install (.nvmrc)
```

## Create package.json
```sh
npm init
```

## Install NextJS and ReactJS
```sh
npm install next@13.1.6
``` 
```sh
npm install react@18.2.0
``` 
(Render HTML in ReactJS)
```sh
npm install react-dom@18.2.0
``` 

## Run (next dev)
```sh
npm run dev
``` 

## Protocols
- FTP
    - File transfer
- SMTP
    - Email message transfer
- HTTP (Web - Client and Server)
    - Rules for document transfer
- TCP (Safe and slower - Confirm if the information has arrived)
    - Error recovery
    - It incurs a cost
- IP (Internet Protocol)
- UDP (Faster, doesn't mind information loss - Used in video calls and games)
    - Lag(Player teleporting)

## Git
The Git stores file snapshots (blobs) and creates pointers(commits: "compromisso") to them. If a file is altered, it generates a new blob and a new pointer (keeping previous pointers for unchanged files).

Old version control systems (CVS) used to store a timeline between changes with diff (Delta between versions: Delta Encoding).

It takes up less space; however, to have a current version of a file, it would be necessary to reprocess its entire history.

### Commands
```sh
git log
```
```sh
git log --stat
```
```sh
git log --oneline
```

- Modified: A file that a previous snapshot (commit) has been modified.
- Staged: The staging area ("palco") is where files to be used in the snapshot (commit) are placed.
- Commit: Creation of the snapshot (commit) for the files in the staged area ("palco") - Immutable.

```sh
git status
```

```sh
git add .gitignore
```

```sh
git commit -m "message" 
```

```sh
git diff
```

Amend("Emendar") a change to an existing commit (replaces the previous commit)
```sh
git commit --amend
```

Push("Empurrar")/upload the changes from the local repository to the remote (GitHub)
```sh
git push
```
```sh
git push -f (Danger)
```

List branches: 
origin/main (github web) | local/main (local git)
```sh
git branch
```