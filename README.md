# npmtest-redbox-react

#### basic test coverage for  [redbox-react (v1.3.6)](https://github.com/commissure/redbox-react)  [![npm package](https://img.shields.io/npm/v/npmtest-redbox-react.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-redbox-react) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-redbox-react.svg)](https://travis-ci.org/npmtest/node-npmtest-redbox-react)

#### A redbox (rsod) component to display your errors.

[![NPM](https://nodei.co/npm/redbox-react.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/redbox-react)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-redbox-react/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-redbox-react/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-redbox-react/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-redbox-react/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-redbox-react/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-redbox-react/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-redbox-react/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-redbox-react/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-redbox-react/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-redbox-react/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-redbox-react/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-redbox-react/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-redbox-react/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-redbox-react/build/test-report.html](https://npmtest.github.io/node-npmtest-redbox-react/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-redbox-react/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-redbox-react/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-redbox-react/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-redbox-react/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-redbox-react/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-redbox-react/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-redbox-react/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-redbox-react/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "David Pfahler"
    },
    "bugs": {
        "url": "https://github.com/commissure/redbox-react/issues"
    },
    "dependencies": {
        "error-stack-parser": "^1.3.6",
        "object-assign": "^4.0.1",
        "prop-types": "^15.5.4"
    },
    "description": "A redbox (rsod) component to display your errors.",
    "devDependencies": {
        "babel-cli": "^6.9.0",
        "babel-core": "^6.9.0",
        "babel-loader": "^6.2.4",
        "babel-plugin-rewire": "^1.0.0-rc-3",
        "babel-preset-es2015": "^6.3.3",
        "babel-preset-react": "^6.5.0",
        "babel-preset-stage-0": "^6.3.13",
        "react": "^0.14.0 || ^15.0.0",
        "react-addons-test-utils": "^15.0.0",
        "react-dom": "^0.14.0 || ^15.0.0",
        "rimraf": "^2.5.2",
        "semantic-release": "^4.0.0",
        "standard": "^7.1.1",
        "tap-spec": "^4.0.2",
        "tape": "^4.5.1",
        "webpack": "^1.13.1"
    },
    "directories": {},
    "dist": {
        "shasum": "70314c57c066257eb70b0a24dc794b5cef4f1c4e",
        "tarball": "https://registry.npmjs.org/redbox-react/-/redbox-react-1.3.6.tgz"
    },
    "files": [
        "dist",
        "lib",
        "src"
    ],
    "gitHead": "015f38af2ef1d6c4d1a180050dbc807cc627e4e8",
    "homepage": "https://github.com/commissure/redbox-react",
    "keywords": [
        "redbox",
        "rsod",
        "react",
        "react-native"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "davidpfahler"
        },
        {
            "name": "mxlje"
        }
    ],
    "name": "redbox-react",
    "optionalDependencies": {},
    "peerDependencies": {
        "react": "^0.14.0 || ^15.0.0",
        "react-dom": "^0.14.0 || ^15.0.0"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/commissure/redbox-react.git"
    },
    "scripts": {
        "build": "npm run build:umd && npm run build:umd:min && npm run build:lib",
        "build:lib": "babel src --out-dir lib",
        "build:umd": "webpack src/index.js dist/redbox.js",
        "build:umd:min": "webpack --config webpack.config.prod.js src/index.js dist/redbox.min.js",
        "clean": "rimraf dist lib tmp",
        "prepublish": "npm run clean && npm run build",
        "semantic-release": "semantic-release pre && npm publish && semantic-release post",
        "test": "standard ./src && babel-node ./tests | tap-spec"
    },
    "version": "1.3.6",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
