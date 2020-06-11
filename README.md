# eslint-config-auto

This config will automatically configure the *airbnb* esLint rules and a range of other plugins, based on the contents of your projects `package.json` file.

## Install

To install this config, run the following command.

```sh
yarn add eslint-config-auto --dev
```

## Configure

Create an `.eslintrc` file with the following contents.

```json
{
  "extends": ["eslint-config-auto"]
}
```

You can now include `html`, `json` and `markdown` in the list of files passed to `eslint` to lint any JavaScript contained.

```json
{
  "scripts": {
    "eslint": "eslint --color *.{html,js,json,jsx,md,ts,tsx} src/*.{html,js,json,jsx,md,ts,tsx}",
    "eslint:fix": "npm run eslint -- --fix"
  }
}
```

## Install Dependencies

After you have configured `eslint` to include this package, the first time you run `eslint` it will output the `npm` command to install the dependencies required for your project. Cut'n'paste this command into the console, and you are then ready to start linting.

## Rules

### AirBNB

The most appropreate version of the AirBNB eslint config will be automatically selected

### Adjunct

The [eslint-config-adjunct](https://github.com/davidjbradshaw/eslint-config-adjunct#plugins) config is included, this will install a range of plugins based on your project's dependancies.

### TypeScript

If you project includes TypeScript, then the rules will adapt to lint typescipt files.