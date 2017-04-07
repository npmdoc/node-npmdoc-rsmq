# api documentation for  [rsmq (v0.8.2)](https://github.com/smrchy/rsmq#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-rsmq.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-rsmq) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-rsmq.svg)](https://travis-ci.org/npmdoc/node-npmdoc-rsmq)
#### A really simple message queue based on Redis

[![NPM](https://nodei.co/npm/rsmq.png?downloads=true)](https://www.npmjs.com/package/rsmq)

[![apidoc](https://npmdoc.github.io/node-npmdoc-rsmq/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-rsmq_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-rsmq/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-rsmq/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-rsmq/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "P. Liess",
        "email": "smrchy+npm@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/smrchy/rsmq/issues"
    },
    "dependencies": {
        "hiredis": "^0.5.0",
        "lodash": "^4.17.4",
        "redis": "^2.6.5"
    },
    "description": "A really simple message queue based on Redis",
    "devDependencies": {
        "async": "*",
        "mocha": "*",
        "should": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "897166f6405840d1e6c7e98b1405466e1727ff4b",
        "tarball": "https://registry.npmjs.org/rsmq/-/rsmq-0.8.2.tgz"
    },
    "engines": {
        "node": "> 0.10.20"
    },
    "gitHead": "66216b84282c16e810a6d320916218edb691ffba",
    "homepage": "https://github.com/smrchy/rsmq#readme",
    "keywords": [
        "queue",
        "messagequeue",
        "jobs",
        "message-queue",
        "redis"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "smrchy",
            "email": "smrchy@gmail.com"
        }
    ],
    "name": "rsmq",
    "optionalDependencies": {
        "hiredis": "^0.5.0"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/smrchy/rsmq.git"
    },
    "scripts": {
        "test": "mocha ./test/test.js"
    },
    "version": "0.8.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module rsmq](#apidoc.module.rsmq)
1.  boolean <span class="apidocSignatureSpan">rsmq.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">rsmq.</span>EventEmitter ()](#apidoc.element.rsmq.EventEmitter)
1.  [function <span class="apidocSignatureSpan">rsmq.</span>init ()](#apidoc.element.rsmq.init)
1.  [function <span class="apidocSignatureSpan">rsmq.</span>listenerCount (emitter, type)](#apidoc.element.rsmq.listenerCount)
1.  number <span class="apidocSignatureSpan">rsmq.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">rsmq.</span>__super__



# <a name="apidoc.module.rsmq"></a>[module rsmq](#apidoc.module.rsmq)

#### <a name="apidoc.element.rsmq.EventEmitter"></a>[function <span class="apidocSignatureSpan">rsmq.</span>EventEmitter ()](#apidoc.element.rsmq.EventEmitter)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsmq.init"></a>[function <span class="apidocSignatureSpan">rsmq.</span>init ()](#apidoc.element.rsmq.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsmq.listenerCount"></a>[function <span class="apidocSignatureSpan">rsmq.</span>listenerCount (emitter, type)](#apidoc.element.rsmq.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
