# drafter.js Changelog

## 3.0.0-pre.2

This update now uses Drafter 4.0.0-pre.2. Please see [Drafter
4.0.0-pre.2](https://github.com/apiaryio/drafter/releases/tag/v4.0.0-pre.2) for
the list of changes.

### Breaking

- `parse` won't return `err` if we get a parse result with error annotations
- `parse`'s `options` is now optional following node.js convention
- `validate`'s `options` is now optional following node.js convention

## 3.0.0-pre.1

This update now uses Drafter 4.0.0-pre.1. Please see [Drafter
4.0.0-pre.1](https://github.com/apiaryio/drafter/releases/tag/v4.0.0-pre.1) for
the list of changes.

- Build done using emscripten 1.38.x

### Breaking

- `parse` returns parse result in both `err` and `result` of the callback function
- `parseSync` doesn't throw error anymore if we get a parse result with error annotations

## 3.0.0-pre.0

This update now uses Drafter 4.0.0-pre.0. Please see [Drafter
4.0.0-pre.0](https://github.com/apiaryio/drafter/releases/tag/v4.0.0-pre.0) for
the list of changes.

- Build done using emscripten 1.37.x

### Breaking

- Drop support node < 4.0
- Remove the option to select AST Type. The ouput will be only refract

## 2.6.7

This update now uses Drafter 3.2.7. Please see [Drafter
3.2.7]https://github.com/apiaryio/drafter/releases/tag/v3.2.7) for
the list of changes.

## 2.6.6

### Bug Fixes

This update now uses Drafter 3.2.6. Please see [Drafter
3.2.6](https://github.com/apiaryio/drafter/releases/tag/v3.2.6) for
the list of changes.

## 2.6.5

### Bug Fixes

This update now uses Drafter 3.2.5. Please see [Drafter
3.2.5](https://github.com/apiaryio/drafter/releases/tag/v3.2.5) for
the list of changes.

## 2.6.4

### Bug Fixes

- Drafter.js will no longer override `Module` allowing drafter.js users to
  [override the emscripten execution
  environment](https://kripken.github.io/emscripten-site/docs/api_reference/module.html#overriding-execution-environment).


## 2.6.3

This update now uses Drafter 3.2.3. Please see [Drafter
3.2.3](https://github.com/apiaryio/drafter/releases/tag/v3.2.3) for
the list of changes.

## 2.6.2

This update now uses Drafter 3.2.2. Please see [Drafter
3.2.2](https://github.com/apiaryio/drafter/releases/tag/v3.2.2) for
the list of changes.

The package now includes Typescript ts file.

## 2.6.1

This update now uses Drafter 3.2.1. Please see [Drafter
3.2.1](https://github.com/apiaryio/drafter/releases/tag/v3.2.1) for
the list of changes.

## 2.6.0

### Enhancements

- Added `validate` and `validateSync` to just return the warnings and errors
  after parsing a blueprint.

## 2.5.2

This update now uses Drafter 3.1.3. Please see [Drafter
3.1.3](https://github.com/apiaryio/drafter/releases/tag/v3.1.3) for
the list of changes.

## 2.5.1

This update now uses Drafter 3.1.2. Please see [Drafter
3.1.2](https://github.com/apiaryio/drafter/releases/tag/v3.1.2) for
the list of changes.

## 2.5.0

This update now uses Drafter 3.1.1. Please see [Drafter
3.1.1](https://github.com/apiaryio/drafter/releases/tag/v3.1.1) for
the list of changes.

## 2.5.0-pre.0

This update now uses Drafter 3.1.0-pre.0. Please see [Drafter
3.1.0-pre.0](https://github.com/apiaryio/drafter/releases/tag/v3.1.0-pre.0) for
the list of changes.

## 2.4.3

### Bug Fixes

- Fixes an `undefined` exception thrown when the API Bleuprint
  contained Unicode characters due to a missing function 'UTF8ToString'.
  [issue #54](https://github.com/apiaryio/drafter.js/issues/54)


## 2.4.2

### Bug Fixes

- This release ensures that the .gyp and .gypi files are not detected during
  building the NPM package. NPM incorrectly computes the `gypfile` without
  respecting the `.npmignore` file.
  [npm/read-package-json#52](https://github.com/npm/read-package-json/pull/52)


## 2.4.1

### Bug Fixes

- Removes unnecessary files from the NPM package. 2.4.0 included the C++ source
  for Drafter and this causes problems while trying to install the package via
  NPM since it will try and use node-gyp to build the source.


## 2.4.0

### Enhancements

- Substantial performance improvements, parsing blueprints is now much faster.
- drafter.js now follows [Universal Module Definition (UMD)](https://github.com/umdjs/umd).
