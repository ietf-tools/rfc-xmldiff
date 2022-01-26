# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.6.1] - 2019-12-05

### Changed

- Fix two text differance bugs

## [0.5.19] - 2019-08-29

### Changed

- Change source repository

## [0.5.18] - 2019-08-17

### Changed

- Fix error building paragraphs with 'li'
- Fix error in JavaScript
- Correct problem with writing unicode on Python 2.7

### Removed

- Remove Python 3.4 from the supported list

## [0.5.15] - 2019-05-31

### Changed

- Change the parameterization on the text difference code to use shorter unmatched strings.
- Alter how namespaces are displayed so they are not everywhere.

## [0.5.14] - 2019-04-21

### Added

- Add 2.7 dependency for enumerations

### Changed

- Change the text matching code to use longer sequences when possible

## [0.5.13] - 2019-04-06

### Changed

- Clean up so that pyflakes is happy

## [0.5.12] - 2019-02-22

### Added

- Add a class to deal with entities when they are not expanded.
- Load files from the cache if possible

### Removed

- Remove --template-url option as the templates are now self-contained

## [0.5.11] - 2019-01-01

### Added

- Add code to deal with trees which are going to merge but they	subtrees are going to overlap
- Add -D option to surpress filling in default attributes from DTD

### Changed

- Name spaces are now using a nsX namespace rather than using the {ns}field format.
- Change the html template to make sure that it is all within the screen.

## [0.5.10] - 2018-09-01

### Added

- Add a wdiff.html template which mimics the wdiff marking
- Add the --no-xinclude option. This option will additionally not process <?rfc include=""?> as well.

### Changed

- Make base.html be the default template
- Deal with getting UTF8 characters in source files - python 2 doesn't like it
- Clean out some unused items in the manifest file

## [0.5.9.1] - 2018-08-27

### Added

- Add missing file to distribution

## [0.5.9] - 2018-08-06

### Changed

- Make the HTML file be self contained
- Change the pane re-size algorithm.

### Added

- Add space after differences for readability

### Removed

- Complete work to remove JQuery from the html file

## [0.5.8.1] - 2018-07-18

### Changed

- Switch to a word by word diff computation for display

## [0.5.8] - 2018-07-11

### Changed

- Change the underlying difference algorithm used to word based
- Point to network server for all resources

## [0.5.7] - 2018-07-02

### Added

- Add options dealing w/ no network and no entity resolution

## [0.5.6] - 2018-06-22

### Changed

- Make things look prettier
- Fix top of page sync bug

## [0.5.5] - 2018-06-11

### Changed

- Update readme file

## [0.5.4.1] - 2018-05-10

### Changed

- Correct path to the build files for C code

## [0.5.4] - 2018-05-09

### Changed

- Respect whitespace in comments
- Make everything be a fixed pitch font based on RPC request
- Put in code to cause the right and left panels scroll based on the center scrolling

## [0.5.3] - 2018-04-25

### Added

- Add missing items from the manifest to make the html work correctly.

### Changed

- Move resize javascript into a separate file
- Move debuging output to being a note so it is not always emitted
- Fix the fact that half of the command line options are missing

## [0.5.1] - 2018-02-28

### Added

- Switch to a new tree paradigm as the old one did not allow needed cut and paste features.
- Implement a button to just open modified nodes

### Changed

- Tag artwork and sourcecode correctly so that they are formatted as space preserving.
- Emit the xml declaration and DOCTYPE declaration
- Setup to have and be able to select from multiple HTML templates.

## [0.5.0] - 2018-02-25

### Changed

- Many different css changes applied.  Changes include: resize the different columns, add background coloration, wrap lines and make the tree leafs of variable height, change the charset to allow Utf-8 characters. Long term should point to the column change code, but currently I don't know of a good place.
- Format paragraphs as a single node in the tree rather than spreading them out over the tree structure. This improves readability substantially.
- Force the matching of some v2 and v3 elements which provide equivalent functionality, but have different names.
- Include comments as nodes in the displayed tree.
- Fix some errors in the tree merging code so that elements are placed in the correct location.
- Need to separate the left/right class tagging from the li element as it gets clobbered by the tree code. Thus the addition of span elements all over the place.
- Clean up some memory leaks in the distance algorithm.

## [0.0.3] - 2018-02-11

### Added

- First drop of code - only does pure xml differences

- [0.6.1]: https://github.com/ietf-tools/rfclint/compare/0.5.19...0.6.1
- [0.5.19]: https://github.com/ietf-tools/rfclint/compare/0.5.18...0.5.19
- [0.5.18]: https://github.com/ietf-tools/rfclint/compare/0.5.15...0.5.18
- [0.5.15]: https://github.com/ietf-tools/rfclint/compare/0.5.14...0.5.15
- [0.5.14]: https://github.com/ietf-tools/rfclint/compare/0.5.13...0.5.14
- [0.5.13]: https://github.com/ietf-tools/rfclint/compare/0.5.12...0.5.13
- [0.5.12]: https://github.com/ietf-tools/rfclint/compare/0.5.11...0.5.12
- [0.5.11]: https://github.com/ietf-tools/rfclint/compare/0.5.10...0.5.11
- [0.5.10]: https://github.com/ietf-tools/rfclint/compare/0.5.9.1...0.5.10
- [0.5.9.1]: https://github.com/ietf-tools/rfclint/compare/0.5.9...0.5.9.1
- [0.5.9]: https://github.com/ietf-tools/rfclint/compare/0.5.8.1...0.5.9
- [0.5.8.1]: https://github.com/ietf-tools/rfclint/compare/0.5.8...0.5.8.1
- [0.5.8]: https://github.com/ietf-tools/rfclint/compare/0.5.7...0.5.8
- [0.5.7]: https://github.com/ietf-tools/rfclint/compare/0.5.6...0.5.7
- [0.5.6]: https://github.com/ietf-tools/rfclint/compare/0.5.5...0.5.6
- [0.5.5]: https://github.com/ietf-tools/rfclint/compare/0.5.4.1...0.5.5
- [0.5.4.1]: https://github.com/ietf-tools/rfclint/compare/0.5.4...0.5.4.1
- [0.5.4]: https://github.com/ietf-tools/rfclint/compare/0.5.3...0.5.4
- [0.5.3]: https://github.com/ietf-tools/rfclint/compare/0.5.1...0.5.3
- [0.5.1]: https://github.com/ietf-tools/rfclint/compare/0.5.0...0.5.1
- [0.5.0]: https://github.com/ietf-tools/rfclint/compare/0.0.3...0.5.0
- [0.0.3]: https://github.com/ietf-tools/rfclint/releases/tag/0.0.3
