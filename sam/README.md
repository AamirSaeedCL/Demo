# TypeaheadTesting

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 7.0.1.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).



{
  "env": {
    "browser": true,
    "es2021": true
  },
  "extends": ["eslint:recommended", "plugin:@typescript-eslint/recommended"],
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
    "ecmaVersion": 12,
    "sourceType": "module"
  },
  "plugins": ["@typescript-eslint"],
  "ignorePatterns": ["*.spec.ts", "*.js"],
  "rules": {
    // Handled by prettier
    "indent": "off",
    "linebreak-style": "off",
    "quotes": "off",
    "semi": "off",
    // Empty functions are not allowed, with the exception of empty
    // arrow functions. This is for easier implementation of
    // ControlValueAccessor
    "@typescript-eslint/no-empty-function": ["error", { "allow": ["arrowFunctions"] }],
    // Explicit return types for public methods are not required
    "@typescript-eslint/explicit-module-boundary-types": ["off"],
    // Unused vars are not allowed, with the exception of unused args
    // when prefixed with an underscore
    "@typescript-eslint/no-unused-vars": [
      "error",
      {
        "argsIgnorePattern": "^_",
        "args": "after-used",
        "ignoreRestSiblings": true
      }
    ],
    // https://github.com/typescript-eslint/typescript-eslint/blob/master/packages/eslint-plugin/docs/rules/naming-convention.md#enforce-that-interface-names-do-not-begin-with-an-i
    // As we have all the interface(s) started with I, so we are making it `match:true`
    "@typescript-eslint/naming-convention": [
      "error",
      {
        "selector": "interface",
        "format": ["PascalCase"],
        "custom": {
          "regex": "^I[A-Z]",
          "match": true
        }
      }
    ],
    "no-warning-comments": [
      "error",
      {
        "terms": ["todo", "fixme"],
        "location": "anywhere"
      }
    ],
    // Console log, info and trace are not allowed
    // Warn and error should only be used for exceptions
    "no-console": [
      "error",
      {
        "allow": ["warn", "error"]
      }
    ],
    "no-mixed-spaces-and-tabs": ["warn", "smart-tabs"]
  }
}
