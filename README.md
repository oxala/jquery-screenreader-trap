# @ebay/jquery-screenreader-trap

<p>
    <a href="https://travis-ci.org/ianmcburnie/jquery-screenreader-trap"><img src="https://api.travis-ci.org/ianmcburnie/jquery-screenreader-trap.svg?branch=master" alt="Build Status" /></a>
    <a href='https://coveralls.io/github/ianmcburnie/jquery-screenreader-trap?branch=master'><img src='https://coveralls.io/repos/ianmcburnie/jquery-screenreader-trap/badge.svg?branch=master&service=github' alt='Coverage Status' /></a>
</p>

Prevents screen reader's virtual cursor from leaving the confines of an element.

Screenreader-trap is a singleton as there can only ever be one active
screenreader-trap on a page. Creating a new screenreader-trap will disable the
current trap.

```js
$.trapScreenreader($el);
$.untrapScreenreader();
```

## Experimental

This plugin is still in an experimental state, until it reaches v1.0.0 you must
consider all minor releases as breaking changes. Patch releases may introduce
new features, but will be backwards compatible.

Please use the tilde range specifier in your package.json to pin to a fixed
major and minor version.

## Install

```js
npm install @ebay/jquery-screenreader-trap
```

## Events

* screenreaderTrap : fired when screenreader trap is activated
* screenreaderUntrap : fired when screenreader trap is deactivated

## Development

Run `npm start` for test driven development. All tests are located in `test.js`.

Execute `npm run` to view all available CLI scripts:

* `npm start` test driven development: watches code and re-tests after any change
* `npm test` runs tests & generates reports (see reports section below)
* `npm run lintsyntax` lints code for syntax and style (reports errors to jshint.txt)
* `npm run lintstyle` lints code for syntax (reports errors to jscs.txt)
* `npm run lint` lints code for syntax and style
* `npm run fixstyle` attempts to auto fix style errors
* `npm run minify` builds minified version of code
* `npm run jsdoc` generates jsdocs
* `npm run build` minifies code and generates jsdocs
* `npm run clean` deletes all generated files

The following hooks exist, and do not need to be invoked manually:

* `npm prepublish` cleans, lints, tests and builds on every `npm publish` command
* `pre-commit` cleans, lints, tests and builds on every `git commit` command

## Test Reports

Each test run will generate the following reports:

* `/test_reports/coverage` contains Istanbul code coverage report
* `/test_reports/html` contains HTML test report
* `/test_reports/junit` contains JUnit test report

## JSDocs

JSDocs are generated under `./jsdoc` folder.

## CI Build

https://travis-ci.org/ianmcburnie/jquery-screenreader-trap

## Code Coverage

https://coveralls.io/github/ianmcburnie/jquery-screenreader-trap?branch=master
