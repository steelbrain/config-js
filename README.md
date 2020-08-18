Config-JS
========

This package is a batteries-included JS configuration for ESLint and Prettier.
`config-js` depends on ESLint and Prettier and their configuration-specific
dependencies so you only have to install this package and by the magic of
flat-dependencies, they are available for use in your project.

## Installation

```
npm install --save-dev @steelbrain/config-js
# OR
yarn add --dev @steelbrain/config-js
```

For ESLint, create a configuration file `.eslintrc.json` and paste the following in it

```json
{
  "extends": "@steelbrain/config-js/eslint"
}
```

For Prettier, add the following to `.prettierrc.js` in your package root

```js
module.exports = require('@steelbrain/config-js/prettier')
```

and that's it. Enjoy!

## Installation Notes

This package has the necessary plugins, including to the **ESLint and Prettier CLIs** themselves.
So you should remove/not install them in your project, the flat dependency installation
will make sure the ESLint CLI from this package is accessible to `npm run` etc.

### License

This project is licensed under the terms of MIT License. See the LICENSE file for more info.
