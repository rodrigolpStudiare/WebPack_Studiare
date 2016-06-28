# WebPack_Studiare
WebPack Start Point Documentation and Examples (Compilation of knowledge)

Useful Links (recommended order)

## RequireJS
- [DA2k-Blog](http://blog.da2k.com.br/2015/01/18/requirejs-carregando-javacript-sob-demanda/)
- [RequireJS.org](http://requirejs.org/docs/start.html)

## Modularization in JavaScript
- [Tableless](http://tableless.com.br/modularizacao-em-javascript/)

## Browserify
- [Começando com o Browserify](http://diogo.nu/comecando-com-o-browserify/)
- [Modularizando Frontend JavaScript](https://udgwebdev.com/modularizando-frontend-javascript-com-browserify)

## ReactJS on Rails Project
- [A guide for Rails developers](https://www.airpair.com/reactjs/posts/reactjs-a-guide-for-rails-developers)
- [ReacJS with Browserify and Npm](http://codeutopia.net/blog/2016/01/25/getting-started-with-npm-and-browserify-in-a-react-project/)

## Webpack
- [webpack oficial site](http://webpack.github.io/)

  - [Code Splitting](http://webpack.github.io/docs/code-splitting.html)
  
  - [Setup the Compitation](http://webpack.github.io/docs/tutorials/getting-started/)
  
  - [Getting Started](http://webpack.github.io/docs/usage.html)

## Webpack with Rails
- [How to use?](http://clarkdave.net/2015/01/how-to-use-webpack-with-rails/)
- [Configuration for Rich Client](http://www.railsonmaui.com/blog/2014/10/03/integrating-webpack-and-the-es6-transpiler-into-an-existing-rails-project/)

## React and Rails Integration Using Webpack
- [Motivation](https://www.netguru.co/blog/react-rails-webpack)
- [Npm generator-rails-react-webpack](https://www.npmjs.com/package/generator-rails-react-webpack)

## Summary

#### What is Webpack?
It's a framework that takes modules with dependencies and generates static assets representing those modules.

#### Why use webpack (Gols):
- **Split the dependency tree into chunks loaded on demand.**
  - help you separate the JS for different pages into different files, with ‘common’ modules automatically shared across all pages.
  - split off large modules into separate files which are only downloaded on demand (via require.ensure).
- **Keep initial loading time low.**
- Every static asset should be able to be a module.
- Ability to integrate 3rd-party libraries as modules.
- Ability to customize nearly every part of the module bundler.
- Suited for big projects.
- webpack co-existing with sprockets (is not used or required for development or production use of this gem).
- Its Webpack Dev Server rocks for quick prototypes (Hot Module Replacement) of JS and CSS/Sass code.

#### Why not use webpack:
- It requires a lot of code adaptation, which is so cumbersome as greater as your project.
- Because webpack is a node.js application, you’ll need node, bower or anything else installed to run.
- The official documentation is obscure. You need to read a lot more to have a clear understanding of the subject.

#### Installation Process

  - Preparing Rails for webpack
    - **Untangling Sprockets**: Empty out your `app/assets/javascripts` directory. We’ll be configuring webpack to output its bundles here, so they can then be picked up by Sprockets. All our actual JS code will live elsewhere.
    - **Add this to your** `.gitignore`: `/app/assets/javascripts`. We need this for the deploy step.
  
  - New folder for JavaScript
    - **Create new folder path** `app/frontend/javascripts`: Will be the folder for your actual javaScrict, entries and anything else.
  
  - Install Webpack
    - **Create a package manager file**: Because webpack is a node.js application, we’ll need a `package.json` file in our Rails root. See an example below.
    ```
    {
      "name": "my-rails-app",
      "description": "my-rails-app",
      "version": "1.0.0",
      "devDependencies": {
        "webpack": "~1.4.13",
        "expose-loader": "~0.6.0",
        "imports-loader": "~0.6.3",
        "exports-loader": "~0.6.2",
        "lodash": "~2.4.1"
      },
      "dependencies": {}
    }
    ```
    - **Install with node npm** `npm install`
    - **Install webpack globally**: Do that to get access for `webpack command line tool`.
  
  - Configure Webpack
    - ...
    ```
    var path = require('path');
    var webpack = require('webpack');

    var config = module.exports = {
      // the base path which will be used to resolve entry points
      context: __dirname,
      // the main entry point for our application's frontend JS
      entry: './app/frontend/javascripts/entry.js',
    };
    ```



