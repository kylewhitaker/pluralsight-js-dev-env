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
* Testing
  * Unit Testing
    * Framework
      * Mocha (*), Jasmine, Tape, QUnit, Ava, Jest
    * Assertion Libary
      * Chai (*), Should.js, expect
    * Helper Library
      * JSDOM (*), Cheerio
    * Where to run tests?
      * Browser
        * Karma, Testem
      * Headless Browser
        * PhantomJS
      * In-Memory DOM
        * JSDOM (*) --> Node
    * Where to place tests?
      * Centralized (separate tests folder)
      * Alongside (*)
    * When to run tests?
      * When you hit save (*)
* Continous integration
  * Travis (*) --> for Mac/Linux
    * travisci.org
  * Appveyor (*) --> for Windows
    * appveyor.com
  * Jenkins, circleci, semaphore, SnapCI
* HTTP Calls & Mock API
  * HTTP Call Approaches
    * Node
      * http, request (*)
    * Browser
      * XMLHttpRequest, jQuery ($AJAX), Framework-based (Angular), Fetch (*, need polyfill)
    * Node & Browser
      * isomorphic-fetch, xhr (npm), SuperAgent, Axios
  * Why centralize API calls?
    * Configure all calls in one place
    * Handle preloader logic
    * Handle Errors
    * Single seam for mocking
  * Why send polyfill to all browsers?
    * selective? polyfill.io
  * Why mock HTTP?
    * Unit Testing
    * Instant Response
    * Keep working when services are down
    * Rapid prototyping
    * Avoid inter-team bottlenecks
    * Work offline
  * How to mock HTTP?
    * Nock
    * Static JSON
    * Create development webserver
      * api-mock
      * JSON server
      * JSON Schema faker
      * Browsersync
      * Express
  * Our plan for mocking HTTP
    * Declare Schema
      * JSON Schema Faker
    * Generate Random Data
      * faker.js, randexp.js, chance.js
    * Serve Data via API
      * JSON Server
  * Mocking Libraries
    * JSON Schema (standard)
      * json-schema.org
    * JSON Schema Faker
      * faker.js, chance.js, randexp.js
        * github.com/Marak/faker.js/wiki
        * marak.github.io/faker.js/index.html
        * json-schema-faker.js.org
  * Mock Demo
    * bit.ly/ps-mock-data-schema
