# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Unreleased

## [0.3.0] - 2021-09-10

### Added

- `ExpandedDisplay` a different view of data structures. It eases viewing structures with a lot a fields. Proposed by [@sd2k](https://github.com/sd2k)
- `MaxWidth::wrapping` a wrapping mechanism. Setting it will make text wrap to next line after reaching limit.

### Changed

- `MaxWidth` interface changed in regard to support `wrapping`. Now old `MaxWidth` logic can be called by `MaxWidth::trucating`.

### Fixed

- Fix an issue that setting `Alignment` was changing `Indent` settings.

## [0.2.3] - 2021-09-06

### Added

- `Rotate` option for grid to rotate grid over 90 degrees.
- `FormatWithIndex` modifier for cells
- `FormatFrom` modifier for cells

### Changed

- Refactoring in `tabled_derive`

### Fixed

- Improve documentation by [@CGMossa](https://github.com/CGMossa)

## [0.2.2] - 2021-07-14

### Added

- Add `Header/Footer` option for grid. 
- Add path (`::`) support in `display_with` attribute.
- Add `Tabled` implementation for constant arrays. 
- Add blank implementation of `TableOption` for `&TableOption` 

## [0.2.1] - 2021-06-23

### Added

- Add `MaxWidth` option for cells
- Add `#[header(inline)]` attribute to inline internal data structures which implement `Tabled` trait
- Add blank `Tabled` implementaton for String
- Add `#[header(inline)]` example

### Changed

- Use `ansi-cut` instead of `console` to truncate string
- Switch to `github CI` instead of `travis.ci` because free credit limit was reached

### Fixed

- A sublte refactoring in `tabled_derive`

## [0.2.0] - 2021-06-19

### Added

- Add `Table` type instead of `table!` macros
- Consider lambdas Fn(&str) -> String as format options
- Add basic usage example

### Changed

- Removed `table!` macros.

### Fixed

- Improved performance in papergrid; Now it makes 100 allocs on basic example where priviously 400!

## [0.1.4] - 2021-06-07

### Added

- Add a vertical indent support in `Alignment` setting
- Add `Indent` setting for a grid
- Add a support for an attribute `#[field(display_with = "function_name")]` for custom display of a struct fields

### Changed

- `Alignment` interface

### Fixed

- Spelling and grammara mistakes #10 in README.md. Reported by [@atcol](https://github.com/atcol) 
- Panic on emojies #9. Reported by [@nicoulaj](https://github.com/nicoulaj) 

## [0.1.3] - 2021-06-05

### Added

- Add a `Disable` setting for removing rows/column out of the grid
- `Object` combination via `and()`, `not()` methods for targeting more thoroughly
- Modification of default `Style`s
- Add `#[header(hidden)]` attribute to hide variants and fields
