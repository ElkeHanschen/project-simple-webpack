# Simple Webpack v4 Boilerplate

## ToDo
- [ ] live reload not working since I moved the index.html and had some changes in dev-server config  
- [ ] having watch running in the background  
- [ ] to check, if autoprefixer works (when having more content)  
- [ ] code review via Micha!  

## Preconditions  
- only Front-End related  
- at point of writing: node v12.12.0, webpack 4.44.1

## Goal
- take HTML, SCSS/CSS, JavaScript files  
- minimize / distribute them into dist folder  
- watch saved files on change  
- distribute on localhost  
- for this, only use the utmost necessary packages  

## Environment set-up  
- for npm, you need node.js  
- check for node / node version in your terminal `node -v`  
- if you don't have it, install it  
#### How? Install node.js via homebrew  
- install node.js via [homebrew](https://formulae.brew.sh/formula/node)  
- run this command in your terminal: `$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`  
- [also see here](https://medium.com/@hayasnc/how-to-install-nodejs-and-npm-on-mac-using-homebrew-b33780287d8f)  
- check for homebrew `brew -v`  
- install node via homebrew `brew install node`  
- check for node again `node -v`  

## npm packages - short explanation
Of course find all of them on [npm](https://www.npmjs.com/package/npm) but to make it easier to follow my approach, a short explanation here:  

#### webpack
Module bundler for JavaScript applications.  
Takes all the code from your application and makes it usable in a web browser.  
Out of the box it only understands JavaScript and JSON.  

#### webpack-cli
Flexible set of commands for DEVs to increase speed when setting up a custom webpack project.  
As of webpack v4, you also need to install -cli.  

#### style-loader - use for Development
Injects CSS into the DOM. 
It's faster than extracting the styles each time, like you do it with mini-css-extract-plugin.  
It’s recommended to combine style-loader with css-loader. 
  
#### mini-css-extract-plugin - use for Production
Extract CSS into separate files.  
It creates a CSS file per JS file which contains CSS.  
It’s recommended to combine mini-css-extract-plugin with css-loader.  

#### css-loader
Interprets `@import` and `url()` like `import/require()` and will resolve them.  

#### postcss-loader and autoprefixer
Parse CSS and add vendor prefixes to CSS.  

#### sass-loader
Loads a Sass/SCSS file and compiles it to CSS.    

#### webpack-dev-server  
Use with a development server that provides live reloading.  
This should be used for development only.  
webpack-dev-server is configured by default to support live-reload of files as you edit your assets while the server is running.  

## Run commands
- `npm run build` builds files for production - minified  
- `npm start` serves on localhost 

#### Trouble shooting
- sometimes it's helpful to delete the dist folder and build files anew  
- for this, run `m -rf ./dist` and build files again with `npm run build` 
- sometimes it's also helpful to delete the node_modules folder and build it anew  
- for this, run `rm -rf node_modules` to delete node_modules and run `npm install` to generate it again  

## Sources
[Article: A tale of Webpack 4 and how to finally configure it in the right way](https://medium.com/hackernoon/a-tale-of-webpack-4-and-how-to-finally-configure-it-in-the-right-way-4e94c8e7e5c1)  
[Github - webpack boilerplate](https://github.com/marharyta/webpack-boilerplate)  

[Webpack Getting Started](https://webpack.js.org/guides/getting-started/)  
[Webpack Development](https://webpack.js.org/guides/development/)  

[Article: How to configure webpack from scratch for a basic website](https://dev.to/pixelgoo/how-to-configure-webpack-from-scratch-for-a-basic-website-46a5)  
[Article, super helpful: Why Webpack](https://blog.andrewray.me/webpack-when-to-use-and-why/)  
 
