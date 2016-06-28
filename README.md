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
- ...
