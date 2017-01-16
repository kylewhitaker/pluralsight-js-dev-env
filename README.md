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
