# VSCode Node Debug issue with Nuxt 3

## Setup

Clone the repo and install the repo.

Make sure to install the dependencies:

```bash
# npm
npm install
```

## Development Server

Start the development server with debugging enabled on `http://localhost:3000`:

```bash
# npm
npm run debug
```

## Attach Debugger (Config "Attach to local")

There is a preconfigured launch configuration for VSCode in `.vscode/launch.json`. You can use this to attach the debugger to the running application.

You can set a breakpoint in `server/api/test.ts` and then open `http://localhost:3000/api/test` in your browser. 

The debugger should stop at the breakpoint. But it does not. For some reasons the sourcemaps located unter `.nuxt/dev` are not loaded.

## Start Nuxt Server with debugger from VSCode (Config: server: nuxt)

Instead of starting the application from the terminal, you can also start it from VSCode. There is a preconfigured launch configuration for VSCode in `.vscode/launch.json`. 
You can use this to start the application with the debugger.

You can set a breakpoint in `server/api/test.ts` and then open `http://localhost:3000/api/test` in your browser. 

The debugger stops at the breakpoint. The sourcemaps under `.nuxt/dev` are loaded and the breakpoint is hit.
