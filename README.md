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

## Convert JS to TS With Type Checking
- First run the following command in your console.
```
npx typescript --init
```
- Now a tsconfig.json file will be created and now make the following changes.
1. Make outDir: './dist'
2. Make rootDir: './src'
3. Uncomment the following attibute named moduleResolution.
4. Uncomment the attribute CheckJS so that it enables ts to type check for your js files.

- Now you can just rename your js file to ts.

- Check for the modules that you imported whether it supports both natively, if not them install it using @types.
For example if express has no definations and is a seperate module for TS, then you can install it following this snippet.
```
npx -i -D typescript @types/node @types/express
```

- Update the scripts in packages.json with following changes -
1. It is optional to include start , so for start command use this: node dist/index.js
2. For build command use this: tsc -p tsconfig.json
3. By now it should working if you run the following commands.

- Make sure in your js file you change your variable type to 'Any'.
- Now you can just refactor the code according to make it to TS.

- Also now you can create a dev command and include this : ts-node src/index.js

- If you are facing problems and not able to execute these steps. Click on this [Link](https://www.youtube.com/watch?v=qFMMOJucqTw).

