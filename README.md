# npmdoc-mongodb

#### api documentation for  [mongodb (v2.2.26)](https://github.com/mongodb/node-mongodb-native)  [![npm package](https://img.shields.io/npm/v/npmdoc-mongodb.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mongodb) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mongodb.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mongodb)

#### The official MongoDB driver for Node.js

[![NPM](https://nodei.co/npm/mongodb.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/mongodb)

- [https://npmdoc.github.io/node-npmdoc-mongodb/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-mongodb/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mongodb/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mongodb/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-mongodb/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-mongodb/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Christian Kvalheim"
    },
    "bugs": {
        "url": "https://github.com/mongodb/node-mongodb-native/issues"
    },
    "dependencies": {
        "es6-promise": "3.2.1",
        "mongodb-core": "2.1.10",
        "readable-stream": "2.2.7"
    },
    "description": "The official MongoDB driver for Node.js",
    "devDependencies": {
        "JSONStream": "^1.0.7",
        "betterbenchmarks": "^0.1.0",
        "bluebird": "3.4.6",
        "bson": "latest",
        "cli-table": "^0.3.1",
        "co": "4.6.0",
        "colors": "^1.1.2",
        "coveralls": "^2.11.6",
        "eslint": "^3.8.1",
        "event-stream": "^3.3.2",
        "gleak": "0.5.0",
        "integra": "0.1.8",
        "jsdoc": "3.4.0",
        "ldjson-stream": "^1.2.1",
        "mongodb-extended-json": "1.7.1",
        "mongodb-topology-manager": "1.0.x",
        "mongodb-version-manager": "github:christkv/mongodb-version-manager#master",
        "nyc": "^8.1.0",
        "optimist": "0.6.1",
        "rimraf": "2.5.4",
        "semver": "5.3.0",
        "worker-farm": "^1.3.1"
    },
    "directories": {},
    "dist": {
        "shasum": "1bd50c557c277c98e1a05da38c9839c4922b034a",
        "tarball": "https://registry.npmjs.org/mongodb/-/mongodb-2.2.26.tgz"
    },
    "engines": {
        "node": ">=0.10.3"
    },
    "gitHead": "fce57db6d9d56b3943b8a646590b489988cb8e08",
    "homepage": "https://github.com/mongodb/node-mongodb-native",
    "keywords": [
        "mongodb",
        "driver",
        "official"
    ],
    "license": "Apache-2.0",
    "main": "index.js",
    "maintainers": [
        {
            "name": "christkv"
        }
    ],
    "name": "mongodb",
    "nyc": {
        "include": [
            "lib/**/*.js"
        ]
    },
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/mongodb/node-mongodb-native.git"
    },
    "scripts": {
        "coverage": "nyc node test/runner.js -t functional && node_modules/.bin/nyc report --reporter=text-lcov | node_modules/.bin/coveralls",
        "lint": "eslint lib",
        "test": "node test/runner.js -t functional -l"
    },
    "version": "2.2.26"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
