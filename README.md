# pluralsight-js-dev-env
JavaScript Development Environment from Pluralsight Course with Cory House

# Course Notes
* JavaScript Editors
  * Atom ($), Webstorm, Brackets, VSCode (*)
* Editor Config
  * editorconfig.org
  * create file, install plug-in for VSCode
* JS Package Managers
  * Bower, npm (*), JSPM, Jam, Volo
* Node Security Project
  * (sudo) npm install -g nsp
  * nsp check
* Web Servers (only for Dev hosting)
  * http-server
  * live-server
  * Express (*) (koa, hapi)
  * budō
  * Webpack Dev Server
  * Browsersync (syncs across devices all at once!)
* Sharing Work-in-progress
  * localtunnel (*)
    * punch hole in firewall, quick setup
    1. npm install localtunnel -g
    2. Start your app
    3. lt --port 3000
  * ngrok
    * localtunnel with password protection
    1. sign up
    2. install ngrok
    3. install authtoken
    4. start your app
    5. ./ngrok http 80
  * now
    * quickly deplay Node.js to the cloud
    * more permanent (machine can be off)
    1. nmp install -g now
    2. Create start script
    3. now (to deploy)
  * Surge
    * downside: only use static files
    * publish on public URL
    1. npm install -g Surge
    2. Surge
* Automation
  * Grunt, Gulp, npm Scripts (*)
    * bit.ly/npmvsgulp
* Transpiling
  * "Compiling one language into another of similar abstraction"
  * Babel (*), Typescript (JS superset), Elm (unique benefits)
* Module formats
  * IIFE, AMD, UMD, CommonJS, ES6 (*)
* Bundling
  * Browserify
    * simple
  * Webpack (*)
    * comprehensive
  * Rollup
    * tree shaking, performance
  * JSPM
    * runtime loader, package manager
* Debugging transpiled, bundled code
  * Sourcemaps
    * maps code back to original source
    * part of our build
    * downloaded if you open developer tools
* Linting
  * Why? Enforce consistency, avoid mistakes
  * JSLint, JSHint, ESLint (*), TSLine (Typescript)
  * Core Decisions
    * 1 - Config Format: dedicated file (*) vs. package.json
    * 2 - Which Rules? check ESLint API for options
    * 3 - Warnings vs Errors
    * 4 - Which Plug-ins? github.com/dustinspecker/awesome-ESLint
    * 5 - Use a preset? Custom steps 1-4, default preset step 5 only (recommended (*) vs. others like AirBnB)
  * Issues
    * ESLint does not watch files
      * eslint-loader (re-lint on save)
      * eslint-watch (*)
        * wrapper that adds file watch to ESLint
        * not tied to Webpack
        * better warning/error messages
    * ESLint does not support experimental JS
      * babel-eslint: also lints stage 0-4 features
  * Why lint during automation build?
    * one place to check, universal config, part of continuous integration
