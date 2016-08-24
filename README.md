# New Relic - React integration plugin

The package is based on [new-relic-react](https://github.com/reggi/new-relic-react) package by [reggi](https://github.com/reggi/).
This one includes a recent version of New Relic Browser plugin to inject [JavaScript snippet](https://docs.newrelic.com/docs/browser/new-relic-browser/page-load-timing/instrumentation-page-load-timing) to instrument your app's webpages.

It includes also [rollup.js](http://rollupjs.org/) to bundle source code as React component.

<br>
# Getting Started

`new-relic-react` can be installed as any other npm package.

<br>
# Installation

`npm install @wanderio/new-relic-react --save`

<br>
# Application Structure
```
.
├── src                     # Source files
│   ├── .babelrc            # Babel transpiler configuration
│   ├── index.js            # New Relic - React component source code
├── rollup.config.js        # Rollup.js configuration file to bundle module
├── package.json            # Package information with list of dependencies
├── LICENSE.md
└── README.md
```

<br>
# Usage

Just import `NewRelic` into your component

Retrieve this information from your New Relic account
- licenseKey: New Relic account license key
- applicationID: Current New Relic application ID

```<NewRelic licenseKey="{licenseKey}" applicationID="{applicationID}" />```  
where licenseKey and applicationID are real IDs you retrieved

<br>
Following code is a super simple example of integration
```
import React from 'react'
import NewRelic from 'new-relic-react'

const Html = () => {
  return (
    <html>
      <head>
        <meta charSet="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <meta httpEquiv="x-ua-compatible" content="ie=edge" />
        <NewRelic licenseKey="xxxx" applicationID="yyyy" />
        <title>Web App</title>
      </head>
      <body>
        <div id="app">
          {children}
        </div>
      </body>
    </html>
  )
}

export default Html
```

<br>
# Changelog

1.0.1 - Published scoped package on npm registry with additional rollup.js bundler and updated New Relic script

<br>
# License

Copyright (c) 2016 Wanderio

MIT (http://opensource.org/licenses/mit-license.php)

-----

based on https://github.com/reggi/new-relic-react
