# Cheat Sheet for npm Projects

Useful information about npm projects running via Node.js

## Steps to build and use a new npm project/Node.js package

* ### Setting up files

    1. Make a new project folder
    2. Create a JavaScript module file in the folder
    3. Run `npm init` to create a package.json (`npm init -y` to enter default info)
    4. Use `module.exports` to export whatever is needed for the child of the dependency
    5. Import the created module in the dependent file (e.g. index.js) using `const foo = require("./PATH_TO_MODULE");`
    6. Run the result with `node index.js`

* ### Pushing project onto remote git repo

    1. Run `git init` to create a new repo in the project directory
    2. Create a .gitignore file and add `node_modules` to it (`echo node_modules >> .gitignore` one-liner)
    3. Standard `git add <FILES>`, `git commit -m <COMMIT_MESSAGE>`, and `git push origin main`

## Setting up a repository that uses Node.js packages

1. (Optional) Run `npm init` in the root directory of the repository and add basic project info
2. Install the necessary node packages in the root directory of the repo
3. Add a .gitignore file with a `node_modules` line to prevent the packages from being pushed to a remote repo

## Cloning a repo containing Node.js packages
1. Clone the remote repo to local machine using `git clone ${URL_OF_REPO}`
2. Install all dependencies with `npm install` or just `npm i`