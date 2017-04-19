# npmdoc-simple-statistics

#### api documentation for  [simple-statistics (v3.0.0)](https://github.com/simple-statistics/simple-statistics#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-simple-statistics.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-simple-statistics) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-simple-statistics.svg)](https://travis-ci.org/npmdoc/node-npmdoc-simple-statistics)

#### Simple Statistics

[![NPM](https://nodei.co/npm/simple-statistics.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/simple-statistics)

- [https://npmdoc.github.io/node-npmdoc-simple-statistics/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-simple-statistics/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-simple-statistics/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-simple-statistics/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-simple-statistics/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-simple-statistics/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tom MacWright",
        "url": "http://macwright.org/"
    },
    "bugs": {
        "url": "https://github.com/simple-statistics/simple-statistics/issues"
    },
    "config": {
        "commitizen": {
            "path": "./node_modules/cz-conventional-changelog"
        }
    },
    "dependencies": {},
    "description": "Simple Statistics",
    "devDependencies": {
        "are-we-flow-yet": "^1.0.0",
        "browserify": "^14.1.0",
        "bundle-collapser": "^1.0.0",
        "cz-conventional-changelog": "^1.2.0",
        "eslint": "^3.8.1",
        "exorcist": "^0.4.0",
        "flow-bin": "^0.39.0",
        "jsdoctest": "1.7.0",
        "mocha": "3.2.0",
        "random-js": "^1.0.4",
        "standard-changelog": "^0.0.1",
        "tap": "^10.1.1",
        "uglify-js": "^2.6.2"
    },
    "directories": {},
    "dist": {
        "shasum": "54b66d2655b2a21125600dc0d02be764a3a73a3d",
        "tarball": "https://registry.npmjs.org/simple-statistics/-/simple-statistics-3.0.0.tgz"
    },
    "engines": {
        "node": "*"
    },
    "files": [
        "bower.json",
        "src",
        "dist"
    ],
    "gitHead": "9bb0cda4c8b64bbc1924c7270f6beeee0be1411a",
    "homepage": "https://github.com/simple-statistics/simple-statistics#readme",
    "keywords": [
        "descriptive",
        "linear",
        "math",
        "probability",
        "regression",
        "statistics"
    ],
    "license": "ISC",
    "main": "index.js",
    "maintainers": [
        {
            "name": "tmcw"
        }
    ],
    "name": "simple-statistics",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/simple-statistics/simple-statistics.git"
    },
    "scripts": {
        "build": "npm run bundle && npm run minify",
        "bundle": "mkdir -p dist && browserify -p bundle-collapser/plugin -s ss index.js --debug | exorcist dist/simple-statistics.js.map > dist/simple-statistics.js",
        "changelog": "standard-changelog -i CHANGELOG.md --overwrite",
        "jsdoctest": "mocha --require jsdoctest index.js",
        "minify": "uglifyjs dist/simple-statistics.js -c -m --in-source-map=dist/simple-statistics.js.map --source-map=dist/simple-statistics.min.js.map -o dist/simple-statistics.min.js",
        "prepublish": "npm run build && ./scripts/update_readme.js",
        "test": "are-we-flow-yet src && flow check src && eslint index.js src/*.js test/*.js && tap --coverage test/*.js && npm run jsdoctest",
        "test-sauce": "node scripts/browser_test.js"
    },
    "version": "3.0.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
