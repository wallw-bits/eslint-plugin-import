# Change Log
All notable changes to this resolver will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).
This change log adheres to standards from [Keep a CHANGELOG](http://keepachangelog.com).

## Unreleased

## 0.13.1 - 2021-05-13

### Added
- add support for webpack5 'externals function' ([#2023], thanks [@jet2jet])

### Changed
- Add warning about async Webpack configs ([#1962], thanks [@ogonkov])
- Replace `node-libs-browser` with `is-core-module` ([#1967], thanks [@andersk])
- [meta] add "engines" field to document existing requirements
- [Refactor] use `is-regex` instead of `instanceof RegExp`
- [Refactor] use `Array.isArray` instead of `instanceof Array`
- [deps] update `debug`, `interpret`, `is-core-module`, `lodash`, `resolve`

## 0.13.0 - 2020-09-27

### Breaking
- [Breaking] Allow to resolve config path relative to working directory (#1276)

## 0.12.2 - 2020-06-16

### Fixed
- [fix] provide config fallback ([#1705], thanks [@migueloller])

## 0.12.1 - 2020-01-10

### Changed
- [meta] copy LICENSE file to all npm packages on prepublish ([#1595], thanks [@opichals])

## 0.12.0 - 2019-12-07

### Added
- [New] enable passing cwd as an option to `eslint-import-resolver-webpack` ([#1503], thanks [@Aghassi])

## 0.11.1 - 2019-04-13

### Fixed
- [fix] match coreLibs after resolveSync in webpack-resolver ([#1297], thanks [@echenley])

## 0.11.0 - 2018-01-22

### Added
- support for `argv` parameter when config is a function. ([#1261], thanks [@keann])

### Fixed
- crash when webpack config is an array of functions ([#1219]/[#1220] by [@idudinov])

## 0.10.1 - 2018-06-24
### Fixed
- log a useful error in a module bug arises ([#768]/[#767], thanks [@mattkrick])

## 0.10.0 - 2018-05-17
### Changed
- cache webpack resolve function, for performance ([#788]/[#1091])

## 0.9.0 - 2018-03-29
### Breaking
- Fix with `pnpm` by bumping `resolve` ([#968])

## 0.8.4 - 2018-01-05
### Changed
- allow newer version of node-libs-browser ([#969])

## 0.8.3 - 2017-06-23
### Changed
- `debug` bumped to match others

## 0.8.2 - 2017-06-22
### Changed
- `webpack` peer dep updated to >= 1.11 (works fine with webpack 3 AFAICT)

## 0.8.1 - 2017-01-19
### Changed
- official support for Webpack 2.2.0 (RC), thanks [@graingert]

## 0.8.0 - 2016-12-15
### Changed
- bumped `resolve` to fix issues with Node builtins (thanks [@SkeLLLa] and [@ljharb])
- allow `enhanced-resolve` to be version `>= 2` (thanks [@Kovensky])

## 0.7.1
### Fixed
- missing `has` dependency ([#681] + [#683], thanks [@benmvp] + [@ljharb])

## 0.7.0
### Added
- Support for explicit Webpack config object in `.eslintrc.*`. ([#572], thanks [@jameslnewell])
- Added `resolve.modules` to configs for webpack2 support ([#569], thanks [@toshafed])

## 0.6.0 - 2016-09-13
### Added
- support for config-as-function ([#533], thanks [@grahamb])

## 0.5.1 - 2016-08-11
### Fixed
- don't throw and die if no webpack config is found

## 0.5.0 - 2016-08-11
### Added
- support for Webpack 2 + `module` package.json key! ([#475], thanks [@taion])

### Changed
- don't swallow errors, assume config exists ([#435], thanks [@Kovensky])

## 0.4.0 - 2016-07-17
### Added
- support for `webpack.ResolverPlugin` ([#377], thanks [@Rogeres])

### Fixed
- provide string `context` to `externals` functions ([#411] + [#413], thanks [@Satyam])

## 0.3.2 - 2016-06-30
### Added
- shared config ([config.js](./config.js)) with barebones settings needed to use this resolver. ([#283])

### Fixed
- strip resource query ([#357], thanks [@daltones])
- allow `externals` to be defined as a function ([#363], thanks [@kesne])

## 0.3.1 - 2016-06-02
### Added
- debug logging. run with `DEBUG=eslint-plugin-import:*` to see log output.

## 0.3.0 - 2016-06-01
### Changed
- use `enhanced-resolve` to support additional plugins instead of re-implementing
  aliases, etc.

## 0.2.5 - 2016-05-23
### Added
- Added support for multiple webpack configs ([#181], thanks [@GreenGremlin])

## 0.2.4 - 2016-04-29
### Changed
- automatically find webpack config with `interpret`-able extensions ([#287], thanks [@taion])

## 0.2.3 - 2016-04-28
### Fixed
- `interpret` dependency was declared in the wrong `package.json`.
   Thanks [@jonboiser] for sleuthing ([#286]) and fixing ([#289]).

## 0.2.2 - 2016-04-27
### Added
- `interpret` configs (such as `.babel.js`).
  Thanks to [@gausie] for the initial PR ([#164], ages ago! 😅) and [@jquense] for tests ([#278]).

[#2023]: https://github.com/import-js/eslint-plugin-import/pull/2023
[#1967]: https://github.com/import-js/eslint-plugin-import/pull/1967
[#1962]: https://github.com/import-js/eslint-plugin-import/pull/1962
[#1705]: https://github.com/import-js/eslint-plugin-import/pull/1705
[#1595]: https://github.com/import-js/eslint-plugin-import/pull/1595
[#1503]: https://github.com/import-js/eslint-plugin-import/pull/1503
[#1297]: https://github.com/import-js/eslint-plugin-import/pull/1297
[#1261]: https://github.com/import-js/eslint-plugin-import/pull/1261
[#1220]: https://github.com/import-js/eslint-plugin-import/pull/1220
[#1091]: https://github.com/import-js/eslint-plugin-import/pull/1091
[#969]: https://github.com/import-js/eslint-plugin-import/pull/969
[#968]: https://github.com/import-js/eslint-plugin-import/pull/968
[#768]: https://github.com/import-js/eslint-plugin-import/pull/768
[#683]: https://github.com/import-js/eslint-plugin-import/pull/683
[#572]: https://github.com/import-js/eslint-plugin-import/pull/572
[#569]: https://github.com/import-js/eslint-plugin-import/pull/569
[#533]: https://github.com/import-js/eslint-plugin-import/pull/533
[#413]: https://github.com/import-js/eslint-plugin-import/pull/413
[#377]: https://github.com/import-js/eslint-plugin-import/pull/377
[#363]: https://github.com/import-js/eslint-plugin-import/pull/363
[#289]: https://github.com/import-js/eslint-plugin-import/pull/289
[#287]: https://github.com/import-js/eslint-plugin-import/pull/287
[#278]: https://github.com/import-js/eslint-plugin-import/pull/278
[#181]: https://github.com/import-js/eslint-plugin-import/pull/181
[#164]: https://github.com/import-js/eslint-plugin-import/pull/164

[#1219]: https://github.com/import-js/eslint-plugin-import/issues/1219
[#788]: https://github.com/import-js/eslint-plugin-import/issues/788
[#767]: https://github.com/import-js/eslint-plugin-import/issues/767
[#681]: https://github.com/import-js/eslint-plugin-import/issues/681
[#435]: https://github.com/import-js/eslint-plugin-import/issues/435
[#411]: https://github.com/import-js/eslint-plugin-import/issues/411
[#357]: https://github.com/import-js/eslint-plugin-import/issues/357
[#286]: https://github.com/import-js/eslint-plugin-import/issues/286
[#283]: https://github.com/import-js/eslint-plugin-import/issues/283

[@gausie]: https://github.com/gausie
[@jquense]: https://github.com/jquense
[@taion]: https://github.com/taion
[@GreenGremlin]: https://github.com/GreenGremlin
[@daltones]: https://github.com/daltones
[@kesne]: https://github.com/kesne
[@Satyam]: https://github.com/Satyam
[@Rogeres]: https://github.com/Rogeres
[@Kovensky]: https://github.com/Kovensky
[@grahamb]: https://github.com/grahamb
[@jameslnewell]: https://github.com/jameslnewell
[@toshafed]: https://github.com/toshafed
[@benmvp]: https://github.com/benmvp
[@ljharb]: https://github.com/ljharb
[@SkeLLLa]: https://github.com/SkeLLLa
[@graingert]: https://github.com/graingert
[@mattkrick]: https://github.com/mattkrick
[@idudinov]: https://github.com/idudinov
[@keann]: https://github.com/keann
[@echenley]: https://github.com/echenley
[@Aghassi]: https://github.com/Aghassi
[@migueloller]: https://github.com/migueloller
[@opichals]: https://github.com/opichals
[@andersk]: https://github.com/andersk
[@ogonkov]: https://github.com/ogonkov
[@jet2jet]: https://github.com/jet2jet