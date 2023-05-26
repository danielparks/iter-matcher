# Change log

All notable changes to this project will be documented in this file.

## main branch

### Breaking changes

* Renamed `TreeMatcher::set_input_type()` to `TreeMatcher::input_type()`.

### Changes

* Made sure generated functions pass [Clippy]’s [pedantic lint group]:
  * Changed to add [`#[must_use]`] to generated functions by default.
  * Added trivial documentation about what errors are returned by a few
    functions.
  * Disabled [`clippy::single_match_else`] lint within generated match
    functions, since we sometimes generate `match` statements with a single arm.
  * Disabled [`clippy::too_many_lines`] lint within generated match
    functions, since such functions can be extremely long.

[Clippy]: https://doc.rust-lang.org/stable/clippy/index.html
[pedantic lint group]: https://doc.rust-lang.org/stable/clippy/usage.html#clippypedantic
[`#[must_use]`]: https://doc.rust-lang.org/reference/attributes/diagnostics.html#the-must_use-attribute
[`clippy::single_match_else`]: https://rust-lang.github.io/rust-clippy/master/index.html#single_match_else
[`clippy::too_many_lines`]: https://rust-lang.github.io/rust-clippy/master/index.html#too_many_lines

## Release 0.1.0 (2023-02-27)

### Features

* Initial release.
