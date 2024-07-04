# async-rayon

_Mix async code with CPU-heavy thread pools using [Futures][futures-url] + [Rayon][rayon-url]_

[futures-url]: https://docs.rs/futures
[rayon-url]: https://docs.rs/rayon

[![Documentation][docs-badge]][docs-url]
[![Build status][build-badge]][build-url]
[![Test coverage][coverage-badge]][coverage-url]
<br />
[![crates.io][crates-badge]][crates-url]
[![Downloads][downloads-badge]][crates-url]
[![Rust version][rust-version-badge]][rust-version-link]
<br />
[![MIT license][license-badge]][license-url]

[build-badge]: https://img.shields.io/github/workflow/status/ArvinSKushwaha/async-rayon/CI?labelColor=112&logo=github&logoColor=fff&style=flat-square
[build-url]: https://github.com/ArvinSKushwaha/async-rayon/actions
[coverage-badge]: https://img.shields.io/codecov/c/gh/ArvinSKushwaha/async-rayon?labelColor=112&logo=codecov&logoColor=fff&style=flat-square
[coverage-url]: https://codecov.io/gh/ArvinSKushwaha/async-rayon
[crates-badge]: https://img.shields.io/crates/v/async-rayon?labelColor=112&logo=rust&logoColor=fff&style=flat-square
[crates-url]: https://crates.io/crates/async-rayon
[docs-badge]: https://img.shields.io/docsrs/async-rayon?labelColor=112&logo=read-the-docs&logoColor=fff&style=flat-square
[docs-url]: https://docs.rs/async-rayon
[downloads-badge]: https://img.shields.io/crates/d/async-rayon?labelColor=112&color=informational&style=flat-square
[license-badge]: https://img.shields.io/crates/l/async-rayon?labelColor=112&style=flat-square
[license-url]: https://github.com/ArvinSKushwaha/async-rayon/blob/main/LICENSE.txt
[rust-version-badge]: https://img.shields.io/badge/rustc-1.45+-informational?logo=rust&logoColor=fff&labelColor=112&style=flat-square
[rust-version-link]: https://www.rust-lang.org

## Resources

- [**Documentation**][docs-url]
- [crates.io][crates-url]

## TL;DR

Sometimes, you're doing async stuff, and you also need to do CPU-heavy
stuff. This library will help!

```rust
let nft = async_rayon::spawn_async(|| {
  do_some_crypto_stuff()
}).await?;

assert_eq!(nft, ExpensiveNft);
```
