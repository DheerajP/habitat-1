# bldr Web

This is the web application for the bldr SaaS.

This is a single page app built using [Angular 2](https://angular.io/).

## Development

Node.js 4.2.4 must be installed.

Run `npm install` to install dependencies.

To run a development web server, run `npm start`.

### Tasks

These are defined in [package.json](package.json) and can be run with `npm run
TASK_NAME`.

* `build`: Build the JS and CSS
* `build-css`
* `build-css-watch`: Build the CSS and watch for changes
* `build-js`
* `build-js-watch`
* `clean`: Remove files created by build tasks
* `clean-css`
* `clean-js`
* `lint`: Check TS and SCSS files for lint errors
* `lint-css`
* `lint-css-watch`
* `lint-js`
* `lint-js-watch`
* `repl`: Start a TypeScript REPL
* `start`: Watch for changes and start a development server running on port 3000

### Code Style Conventions

These are guidelines for how to structure and format code in the application.

* TypeScript is linted with [TSLint](http://palantir.github.io/tslint/). The
  rules followed in this repository are in the [tslint.json](tslint.json) file.
  Check your code with `npm run lint-js`.
* SCSS is linted with [Sass Lint](https://github.com/sasstools/sass-lint). The
  rules followed in this repository are in the [.sass-lint.yml](.sass-lint.yml)
  file. Check your code with `npm run lint-css`.
* TypeScript files should be named the same name as their default export (or the
  main thing they are concerned with, if there is no default export), so if a
  file has `export default class AppComponent {}`, it should be named
  AppComponent.ts. If a module exports many things, it should given an
  appropriate name and use camelCase.
* Directories should be made for components and their associated files when
  there is more than one file that pertains to a component.
* Directories that end in -page/ and components that are SomethingPageComponent
  are "page components", meaning they represent something that functions as a
  page in the app. All of these should be used in the `RouteConfig` of the
  AppComponent.
* Directory names and SCSS file names should use snake-case.
* SCSS files should start with an underscore and use snake-case:
  \_my-thing.scss. (in Sass, files that start with underscore are partials and
  can be loaded into other files. [app/app.scss](app/app.scss) imports these
  files.)

## "Production"

To build the JavaScript and CSS files, run `npm run build`.

`npm run dist` will build these files and put them along with the index.html and
other needed files into the dist/ directory. A web server can serve the files in
the dist directory to run the app.

## Additional Documentation

* [Why are there so many files and what do all of them mean?](doc/files.md)