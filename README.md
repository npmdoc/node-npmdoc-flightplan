# api documentation for  [flightplan (v0.6.15)](https://github.com/pstadler/flightplan)  [![npm package](https://img.shields.io/npm/v/npmdoc-flightplan.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-flightplan) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-flightplan.svg)](https://travis-ci.org/npmdoc/node-npmdoc-flightplan)
#### Library for streamlining application deployment or systems administration tasks

[![NPM](https://nodei.co/npm/flightplan.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/flightplan)

[![apidoc](https://npmdoc.github.io/node-npmdoc-flightplan/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-flightplan/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-flightplan/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-flightplan/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Patrick Stadler"
    },
    "bin": {
        "fly": "./bin/fly.js"
    },
    "bugs": {
        "url": "https://github.com/pstadler/flightplan/issues"
    },
    "dependencies": {
        "byline": "^4.2.1",
        "chalk": "^1.1.1",
        "fibers": "^1.0.10",
        "interpret": "^1.0.0",
        "liftoff": "^2.2.0",
        "nopt": "^3.0.4",
        "pretty-hrtime": "^1.0.1",
        "prompt": "^0.2.14",
        "semver": "^5.1.0",
        "ssh2": "^0.4.15",
        "util-extend": "^1.0.1",
        "v8flags": "^2.0.10"
    },
    "description": "Library for streamlining application deployment or systems administration tasks",
    "devDependencies": {
        "chai": "^3.3.0",
        "coveralls": "^2.11.4",
        "eslint": "^1.10.3",
        "istanbul": "^0.4.0",
        "markdox": "^0.1.10",
        "mocha": "^2.3.3",
        "pre-commit": "^1.1.1",
        "proxyquire": "^1.7.3",
        "sinon": "^1.17.2"
    },
    "directories": {},
    "dist": {
        "shasum": "f8dff79554a02daff87f1c584aaf7ac7477c846c",
        "tarball": "https://registry.npmjs.org/flightplan/-/flightplan-0.6.15.tgz"
    },
    "gitHead": "9e04ecf71677222b7d8460ffffbcac9b30f51b45",
    "homepage": "https://github.com/pstadler/flightplan",
    "keywords": [
        "deploy",
        "deployment",
        "commands",
        "devops",
        "exec",
        "shell",
        "bash",
        "ssh",
        "tasks",
        "parallel",
        "sequential",
        "remote",
        "local",
        "cloud",
        "fabric"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "pstadler"
        }
    ],
    "name": "flightplan",
    "optionalDependencies": {},
    "pre-commit": [
        "lint"
    ],
    "repository": {
        "type": "git",
        "url": "git+https://github.com/pstadler/flightplan.git"
    },
    "scripts": {
        "coverage": "rm -rf ./coverage; ./node_modules/.bin/istanbul cover --dir coverage/lib ./node_modules/.bin/_mocha -- -R spec; ./node_modules/.bin/istanbul report",
        "coverage-lcov": "rm -rf ./coverage; ./node_modules/.bin/istanbul cover --dir coverage/lib --report lcovonly ./node_modules/.bin/_mocha -- -R spec; ./node_modules/.bin/istanbul report lcovonly",
        "coveralls": "npm run coverage-lcov && cat ./coverage/lcov.info | ./node_modules/.bin/coveralls",
        "docs": "cd ./docs; node generate.js",
        "lint": "eslint .",
        "test": "mocha"
    },
    "version": "0.6.15"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module flightplan](#apidoc.module.flightplan)
1.  object <span class="apidocSignatureSpan">flightplan.</span>_flights
1.  object <span class="apidocSignatureSpan">flightplan.</span>_targets
1.  object <span class="apidocSignatureSpan">flightplan.</span>runtime



# <a name="apidoc.module.flightplan"></a>[module flightplan](#apidoc.module.flightplan)



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
