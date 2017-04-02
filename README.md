# api documentation for  [mustache (v2.3.0)](https://github.com/janl/mustache.js)  [![npm package](https://img.shields.io/npm/v/npmdoc-mustache.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mustache) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mustache.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mustache)
#### Logic-less {{mustache}} templates with JavaScript

[![NPM](https://nodei.co/npm/mustache.png?downloads=true)](https://www.npmjs.com/package/mustache)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mustache/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-mustache_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mustache/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-mustache/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "mustache.js Authors",
        "email": "http://github.com/janl/mustache.js"
    },
    "bin": {
        "mustache": "./bin/mustache"
    },
    "bugs": {
        "url": "https://github.com/janl/mustache.js/issues"
    },
    "dependencies": {},
    "description": "Logic-less {{mustache}} templates with JavaScript",
    "devDependencies": {
        "chai": "^3.4.0",
        "eslint": "^2.5.1",
        "mocha": "^3.0.2",
        "zuul": "^3.11.0"
    },
    "directories": {},
    "dist": {
        "shasum": "4028f7778b17708a489930a6e52ac3bca0da41d0",
        "tarball": "https://registry.npmjs.org/mustache/-/mustache-2.3.0.tgz"
    },
    "engines": {
        "npm": ">=1.4.0"
    },
    "files": [
        "mustache.js",
        "mustache.min.js",
        "bin",
        "wrappers",
        "LICENSE"
    ],
    "gitHead": "23beb3a8805c9a857e3ea777431481599fab503e",
    "greenkeeper": {
        "ignore": [
            "eslint"
        ]
    },
    "homepage": "https://github.com/janl/mustache.js",
    "keywords": [
        "mustache",
        "template",
        "templates",
        "ejs"
    ],
    "license": "MIT",
    "main": "./mustache.js",
    "maintainers": [
        {
            "name": "dasilvacontin",
            "email": "dasilvacontin@gmail.com"
        },
        {
            "name": "flipp",
            "email": "johphi@gmail.com"
        },
        {
            "name": "jan",
            "email": "jan@apache.org"
        },
        {
            "name": "mjackson",
            "email": "mjijackson@gmail.com"
        },
        {
            "name": "nathan",
            "email": "nrstott@gmail.com"
        }
    ],
    "name": "mustache",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/janl/mustache.js.git"
    },
    "scripts": {
        "pre-test-browser": "node test/create-browser-suite.js",
        "pretest": "eslint mustache.js bin/mustache",
        "test": "mocha --reporter spec test/*-test.js",
        "test-browser": "npm run pre-test-browser && zuul -- test/context-test.js test/parse-test.js test/scanner-test.js test/render-test-browser.js",
        "test-browser-local": "npm run pre-test-browser && zuul --local 8080 -- test/context-test.js test/scanner-test.js test/parse-test.js test/render-test-browser.js",
        "test-render": "mocha  --reporter spec test/render-test"
    },
    "spm": {
        "main": "mustache.js",
        "ignore": [
            "test",
            "wrappers"
        ]
    },
    "version": "2.3.0",
    "volo": {
        "url": "https://raw.github.com/janl/mustache.js/{version}/mustache.js"
    }
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module mustache](#apidoc.module.mustache)
1.  [function <span class="apidocSignatureSpan">mustache.</span>Context (view, parentContext)](#apidoc.element.mustache.Context)
1.  [function <span class="apidocSignatureSpan">mustache.</span>Scanner (string)](#apidoc.element.mustache.Scanner)
1.  [function <span class="apidocSignatureSpan">mustache.</span>Writer ()](#apidoc.element.mustache.Writer)
1.  [function <span class="apidocSignatureSpan">mustache.</span>clearCache ()](#apidoc.element.mustache.clearCache)
1.  [function <span class="apidocSignatureSpan">mustache.</span>escape (string)](#apidoc.element.mustache.escape)
1.  [function <span class="apidocSignatureSpan">mustache.</span>parse (template, tags)](#apidoc.element.mustache.parse)
1.  [function <span class="apidocSignatureSpan">mustache.</span>render (template, view, partials)](#apidoc.element.mustache.render)
1.  [function <span class="apidocSignatureSpan">mustache.</span>to_html (template, view, partials, send)](#apidoc.element.mustache.to_html)
1.  object <span class="apidocSignatureSpan">mustache.</span>Context.prototype
1.  object <span class="apidocSignatureSpan">mustache.</span>Scanner.prototype
1.  object <span class="apidocSignatureSpan">mustache.</span>Writer.prototype
1.  object <span class="apidocSignatureSpan">mustache.</span>tags
1.  string <span class="apidocSignatureSpan">mustache.</span>name
1.  string <span class="apidocSignatureSpan">mustache.</span>version

#### [module mustache.Context](#apidoc.module.mustache.Context)
1.  [function <span class="apidocSignatureSpan">mustache.</span>Context (view, parentContext)](#apidoc.element.mustache.Context.Context)

#### [module mustache.Context.prototype](#apidoc.module.mustache.Context.prototype)
1.  [function <span class="apidocSignatureSpan">mustache.Context.prototype.</span>lookup (name)](#apidoc.element.mustache.Context.prototype.lookup)
1.  [function <span class="apidocSignatureSpan">mustache.Context.prototype.</span>push (view)](#apidoc.element.mustache.Context.prototype.push)

#### [module mustache.Scanner](#apidoc.module.mustache.Scanner)
1.  [function <span class="apidocSignatureSpan">mustache.</span>Scanner (string)](#apidoc.element.mustache.Scanner.Scanner)

#### [module mustache.Scanner.prototype](#apidoc.module.mustache.Scanner.prototype)
1.  [function <span class="apidocSignatureSpan">mustache.Scanner.prototype.</span>eos ()](#apidoc.element.mustache.Scanner.prototype.eos)
1.  [function <span class="apidocSignatureSpan">mustache.Scanner.prototype.</span>scan (re)](#apidoc.element.mustache.Scanner.prototype.scan)
1.  [function <span class="apidocSignatureSpan">mustache.Scanner.prototype.</span>scanUntil (re)](#apidoc.element.mustache.Scanner.prototype.scanUntil)

#### [module mustache.Writer](#apidoc.module.mustache.Writer)
1.  [function <span class="apidocSignatureSpan">mustache.</span>Writer ()](#apidoc.element.mustache.Writer.Writer)

#### [module mustache.Writer.prototype](#apidoc.module.mustache.Writer.prototype)
1.  [function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>clearCache ()](#apidoc.element.mustache.Writer.prototype.clearCache)
1.  [function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>escapedValue (token, context)](#apidoc.element.mustache.Writer.prototype.escapedValue)
1.  [function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>parse (template, tags)](#apidoc.element.mustache.Writer.prototype.parse)
1.  [function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>rawValue (token)](#apidoc.element.mustache.Writer.prototype.rawValue)
1.  [function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>render (template, view, partials)](#apidoc.element.mustache.Writer.prototype.render)
1.  [function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>renderInverted (token, context, partials, originalTemplate)](#apidoc.element.mustache.Writer.prototype.renderInverted)
1.  [function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>renderPartial (token, context, partials)](#apidoc.element.mustache.Writer.prototype.renderPartial)
1.  [function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>renderSection (token, context, partials, originalTemplate)](#apidoc.element.mustache.Writer.prototype.renderSection)
1.  [function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>renderTokens (tokens, context, partials, originalTemplate)](#apidoc.element.mustache.Writer.prototype.renderTokens)
1.  [function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>unescapedValue (token, context)](#apidoc.element.mustache.Writer.prototype.unescapedValue)



# <a name="apidoc.module.mustache"></a>[module mustache](#apidoc.module.mustache)

#### <a name="apidoc.element.mustache.Context"></a>[function <span class="apidocSignatureSpan">mustache.</span>Context (view, parentContext)](#apidoc.element.mustache.Context)
- description and source-code
```javascript
function Context(view, parentContext) {
  this.view = view;
  this.cache = { '.': this.view };
  this.parent = parentContext;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.Scanner"></a>[function <span class="apidocSignatureSpan">mustache.</span>Scanner (string)](#apidoc.element.mustache.Scanner)
- description and source-code
```javascript
function Scanner(string) {
  this.string = string;
  this.tail = string;
  this.pos = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.Writer"></a>[function <span class="apidocSignatureSpan">mustache.</span>Writer ()](#apidoc.element.mustache.Writer)
- description and source-code
```javascript
function Writer() {
  this.cache = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.clearCache"></a>[function <span class="apidocSignatureSpan">mustache.</span>clearCache ()](#apidoc.element.mustache.clearCache)
- description and source-code
```javascript
function clearCache() {
  return defaultWriter.clearCache();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.escape"></a>[function <span class="apidocSignatureSpan">mustache.</span>escape (string)](#apidoc.element.mustache.escape)
- description and source-code
```javascript
function escapeHtml(string) {
  return String(string).replace(/[&<>"''=\/]/g, function fromEntityMap (s) {
    return entityMap[s];
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.parse"></a>[function <span class="apidocSignatureSpan">mustache.</span>parse (template, tags)](#apidoc.element.mustache.parse)
- description and source-code
```javascript
function parse(template, tags) {
  return defaultWriter.parse(template, tags);
}
```
- example usage
```shell
...
'''js
Mustache.render(
  template  : String,
  view      : Object,
  partials? : Object,
) => String

Mustache.parse(
  template              : String,
  tags = ['{{', '}}']   : Tags,
) => String

interface Tags [String, String]
'''
...
```

#### <a name="apidoc.element.mustache.render"></a>[function <span class="apidocSignatureSpan">mustache.</span>render (template, view, partials)](#apidoc.element.mustache.render)
- description and source-code
```javascript
function render(template, view, partials) {
  if (typeof template !== 'string') {
    throw new TypeError('Invalid template! Template should be a "string" ' +
                        'but "' + typeStr(template) + '" was given as the first ' +
                        'argument for mustache#render(template, view, partials)');
  }

  return defaultWriter.render(template, view, partials);
}
```
- example usage
```shell
...
var view = {
  title: "Joe",
  calc: function () {
    return 2 + 4;
  }
};

var output = Mustache.render("{{title}} spends {{calc}}", view);
'''

In this example, the 'Mustache.render' function takes two parameters: 1) the [mustache](http://mustache.github.com/) template and
 2) a 'view' object that contains the data and code needed to render the template.

## API

Following is an [rtype](https://git.io/rtype) signature of the most commonly used functions.
...
```

#### <a name="apidoc.element.mustache.to_html"></a>[function <span class="apidocSignatureSpan">mustache.</span>to_html (template, view, partials, send)](#apidoc.element.mustache.to_html)
- description and source-code
```javascript
function to_html(template, view, partials, send) {
<span class="apidocCodeCommentSpan">  /*eslint-enable*/
</span>
  var result = mustache.render(template, view, partials);

  if (isFunction(send)) {
    send(result);
  } else {
    return result;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mustache.Context"></a>[module mustache.Context](#apidoc.module.mustache.Context)

#### <a name="apidoc.element.mustache.Context.Context"></a>[function <span class="apidocSignatureSpan">mustache.</span>Context (view, parentContext)](#apidoc.element.mustache.Context.Context)
- description and source-code
```javascript
function Context(view, parentContext) {
  this.view = view;
  this.cache = { '.': this.view };
  this.parent = parentContext;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mustache.Context.prototype"></a>[module mustache.Context.prototype](#apidoc.module.mustache.Context.prototype)

#### <a name="apidoc.element.mustache.Context.prototype.lookup"></a>[function <span class="apidocSignatureSpan">mustache.Context.prototype.</span>lookup (name)](#apidoc.element.mustache.Context.prototype.lookup)
- description and source-code
```javascript
function lookup(name) {
  var cache = this.cache;

  var value;
  if (cache.hasOwnProperty(name)) {
    value = cache[name];
  } else {
    var context = this, names, index, lookupHit = false;

    while (context) {
      if (name.indexOf('.') > 0) {
        value = context.view;
        names = name.split('.');
        index = 0;

<span class="apidocCodeCommentSpan">        /**
         * Using the dot notion path in 'name', we descend through the
         * nested objects.
         *
         * To be certain that the lookup has been successful, we have to
         * check if the last object in the path actually has the property
         * we are looking for. We store the result in 'lookupHit'.
         *
         * This is specially necessary for when the value has been set to
         * 'undefined' and we want to avoid looking up parent contexts.
         **/
</span>        while (value != null && index < names.length) {
          if (index === names.length - 1)
            lookupHit = hasProperty(value, names[index]);

          value = value[names[index++]];
        }
      } else {
        value = context.view[name];
        lookupHit = hasProperty(context.view, name);
      }

      if (lookupHit)
        break;

      context = context.parent;
    }

    cache[name] = value;
  }

  if (isFunction(value))
    value = value.call(this.view);

  return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.Context.prototype.push"></a>[function <span class="apidocSignatureSpan">mustache.Context.prototype.</span>push (view)](#apidoc.element.mustache.Context.prototype.push)
- description and source-code
```javascript
function push(view) {
  return new Context(view, this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mustache.Scanner"></a>[module mustache.Scanner](#apidoc.module.mustache.Scanner)

#### <a name="apidoc.element.mustache.Scanner.Scanner"></a>[function <span class="apidocSignatureSpan">mustache.</span>Scanner (string)](#apidoc.element.mustache.Scanner.Scanner)
- description and source-code
```javascript
function Scanner(string) {
  this.string = string;
  this.tail = string;
  this.pos = 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mustache.Scanner.prototype"></a>[module mustache.Scanner.prototype](#apidoc.module.mustache.Scanner.prototype)

#### <a name="apidoc.element.mustache.Scanner.prototype.eos"></a>[function <span class="apidocSignatureSpan">mustache.Scanner.prototype.</span>eos ()](#apidoc.element.mustache.Scanner.prototype.eos)
- description and source-code
```javascript
function eos() {
  return this.tail === '';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.Scanner.prototype.scan"></a>[function <span class="apidocSignatureSpan">mustache.Scanner.prototype.</span>scan (re)](#apidoc.element.mustache.Scanner.prototype.scan)
- description and source-code
```javascript
function scan(re) {
  var match = this.tail.match(re);

  if (!match || match.index !== 0)
    return '';

  var string = match[0];

  this.tail = this.tail.substring(string.length);
  this.pos += string.length;

  return string;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.Scanner.prototype.scanUntil"></a>[function <span class="apidocSignatureSpan">mustache.Scanner.prototype.</span>scanUntil (re)](#apidoc.element.mustache.Scanner.prototype.scanUntil)
- description and source-code
```javascript
function scanUntil(re) {
  var index = this.tail.search(re), match;

  switch (index) {
    case -1:
      match = this.tail;
      this.tail = '';
      break;
    case 0:
      match = '';
      break;
    default:
      match = this.tail.substring(0, index);
      this.tail = this.tail.substring(index);
  }

  this.pos += match.length;

  return match;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mustache.Writer"></a>[module mustache.Writer](#apidoc.module.mustache.Writer)

#### <a name="apidoc.element.mustache.Writer.Writer"></a>[function <span class="apidocSignatureSpan">mustache.</span>Writer ()](#apidoc.element.mustache.Writer.Writer)
- description and source-code
```javascript
function Writer() {
  this.cache = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mustache.Writer.prototype"></a>[module mustache.Writer.prototype](#apidoc.module.mustache.Writer.prototype)

#### <a name="apidoc.element.mustache.Writer.prototype.clearCache"></a>[function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>clearCache ()](#apidoc.element.mustache.Writer.prototype.clearCache)
- description and source-code
```javascript
function clearCache() {
  this.cache = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.Writer.prototype.escapedValue"></a>[function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>escapedValue (token, context)](#apidoc.element.mustache.Writer.prototype.escapedValue)
- description and source-code
```javascript
function escapedValue(token, context) {
  var value = context.lookup(token[1]);
  if (value != null)
    return mustache.escape(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.Writer.prototype.parse"></a>[function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>parse (template, tags)](#apidoc.element.mustache.Writer.prototype.parse)
- description and source-code
```javascript
function parse(template, tags) {
  var cache = this.cache;
  var tokens = cache[template];

  if (tokens == null)
    tokens = cache[template] = parseTemplate(template, tags);

  return tokens;
}
```
- example usage
```shell
...
'''js
Mustache.render(
  template  : String,
  view      : Object,
  partials? : Object,
) => String

Mustache.parse(
  template              : String,
  tags = ['{{', '}}']   : Tags,
) => String

interface Tags [String, String]
'''
...
```

#### <a name="apidoc.element.mustache.Writer.prototype.rawValue"></a>[function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>rawValue (token)](#apidoc.element.mustache.Writer.prototype.rawValue)
- description and source-code
```javascript
function rawValue(token) {
  return token[1];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.Writer.prototype.render"></a>[function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>render (template, view, partials)](#apidoc.element.mustache.Writer.prototype.render)
- description and source-code
```javascript
function render(template, view, partials) {
  var tokens = this.parse(template);
  var context = (view instanceof Context) ? view : new Context(view);
  return this.renderTokens(tokens, context, partials, template);
}
```
- example usage
```shell
...
var view = {
  title: "Joe",
  calc: function () {
    return 2 + 4;
  }
};

var output = Mustache.render("{{title}} spends {{calc}}", view);
'''

In this example, the 'Mustache.render' function takes two parameters: 1) the [mustache](http://mustache.github.com/) template and
 2) a 'view' object that contains the data and code needed to render the template.

## API

Following is an [rtype](https://git.io/rtype) signature of the most commonly used functions.
...
```

#### <a name="apidoc.element.mustache.Writer.prototype.renderInverted"></a>[function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>renderInverted (token, context, partials, originalTemplate)](#apidoc.element.mustache.Writer.prototype.renderInverted)
- description and source-code
```javascript
function renderInverted(token, context, partials, originalTemplate) {
  var value = context.lookup(token[1]);

  // Use JavaScript's definition of falsy. Include empty arrays.
  // See https://github.com/janl/mustache.js/issues/186
  if (!value || (isArray(value) && value.length === 0))
    return this.renderTokens(token[4], context, partials, originalTemplate);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.Writer.prototype.renderPartial"></a>[function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>renderPartial (token, context, partials)](#apidoc.element.mustache.Writer.prototype.renderPartial)
- description and source-code
```javascript
function renderPartial(token, context, partials) {
  if (!partials) return;

  var value = isFunction(partials) ? partials(token[1]) : partials[token[1]];
  if (value != null)
    return this.renderTokens(this.parse(value), context, partials, value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.Writer.prototype.renderSection"></a>[function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>renderSection (token, context, partials, originalTemplate)](#apidoc.element.mustache.Writer.prototype.renderSection)
- description and source-code
```javascript
function renderSection(token, context, partials, originalTemplate) {
  var self = this;
  var buffer = '';
  var value = context.lookup(token[1]);

  // This function is used to render an arbitrary template
  // in the current context by higher-order sections.
  function subRender (template) {
    return self.render(template, context, partials);
  }

  if (!value) return;

  if (isArray(value)) {
    for (var j = 0, valueLength = value.length; j < valueLength; ++j) {
      buffer += this.renderTokens(token[4], context.push(value[j]), partials, originalTemplate);
    }
  } else if (typeof value === 'object' || typeof value === 'string' || typeof value === 'number') {
    buffer += this.renderTokens(token[4], context.push(value), partials, originalTemplate);
  } else if (isFunction(value)) {
    if (typeof originalTemplate !== 'string')
      throw new Error('Cannot use higher-order sections without the original template');

    // Extract the portion of the original template that the section contains.
    value = value.call(context.view, originalTemplate.slice(token[3], token[5]), subRender);

    if (value != null)
      buffer += value;
  } else {
    buffer += this.renderTokens(token[4], context, partials, originalTemplate);
  }
  return buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.Writer.prototype.renderTokens"></a>[function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>renderTokens (tokens, context, partials, originalTemplate)](#apidoc.element.mustache.Writer.prototype.renderTokens)
- description and source-code
```javascript
function renderTokens(tokens, context, partials, originalTemplate) {
  var buffer = '';

  var token, symbol, value;
  for (var i = 0, numTokens = tokens.length; i < numTokens; ++i) {
    value = undefined;
    token = tokens[i];
    symbol = token[0];

    if (symbol === '#') value = this.renderSection(token, context, partials, originalTemplate);
    else if (symbol === '^') value = this.renderInverted(token, context, partials, originalTemplate);
    else if (symbol === '>') value = this.renderPartial(token, context, partials, originalTemplate);
    else if (symbol === '&') value = this.unescapedValue(token, context);
    else if (symbol === 'name') value = this.escapedValue(token, context);
    else if (symbol === 'text') value = this.rawValue(token);

    if (value !== undefined)
      buffer += value;
  }

  return buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mustache.Writer.prototype.unescapedValue"></a>[function <span class="apidocSignatureSpan">mustache.Writer.prototype.</span>unescapedValue (token, context)](#apidoc.element.mustache.Writer.prototype.unescapedValue)
- description and source-code
```javascript
function unescapedValue(token, context) {
  var value = context.lookup(token[1]);
  if (value != null)
    return value;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
