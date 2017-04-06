# api documentation for  [grunt-env (v0.4.4)](https://github.com/jsoverson/grunt-env)  [![npm package](https://img.shields.io/npm/v/npmdoc-grunt-env.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-grunt-env) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-grunt-env.svg)](https://travis-ci.org/npmdoc/node-npmdoc-grunt-env)
#### Specify an ENV configuration for future tasks in the chain

[![NPM](https://nodei.co/npm/grunt-env.png?downloads=true)](https://www.npmjs.com/package/grunt-env)

[![apidoc](https://npmdoc.github.io/node-npmdoc-grunt-env/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-grunt-env_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-grunt-env/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-grunt-env/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-grunt-env/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jarrod Overson",
        "email": "jsoverson@gmail.com",
        "url": "http://jarrodoverson.com/"
    },
    "bugs": {
        "url": "https://github.com/jsoverson/grunt-env/issues"
    },
    "dependencies": {
        "ini": "~1.3.0",
        "lodash": "~2.4.1"
    },
    "description": "Specify an ENV configuration for future tasks in the chain",
    "devDependencies": {
        "grunt": "~0.4.5",
        "grunt-contrib-clean": "~0.6.0",
        "grunt-contrib-jshint": "~0.11.0",
        "grunt-jscs": "^1.5.0"
    },
    "directories": {},
    "dist": {
        "shasum": "3b38843a8d737177ddc9f893879fb69ce1a0bc2f",
        "tarball": "https://registry.npmjs.org/grunt-env/-/grunt-env-0.4.4.tgz"
    },
    "engines": {
        "node": "*"
    },
    "gitHead": "37d6b5113a6780a3a35eb8bd98633970470f6d9a",
    "homepage": "https://github.com/jsoverson/grunt-env",
    "keywords": [
        "gruntplugin",
        "env",
        "config"
    ],
    "licenses": [
        {
            "type": "Apache2",
            "url": "https://github.com/jsoverson/grunt-env/blob/master/LICENSE-Apache2"
        }
    ],
    "maintainers": [
        {
            "name": "jsoverson",
            "email": "jsoverson@gmail.com"
        },
        {
            "name": "stephane.bachelier",
            "email": "stephane.bachelier@gmail.com"
        }
    ],
    "name": "grunt-env",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/jsoverson/grunt-env.git"
    },
    "scripts": {
        "test": "grunt"
    },
    "version": "0.4.4"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module grunt-env](#apidoc.module.grunt-env)
1.  object <span class="apidocSignatureSpan">grunt-env.</span>utils

#### [module grunt-env.utils](#apidoc.module.grunt-env.utils)
1.  [function <span class="apidocSignatureSpan">grunt-env.utils.</span>parse (grunt, file)](#apidoc.element.grunt-env.utils.parse)



# <a name="apidoc.module.grunt-env"></a>[module grunt-env](#apidoc.module.grunt-env)



# <a name="apidoc.module.grunt-env.utils"></a>[module grunt-env.utils](#apidoc.module.grunt-env.utils)

#### <a name="apidoc.element.grunt-env.utils.parse"></a>[function <span class="apidocSignatureSpan">grunt-env.utils.</span>parse (grunt, file)](#apidoc.element.grunt-env.utils.parse)
- description and source-code
```javascript
parse = function (grunt, file) {
  var match = file.match(extensionPattern);
  var type = match ? match[1] : 'default'; // default to ini format

  try {
    var parseFn = types[type] || types.default;
    return parseFn(grunt, file) || {};
  } catch (e) {
    return;
  }
}
```
- example usage
```shell
...
} catch (e) {
  return;
}
}

function readIni(grunt, file) {
try {
  return ini.parse(grunt.file.read(file));
} catch (e) {
  return;
}
}

module.exports = {
// Export a single parse function that call the proper parsing function
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
