# Angular QuickStart Source
[![Build Status][travis-badge]][travis-badge-url]

This repository holds the TypeScript source code of the [angular.io quickstart](https://angular.io/docs/ts/latest/quickstart.html),
the foundation for most of the documentation samples and potentially a good starting point for your application.

It's been extended with testing support so you can start writing tests immediately.

**This is not the perfect arrangement for your application. It is not designed for production.
It exists primarily to get you started quickly with learning and prototyping in Angular**

We are unlikely to accept suggestions about how to grow this QuickStart into something it is not.
Please keep that in mind before posting issues and PRs.

## Updating to a newer version of the Quickstart Repo

From time to time the QuickStart will add be enhanced with support for new features or to reflect
changes to the [official Style Guide](https://angular.io/docs/ts/latest/guide/style-guide.html).

You can update your existing project to an up-to-date QuickStart by following these instructions:
- Create a new project using the [instructions below](#create-a-new-project-based-on-the-quickstart)
- Copy the code you have in your project's `main.ts` file onto `src/app/main.ts` in the new project
- Copy your old `app` folder into `src/app`
- Delete `src/app/main.ts` if you have one (we now use `src/main.ts` instead)
- Copy your old `index.html`, `styles.css` and `tsconfig.json` into `src/`
- Install all your third party dependencies
- Copy your old `e2e/` folder into `e2e/`
- Copy over any other files you added to your project
- Copy your old `.git` folder into your new project's root

Now you can continue working on the new project.

## Prerequisites

Node.js and npm are essential to Angular development. 
    
<a href="https://docs.npmjs.com/getting-started/installing-node" target="_blank" title="Installing Node.js and updating npm">
Get it now</a> if it's not already installed on your machine.
 
**Verify that you are running at least node `v4.x.x` and npm `3.x.x`**
by running `node -v` and `npm -v` in a terminal/console window.
Older versions produce errors.

We recommend [nvm](https://github.com/creationix/nvm) for managing multiple versions of node and npm.

## Install npm packages

> See npm and nvm version notes above

Install the npm packages described in the `package.json` and verify that it works:

```shell
npm install
npm start
```

The `npm start` command first compiles the application, 
then simultaneously re-compiles and runs the `lite-server`.
Both the compiler and the server watch for file changes.

Shut it down manually with `Ctrl-C`.

You're ready to write your application.

### npm scripts

We've captured many of the most useful commands in npm scripts defined in the `package.json`:

* `npm start` - runs the compiler and a server at the same time, both in "watch mode".
* `npm run build` - runs the TypeScript compiler once.
* `npm run build:w` - runs the TypeScript compiler in watch mode; the process keeps running, awaiting changes to TypeScript files and re-compiling when it sees them.
* `npm run serve` - runs the [lite-server](https://www.npmjs.com/package/lite-server), a light-weight, static file server, written and 
