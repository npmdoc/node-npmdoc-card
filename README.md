# npmdoc-card

#### api documentation for  card (v2.2.1)  [![npm package](https://img.shields.io/npm/v/npmdoc-card.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-card) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-card.svg)](https://travis-ci.org/npmdoc/node-npmdoc-card)

#### Card lets you add an interactive, CSS3 credit card animation to your credit card form to help your users through the process.

[![NPM](https://nodei.co/npm/card.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/card)

- [https://npmdoc.github.io/node-npmdoc-card/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-card/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-card/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-card/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-card/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-card/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "card",
    "version": "2.2.1",
    "author": "Jesse Pollak <jpollak92@gmail.com>",
    "description": "Card lets you add an interactive, CSS3 credit card animation to your credit card form to help your users through the process.",
    "main": "lib/card.js",
    "repository": {
        "type": "git",
        "url": "https://github.com/jessepollak/card"
    },
    "contributors": [
        {
            "name": "Jesse Pollak"
        },
        {
            "name": "Daniel Juhl"
        }
    ],
    "scripts": {
        "clean": "rimraf ./lib/ && rimraf ./dist/",
        "compile": "npm run clean && npm run compile:lib && npm run compile:dist",
        "compile:lib": "coffee --compile -o ./lib/ ./src/coffee/card.coffee && node-sass ./src/scss/card.scss -o lib/ && replace '../scss/card.scss' './card.css' lib/card.js",
        "compile:dist": "npm run env NODE_ENV=production && webpack",
        "development": "webpack-dev-server --hot --inline",
        "preversion": "npm run compile",
        "prepublish": "npm run env NODE_ENV=production && npm run compile",
        "postpublish": "git push origin master && git push --tags",
        "test": "karma start --single-run --browsers PhantomJS"
    },
    "devDependencies": {
        "bower": "~1.7.9",
        "coffee-loader": "^0.7.2",
        "coffee-script": "~1.10.0",
        "css-loader": "^0.23.1",
        "event-stream": "^3.3.1",
        "glob": "^7.0.5",
        "jquery": "~3.0.0",
        "node-sass": "^3.8.0",
        "nodemon": "~1.9.2",
        "replace": "^0.3.0",
        "rimraf": "^2.5.4",
        "run-sequence": "~1.2.1",
        "sass-loader": "^3.2.2",
        "style-loader": "^0.13.1",
        "underscore": "^1.8.3",
        "vinyl-source-stream": "^1.1.0",
        "webpack": "^1.13.1",
        "webpack-dev-server": "^1.14.1"
    },
    "dependencies": {
        "node.extend": "~1.1.3",
        "qj": "^2.0.0",
        "payment": "^2.2.1"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
