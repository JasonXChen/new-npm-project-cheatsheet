# Cheat Sheet for npm Projects

Useful information about npm projects running via Node.js

## Steps to build and use a new npm project/Node.js package

1. Make a new project folder
2. Create a JavaScript module file in the folder
3. Use `module.exports` to export whatever is needed for the child of the dependency
4. Import the created module in the dependent file (e.g. index.js) using `const foo = require("./PATH_TO_MODULE");`
5. Run the result with `node index.js`

## Setting up a repository that uses Node.js packages

1. (Optional) Run `npm init` in the root directory of the repository and add basic project info
2. Install the necessary node packages in the root directory of the repo
3. Add a .gitignore file with a `node_modules` line to prevent the packages from being pushed to a remote repo

## Cloning a repo containing Node.js packages
1. Clone the remote repo to local machine using `git clone ${URL_OF_REPO}`
2. Install all dependencies with `npm install` or just `npm i`