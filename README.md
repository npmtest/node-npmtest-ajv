# test coverage for  [ajv (v4.11.6)](https://github.com/epoberezkin/ajv)  [![npm package](https://img.shields.io/npm/v/npmtest-ajv.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-ajv) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-ajv.svg)](https://travis-ci.org/npmtest/node-npmtest-ajv)
#### Another JSON Schema Validator

[![NPM](https://nodei.co/npm/ajv.png?downloads=true)](https://www.npmjs.com/package/ajv)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-ajv/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-ajv/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-ajv/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-ajv/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-ajv/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-ajv/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-ajv/tree/gh-pages/build)|

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-ajv/build/screenCapture.buildCustomOrg.browser.coverage.html.png)](https://npmtest.github.io/node-npmtest-ajv/build/coverage.html/index.html)

[![test-report](https://npmtest.github.io/node-npmtest-ajv/build/screenCapture.buildCustomOrg.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmtest%252Fnode-npmtest-ajv%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-ajv/build/test-report.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-ajv/build/screenCapture.buildApidoc.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmdoc%252Fnode-npmdoc-ajv%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-ajv/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-ajv/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-ajv/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Evgeny Poberezkin"
    },
    "bugs": {
        "url": "https://github.com/epoberezkin/ajv/issues"
    },
    "dependencies": {
        "co": "^4.6.0",
        "json-stable-stringify": "^1.0.1"
    },
    "description": "Another JSON Schema Validator",
    "devDependencies": {
        "bluebird": "^3.1.5",
        "brfs": "^1.4.3",
        "browserify": "^14.1.0",
        "chai": "^3.5.0",
        "coveralls": "^2.11.4",
        "del-cli": "^0.2.1",
        "dot": "^1.0.3",
        "eslint": "^3.2.2",
        "gh-pages-generator": "^0.2.0",
        "glob": "^7.0.0",
        "if-node-version": "^1.0.0",
        "js-beautify": "^1.5.6",
        "jshint": "^2.8.0",
        "json-schema-test": "^1.1.1",
        "karma": "^1.0.0",
        "karma-chrome-launcher": "^2.0.0",
        "karma-mocha": "^1.1.1",
        "karma-phantomjs-launcher": "^1.0.0",
        "karma-sauce-launcher": "^1.1.0",
        "mocha": "^3.0.0",
        "nodent": "^3.0.17",
        "nyc": "^10.0.0",
        "phantomjs-prebuilt": "^2.1.4",
        "pre-commit": "^1.1.1",
        "regenerator": "0.9.7",
        "require-globify": "^1.3.0",
        "typescript": "^2.0.3",
        "uglify-js": "^2.6.1",
        "watch": "^1.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "947e93049790942b2a2d60a8289b28924d39f987",
        "tarball": "https://registry.npmjs.org/ajv/-/ajv-4.11.6.tgz"
    },
    "files": [
        "lib/",
        "dist/",
        "scripts/",
        "LICENSE",
        ".tonic_example.js"
    ],
    "gitHead": "75653f78b2a7ef338f8a17a51f0c5cdb79e6e5a3",
    "homepage": "https://github.com/epoberezkin/ajv",
    "keywords": [
        "JSON",
        "schema",
        "validator",
        "validation",
        "jsonschema",
        "json-schema",
        "json-schema-validator",
        "json-schema-validation"
    ],
    "license": "MIT",
    "main": "lib/ajv.js",
    "maintainers": [
        {
            "name": "blakeembrey",
            "email": "hello@blakeembrey.com"
        },
        {
            "name": "esp",
            "email": "e.poberezkin@me.com"
        }
    ],
    "name": "ajv",
    "nyc": {
        "exclude": [
            "**/spec/**",
            "node_modules"
        ],
        "reporter": [
            "lcov",
            "text-summary"
        ]
    },
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/epoberezkin/ajv.git"
    },
    "scripts": {
        "build": "del-cli lib/dotjs/*.js && node scripts/compile-dots.js",
        "bundle": "node ./scripts/bundle.js . Ajv pure_getters",
        "bundle-all": "del-cli dist && npm run bundle && npm run bundle-regenerator && npm run bundle-nodent",
        "bundle-beautify": "node ./scripts/bundle.js js-beautify",
        "bundle-nodent": "node ./scripts/bundle.js nodent",
        "bundle-regenerator": "node ./scripts/bundle.js regenerator",
        "eslint": "if-node-version \">=4\" eslint lib/*.js lib/compile/*.js spec scripts",
        "jshint": "jshint lib/*.js lib/**/*.js --exclude lib/dotjs/**/*",
        "prepublish": "npm run build && npm run bundle-all",
        "test": "npm run jshint && npm run eslint && npm run test-ts && npm run build && npm run test-cov && if-node-version 4 npm run test-browser",
        "test-browser": "del-cli .browser && npm run bundle-all && scripts/prepare-tests && npm run test-karma",
        "test-cov": "nyc npm run test-spec",
        "test-debug": "mocha spec/*.spec.js --debug-brk -R spec",
        "test-fast": "AJV_FAST_TEST=true npm run test-spec",
        "test-karma": "karma start --single-run --browsers PhantomJS",
        "test-spec": "mocha spec/*.spec.js -R spec",
        "test-ts": "tsc --target ES5 --noImplicitAny lib/ajv.d.ts",
        "watch": "watch 'npm run build' ./lib/dot"
    },
    "tonicExampleFilename": ".tonic_example.js",
    "typings": "lib/ajv.d.ts",
    "version": "4.11.6",
    "webpack": "dist/ajv.bundle.js"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
