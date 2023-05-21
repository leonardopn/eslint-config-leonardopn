# eslint-config-leonardopn

This is a ESLint config for my personal projects based on [eslint-config-rocketseat
](https://github.com/Rocketseat/eslint-config-rocketseat)

## Whats included?

- Standard config base;
- React plugin(Changed by me);
- React Hooks plugin;
- JSX a11y plugin;
- Prettier(changed by me);

## Setup

1. Install the dependencies

```bash
npm i -D eslint eslint-config-leonardopn
```

2. Create a `.eslintrc.json` file extending the config:

```json
{
  "extends": "eslint-config-leonardopn/react"
}
```

> You can also use a `.eslintrc.js` instead of JSON if you prefer.

if you use VsCode prettier formatter

3. (Optional) Create a `.prettierrc.js` file extending the config:

```js
const prettier = require("eslint-config-leonardopn/prettier");

module.exports = prettier;
```

> You can override the default prettier file, but update also the file .eslintrc.js for prevent incompatibility between rules Eslint.

Example:

```js
//.prettierrc.js
const prettier = require("eslint-config-leonardopn/prettier");

module.exports = {
  ...prettier,
  semi: false,
};
```

```js
//.eslintrc.js
module.exports = {
  extends: ["eslint-config-leonardopn/react"],
  rules: {
   "prettier/prettier": ["error", { semi: false }],
  },
};
```

## License

This ESlint config is licensed by MIT License - [LICENSE](LICENSE.md) for more details.
