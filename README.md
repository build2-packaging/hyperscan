# hyperscan

`build2` package assimilation of the [~intel/hyperscan]( https://www.hyperscan.io ) library.

## CAVEATS

- `libhs/hs/config.h` is included pre-generated. it could be your system doesn't match.
    - `avx2` is required as well as a 64bit target.
- `libhs/hs/parser/Parser.cpp` is included pre-generated from the actual `ragel` spec ( `Parser.rl` ).
    - this is to avoid the build-time dependency of `ragel`
- `hs_version.h` used for tagging compiled databases is generated using `build2` provided `version.h`
    - you can only open databases compiled with a matching version.

