# Changelog

## [0.7.1] — 2021-08-26

 - Added: Support for building with clang-cl (LLVM-based toolchain for Visual Studio 2019).
   [#179](https://github.com/chfast/ethash/pull/179)
   [#180](https://github.com/chfast/ethash/pull/180)
   [#182](https://github.com/chfast/ethash/pull/182)
   [#183](https://github.com/chfast/ethash/pull/183)
   [#184](https://github.com/chfast/ethash/pull/184)

## [0.7.0] — 2021-05-26

 - Changed: The global context API (aka "managed" API) has been moved to
   separate library `ethash::global-context` and `ethash/global_context.hpp`
   header.
   [#175](https://github.com/chfast/ethash/pull/175)
 - Added: CMake options to disable building of individual libraries:
   - `-DETHASH_BUILD_GLOBAL_CONTEXT=NO` disables building
     `ethash::global-context`.
   - `-DETHASH_BUILD_ETHASH=NO` disables building `ethash::ethash` and
     `ethash::global-context`. Only `ethash::keccak` is built then.
 - Added: Basic support for building to WebAssembly
   [#175](https://github.com/chfast/ethash/pull/175)
   
## [0.6.0] — 2020-12-15

 - Added: The ethash::keccak library received the optimized Keccak implementation
   which uses BMI and BMI2 x86_64 extensions. This implementation is automatically
   selected at startup provided the used extensions are available in the hardware.
   [#162](https://github.com/chfast/ethash/pull/162)
   [#168](https://github.com/chfast/ethash/pull/168)

## [0.5.2] — 2020-08-03

 - Fixed: Fix compilation with MSVC/C++17.
   [#154](https://github.com/chfast/ethash/issues/154)

## [0.5.1] — 2020-01-30

 - Added: Experimental Python bindings — [ethash][pypi-ethash] package.
   [#123](https://github.com/chfast/ethash/pull/123)
   [#138](https://github.com/chfast/ethash/pull/138)
 - Added: More functions exposed in C API.
   [#136](https://github.com/chfast/ethash/pull/136)
 - Changed: ProgPoW implementation updated to revision [0.9.3][ProgPoW-changelog].
   [#151](https://github.com/chfast/ethash/pull/151)

## [0.5.0] — 2019-06-07

 - Changed:
   The Keccak implementation has been moved to separate library "keccak", 
   available as ethash::keccak target in the ethash CMake package.
   [#131](https://github.com/chfast/ethash/pull/131)

## [0.4.4] — 2019-02-26

 - Fixed:
   Fix compilation on PowerPC architectures (-mtune=generic not supported there).
   [#125](https://github.com/chfast/ethash/pull/125)

## [0.4.3] — 2019-02-19

 - Added:
   The public `version.h` header with information about the ethash library version.
   [#121](https://github.com/chfast/ethash/pull/121)
 - Added:
   Ethash and ProgPoW revisions exposed as `{ethash,progpow}::revision` constants.
   [#121](https://github.com/chfast/ethash/pull/121)

## [0.4.2] — 2019-01-24

 - Fixed: The `progpow.cpp` file encoding changed from utf-8 to ascii.

## [0.4.1] — 2018-12-14

 - Added: [KISS99 PRNG](https://en.wikipedia.org/wiki/KISS_(algorithm) distribution tester tool.
 - Changed: ProgPoW implementation updated to revision [0.9.2][ProgPoW-changelog].
 - Changed: ProgPoW implementation optimizations.

## [0.4.0] — 2018-12-04

 - Added: Experimental support for [ProgPoW] [0.9.1][ProgPoW-changelog].


[0.7.1]: https://github.com/chfast/ethash/releases/tag/v0.7.1
[0.7.0]: https://github.com/chfast/ethash/releases/tag/v0.7.0
[0.6.0]: https://github.com/chfast/ethash/releases/tag/v0.6.0
[0.5.2]: https://github.com/chfast/ethash/releases/tag/v0.5.2
[0.5.1]: https://github.com/chfast/ethash/releases/tag/v0.5.1
[0.5.0]: https://github.com/chfast/ethash/releases/tag/v0.5.0
[0.4.4]: https://github.com/chfast/ethash/releases/tag/v0.4.4
[0.4.3]: https://github.com/chfast/ethash/releases/tag/v0.4.3
[0.4.2]: https://github.com/chfast/ethash/releases/tag/v0.4.2
[0.4.1]: https://github.com/chfast/ethash/releases/tag/v0.4.1
[0.4.0]: https://github.com/chfast/ethash/releases/tag/v0.4.0

[ProgPoW]: https://github.com/ifdefelse/ProgPOW/blob/master/README.md
[ProgPoW-changelog]: https://github.com/ifdefelse/ProgPOW#change-history
[pypi-ethash]: https://pypi.org/project/ethash/
