# 👷 `worker-template` Hello World \#NowOnReplit

[![Run on Repl.it](https://repl.it/badge/github/HelloImAlastair/WorkerOnReplit)](https://repl.it/github/HelloImAlastair/WorkerOnReplit)

A template for kick starting a Cloudflare worker project, optimized for use in Replit.

[Learn more about Workers]("https://developers.cloudflare.com/workers")

[`src/index.js`](src/index.js) is the content of the Workers script.

## Commands
Here are some commands that this repo comes with. Feel free to add your own, or add a Pull Request to add some to this repo. Note that all these commands must be added to the _run_ field of the [`.replit`](.replit) file, then press the run button to execute them, and each command must be prefixed with _yarn_. Also, the default command will automatically build and create a miniflare instance for you.

### format
Utilizes [Prettier](https://prettier.io) to format your code. Configuration can be edited in the [`.prettierrc`](.prettierrc) file.

## build
Runs [Esbuild](https://esbuild.github.io) to build your script. Default is to bundle and minify. Configuration can be edited directly in the command in the [`package.json`](package.json).

### big
Disables minifying to allow you to debug your code easier.

## test
Automatically builds your script, then uses [Miniflare]("https://miniflare.dev") to allow you to test your script locally, before deploying.

## clean
Removes the built script and `node_modules`, to allow you to build from scratch.