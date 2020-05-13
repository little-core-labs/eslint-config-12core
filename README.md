# eslint-config-12core
![Node.js CI](https://github.com/little-core-labs/eslint-config-12core/workflows/Node.js%20CI/badge.svg)

A shareable [eslint](ghub.io/eslint) config for 12core projects.

## Usage

```console
npm i @12core/eslint-config-12core eslint --save-dev
```

Then create an `.eslintrc.json` file in the root of your directory:

```json
{
  "extends": "@12core/eslint-config-12core"
}
```

Then run eslint on whatever code you want to lint:

```console
eslint --ext .js esm/
```

Make the linting step part of your testing script.

## What

`@12core/eslint-config-12core` bundles standard + standard-jsx with additional consutomizations that work for all of us at little-core-labs.

Because we control the shareable config, the normally peer-dependent eslint plugins are actually included as transient dependencies, so that usage of this config is a lot more convenient (only 2 deps, instead if 5+).

## Contributing

If you would like to make rule changes, please submit a PR with some discussion with rational.

## Editor plugins

You should use an editor plugin so that you can see the warnings while working, and take advantage of auto formatting:

### VSCode

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

### Sublime

- [SublimeLinter](https://github.com/SublimeLinter/SublimeLinter)
- [SublimeLinter-eslint](https://github.com/SublimeLinter/SublimeLinter-eslint)
- [StandardFormat](https://github.com/bcomnes/sublime-standard-format) (can be customized to run eslint --fix)

### Your favorite editor

... please PR notes you have!

## React

If you want to use the standard react plugin, follow these steps:

### Install deps

```console
npm i @12core/eslint-config-12core eslint babel-eslint eslint-config-standard-react --save-dev
```

### Create eslint config

Create a `.eslintrc.json` with the following.

```json
{
  "parser": "babel-eslint",
  "extends": ["@12core/eslint-config-12core", "standard-react"]
}
```

### Run eslint

```console
eslint --ext .js esm/
```
