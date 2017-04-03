# api documentation for  [flightplan (v0.6.15)](https://github.com/pstadler/flightplan)  [![npm package](https://img.shields.io/npm/v/npmdoc-flightplan.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-flightplan) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-flightplan.svg)](https://travis-ci.org/npmdoc/node-npmdoc-flightplan)
#### Library for streamlining application deployment or systems administration tasks

[![NPM](https://nodei.co/npm/flightplan.png?downloads=true)](https://www.npmjs.com/package/flightplan)

[![apidoc](https://npmdoc.github.io/node-npmdoc-flightplan/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-flightplan_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-flightplan/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-flightplan/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-flightplan/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Patrick Stadler",
        "email": "patrick.stadler@gmail.com"
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
            "name": "pstadler",
            "email": "patrick.stadler@gmail.com"
        }
    ],
    "name": "flightplan",
    "optionalDependencies": {},
    "pre-commit": [
        "lint"
    ],
    "readme": "ERROR: No README data found!",
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
1.  object <span class="apidocSignatureSpan">flightplan.</span>errors
1.  object <span class="apidocSignatureSpan">flightplan.</span>runtime

#### [module flightplan.errors](#apidoc.module.flightplan.errors)
1.  [function <span class="apidocSignatureSpan">flightplan.errors.</span>AbortedError (message)](#apidoc.element.flightplan.errors.AbortedError)
1.  [function <span class="apidocSignatureSpan">flightplan.errors.</span>BaseError (message)](#apidoc.element.flightplan.errors.BaseError)
1.  [function <span class="apidocSignatureSpan">flightplan.errors.</span>CommandExitedAbnormallyError (message)](#apidoc.element.flightplan.errors.CommandExitedAbnormallyError)
1.  [function <span class="apidocSignatureSpan">flightplan.errors.</span>ConnectionFailedError (message)](#apidoc.element.flightplan.errors.ConnectionFailedError)
1.  [function <span class="apidocSignatureSpan">flightplan.errors.</span>InvalidArgumentError (message)](#apidoc.element.flightplan.errors.InvalidArgumentError)
1.  [function <span class="apidocSignatureSpan">flightplan.errors.</span>InvalidTargetError (message)](#apidoc.element.flightplan.errors.InvalidTargetError)
1.  [function <span class="apidocSignatureSpan">flightplan.errors.</span>ProcessInterruptedError (message)](#apidoc.element.flightplan.errors.ProcessInterruptedError)



# <a name="apidoc.module.flightplan"></a>[module flightplan](#apidoc.module.flightplan)



# <a name="apidoc.module.flightplan.errors"></a>[module flightplan.errors](#apidoc.module.flightplan.errors)

#### <a name="apidoc.element.flightplan.errors.AbortedError"></a>[function <span class="apidocSignatureSpan">flightplan.errors.</span>AbortedError (message)](#apidoc.element.flightplan.errors.AbortedError)
- description and source-code
```javascript
function AbortedError(message) {
  AbortedError.super_.call(this, message);
  Error.captureStackTrace(this, this.constructor);
  this.name = this.constructor.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flightplan.errors.BaseError"></a>[function <span class="apidocSignatureSpan">flightplan.errors.</span>BaseError (message)](#apidoc.element.flightplan.errors.BaseError)
- description and source-code
```javascript
function BaseError(message) {
  BaseError.super_.call(this, message);
  Error.captureStackTrace(this, this.constructor);
  this.message = message;
  this.name = this.constructor.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flightplan.errors.CommandExitedAbnormallyError"></a>[function <span class="apidocSignatureSpan">flightplan.errors.</span>CommandExitedAbnormallyError (message)](#apidoc.element.flightplan.errors.CommandExitedAbnormallyError)
- description and source-code
```javascript
function CommandExitedAbnormallyError(message) {
  CommandExitedAbnormallyError.super_.call(this, message);
  Error.captureStackTrace(this, this.constructor);
  this.name = this.constructor.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flightplan.errors.ConnectionFailedError"></a>[function <span class="apidocSignatureSpan">flightplan.errors.</span>ConnectionFailedError (message)](#apidoc.element.flightplan.errors.ConnectionFailedError)
- description and source-code
```javascript
function ConnectionFailedError(message) {
  ConnectionFailedError.super_.call(this, message);
  Error.captureStackTrace(this, this.constructor);
  this.name = this.constructor.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flightplan.errors.InvalidArgumentError"></a>[function <span class="apidocSignatureSpan">flightplan.errors.</span>InvalidArgumentError (message)](#apidoc.element.flightplan.errors.InvalidArgumentError)
- description and source-code
```javascript
function InvalidArgumentError(message) {
  InvalidArgumentError.super_.call(this, message);
  Error.captureStackTrace(this, this.constructor);
  this.name = this.constructor.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flightplan.errors.InvalidTargetError"></a>[function <span class="apidocSignatureSpan">flightplan.errors.</span>InvalidTargetError (message)](#apidoc.element.flightplan.errors.InvalidTargetError)
- description and source-code
```javascript
function InvalidTargetError(message) {
  InvalidTargetError.super_.call(this, message);
  Error.captureStackTrace(this, this.constructor);
  this.name = this.constructor.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flightplan.errors.ProcessInterruptedError"></a>[function <span class="apidocSignatureSpan">flightplan.errors.</span>ProcessInterruptedError (message)](#apidoc.element.flightplan.errors.ProcessInterruptedError)
- description and source-code
```javascript
function ProcessInterruptedError(message) {
  ProcessInterruptedError.super_.call(this, message);
  Error.captureStackTrace(this, this.constructor);
  this.name = this.constructor.name;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
