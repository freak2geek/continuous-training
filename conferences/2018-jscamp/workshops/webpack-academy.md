# Webpack Academy

*When: 18-07-2018 | 09:00 - 13:00*, *Where: Barcelona*

Speakers: [Sean Larkin](https://jscamp.tech/workshops/webpack-academy/#speaker-1), [Juho Vepsäläinen](https://jscamp.tech/workshops/webpack-academy/#speaker-2) and [Johannes Ewald](https://jscamp.tech/workshops/webpack-academy/#speaker-3)

## Expectations

- Get a better grasp about Webpack foundation and capabilities.

- Better understanding of techniques to achieve high-performance like code-splitting, long-term caching, tree shaking and others.

- More confidence to understand and make right front-end/back-end architecture decisions for the next projects.

- Understand how Webpack can be integrated in my existing workflows, like improve the meteor integration.

- Get new skills to contribute to Webpack projects, such us custom loaders and plugins, [`meteor-webpack`](https://github.com/ardatan/meteor-webpack) and etc.

## Workshop ideas

### History

- First Webpack versions were having "scary" documentation. They put efforts to improve that part until current version.

### Why Webpack

Origins:
To load JS in the browser, just inline or file scripts loaded within your html structure. Don't scale. Bottelneck, Too many requests. Unmaintainable scripts. Scope, size, readability, frgability, monolith files.

Solution:

IIFE's Immediately invoked function expression. `(function(){})()` Intercommunication between independent block scopes. Reveal module pattern, the beggining of modules. Every file as an IIFE. Lots of IIFE's are slow in the browser runtime.

JS modules raised:

CommonJs (Modules 1.0). Expose fuctionality from files. Good to static analysis, following imports and require segments. NPM+Node+Modules. Problems: No browser support. No live bindings. Loader slow. No static async. Lazy Loading. Not everyone shipping JS. No rules in JS for shipping modules.

Bundlers. Graph of dependencies. => Browserify, RequireJS,... AMD. `define('lib', function(lib) {})`. Too dynamic of lazy loading.

ESM. `import {} from 'lib'; [...] export const whatever;` Reusable, organized, encapsulated. ESM for browser is very slow. The browser has to do a lot on runtime.

Webpack. Module bundler. Handle all module formats, even mixed. Compile to use all together in the browser.

Ways to use it. Config. Webpack CLI. Node API.

### Hands on

- Run webpack
- Use mode property, development is optimized for dev dependencies, production for small bundles.
- Build: transversing the dependency tree and see what have changed.
- Export function from webpack config. Pass env parameters. Custom modes?
- Support all the browser: web-dev-server, express.
- Hot module replacement: Live updates that keep the state.

#### Core concepts

Main concepts for the Webpack process. Entry, Output, Loader, Plugins.

- Loader, function transformation, src => src (modified state), configured by rules, you can apply options. Interprate, translate, and tranform per-file basis before adding to deph graph.
- rule object: { test: what file to apply, use: which loader to use } + matcher conditions (include, exclude) + enforce (when to run the loaders).
- Resolve loaders: right to left: ['loader3', 'loader2', 'loader1'] => loader3(loader2(loader1(src)))

- Plugins: implement apply function, its body listens different events from a compiler. Webpack, event-driven system, everything is a plugin. They can easily extend or drop any feature.

- Webpack-merge, isolate configuration, partial definitions and merge them together. (feature/09-sm-using-presets)

- Webpack-analyzer

- Hot module API included within the loaders, E.g css-loader

- Url loader, tell webpack to analyze any kind of files, eg. svg.

- image-webpack-loader. compress images or other kind of files.

#### Web performance

Initial download of JS
Initial download of CSS
Network requests on initial download

Code splitting, process of splitting code into pierces of codes that are loaded asyncronously in chuncks.
Load less code, specially in mobile devices.
Static: Heavy JS, anything temporal, Routes.
react-loadable

dynamic: you can pass variables to build routes. Application: Locales.

Use coverage tool for the browser.

A spinner is just a sign that you need to improve your web performance

## References

- See: [JSCamp entry](https://jscamp.tech/workshops/webpack-academy/)

- Fork: [Webpack Course](https://github.com/Gywem/webpack-workshop-2018)

-Read: [Learning JavaScript Design Patterns](https://www.amazon.es/Learning-JavaScript-Design-Patterns-Osmani/dp/1449331815/ref=sr_1_1?ie=UTF8&qid=1531899669&sr=8-1&keywords=javascript+design+patterns)
