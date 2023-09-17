# clone-tabnews

A clone of the tabnews project (curso.dev - Filipe Deschamps)

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

## Add Next to package.json

```json
"scripts": {
  "dev": "next dev",
}
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

The Git stores file snapshots (blobs) and creates pointers(Commit: "Compromisso") to them. If a file is altered, it generates a new blob and a new pointer (keeping previous pointers for unchanged files).

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
git diff
```

```sh
git add .gitignore
```

Stage all files

```sh
git add -A
```

```sh
git commit -m "message"
```

Amend("Emendar") a change to an existing commit (replaces the previous commit)

```sh
git commit --amend -m "message"
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

## Client and Server

- Client: The one who requests something.
- Server: The one who provides something.

Protocol example: HTTP on TCP/IP.

### Host("Abrigo") Website - Vercel

- Moving files to a specific location (deploy: "implantar")
  - FTP Protocol (Old)
  - Editing the file on the server(Old)
  - Using Git on the server (New)

### CI/CD (Continuous Integration/Continuous Delivery)

With each new push, Vercel deploys the last pushed commit and maintains a history of previous deployments with a permanent URL.

## Milestones and Issues

Group issues and pull requests around a stage of the project.

Example: List of assignments to be done.

```MD
- [ ] Ligar sincronização do Editor
- [ ] Configurar o EditorConfig
- [ ] Configurar o Prettier
```

## Code styling (Standards)

### EditorConfig

Obs: Only format the code before saving the file.

#### Create .editorconfig

```.editorconfig
root = true

[*]
indent_style = space
indent_size = 2
```

Install EditorConfig extension on VSCode

### Code Formatter (Prettier)

Obs: Use Prettier with npm scale its use.

#### Install Prettier as a development dependency

```sh
npm install prettier --save-dev
```

```sh
npm install prettier --D
```

#### Add Prettier to package.json

```json
"scripts": {
  "lint:check": "prettier --check .",
  "lint:fix": "prettier --write ."
}
```

#### Run Prettier

```sh
npm run lint:check
```

```sh
npm run lint:fix
```

- Install Prettier extension on VSCode
- Enable prettier as default formatter on VSCode
- Enable format on save on VSCode
- Disable auto save on VSCode
