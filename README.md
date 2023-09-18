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

#### Add .prettierignore

## DNS (Domain Name System)

Converts a domain name to an IP address.

Domain its a human-readable name("apelido") for an IP address.

Your computer asks the DNS server for the IP address of a domain and then connects to it.

Every connection point on the internet has an IP address.

DNS Server is like a database with domain names and their respective IP addresses.

Obs: Distributed denial-of-service attack on root nameservers. (Wikipedia)

### Register a domain

Registrar("registrador") - Company that registers domains. Ex: Registro.br, HostGator, GoDaddy, etc.

Registry("registro") - Nic.br: Responsible for the registration and maintenance of domain names that use the .br extension.

TLD (Top Level Domain) - .br (NIC.br)

Authoritative server(Nameservers) - DNS server that stores the DNS records for a domain. (registro.br)

Root server - DNS server that stores the DNS records for a TLD. (NIC.br)

Obs: <https://whatsmydns.net/#NS/example.com> (DNS propagation CHECKER)

### Configure DNS server(Authoritative)

- Cloudflare - DNS server
- Vercel - DNS server

A = Address: Maps a domain to an IP address.

## McDonald's theory

Sugestion something bizarre, withou any sense, to make the people think about it and choose the other options.

"If i choose this, i prefer the other options. (List other options)"
"You brain will feel inspired to have good ideas, to get away from bad ideas."

## Uptime and SLA (Service Level Agreement)

Uptime: Time that a service is available.
SLA: Contract between the service provider and the customer.

Obs: Don't exist 100% uptime.

### Status page

- <https://status.vercel.com/>
- <https://health.aws.amazon.com/health/status>

## PoC (Proof of Concept) and MVP (Minimum Viable Product)

- What proves that the idea is possible.
- Create a prototype to validate the idea. (The minimum necessary)

Obs: Find cheap ways to validate the idea. After that, invest in the idea with the minimum. (New things or improvements)

## Foundation

- Architeture Proposal and Folders
- Automatated Tests
- Database (Local)
- Migrations
- Continuous Integration
- Code linter
- Commits linter
- Database (Homologation and Production)
- License Type

### Architeture Proposal and Folders

Avoid Overengineering: Excessive use of tools and techniques.

Avoid Underengineering: Lack of tools and techniques.

Find the balance between the two.

Ex: Choosing a language

- Intern maturity (Company)
- Hiring (People - Seniority)
- Documentation (Community)
- Aplicability (Project)

Obs: Software is modifiable.

#### Architeture Proposal

Software Architecture is different from Folder Structure. Ex: You can apply the MVC pattern and the Clean Architecture pattern in one folder structure or file.

Software Architecture: Is defined by the scope of the components and the relationships between them.

A simple architecture and a good modeling can make you go far.

#### Folders

```md
📦 root
┣ 📂 pages
┃ ┗ 📜 index.js
┣ 📂 models
┃ ┣ 📜 user.js
┃ ┣ 📜 content.js
┃ ┗ 📜 password.js
┣ 📂 infra
┃ ┗ 📜 database.js
┃ ┣ 📂 migrations
┃ ┣ 📂 provisioning
┃ ┃ ┣ 📂 staging
┃ ┃ ┣ 📂 production
┣ 📂 tests
```

### Automatated Tests (Jest)

Test everything after a change.

#### Test runner and Test framework

A code that execute your code.

Expect("espera"): What you expect to happen.

Watch mode: Run the tests after a change automatically.

#### Install Jest as a development dependency

```sh
npm install --save-dev jest@29.6.2
```

#### Add Jest to package.json

```json
"scripts": {
  "test": "jest",
  "test:watch": "jest --watch"
}
```

#### Run Jest

```sh
npm run test
```

```sh
npm test
```

#### Write a test

/models/calculator.js

```js
function sum(a, b) {
  if (typeof a !== "number" || typeof b !== "number") {
    return "Error";
  }
  return a + b;
}

exports.sum = sum; // CommonJS
```

/tests/calculator.test.js

```js
const calculator = require("../models/calculator.js");

test("sum 2 + 2 to equal 4", () => {
  const result = calculator.sum(2, 2);
  expect(result).toBe(4);
});

test("sum 5 + 100 to equal 105", () => {
  const result = calculator.sum(5, 100);
  expect(result).toBe(105);
});

test("sum 'banana' + 100 to equal 'Erro'", () => {
  const result = calculator.sum("banana", 100);
  expect(result).toBe("Error");
});
```

On the left side(expect) there is a dinamic value (Softcoded), on the right(toBe) there is a expected value (Hardcoded).

Obs: One test dont prove anything that the application works. You need to test various the possibilities/scenarios.

#### TDD (Test Driven Development)

Test guide the development. First write the test, then write the code.
