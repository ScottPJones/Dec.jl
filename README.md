# Dec

[![Build Status](https://travis-ci.org/ScottPJones/Dec.jl.svg?branch=master)](https://travis-ci.org/ScottPJones/Dec.jl)

The Dec package is a work-in-progress, starting from a Julia wrapper around the
[decNumber C library](http://speleotrove.com/decimal/), which provides a software implementation of the packed decimal formats of the IEEE 754-2008 Decimal Floating-Point Arithmetic specification.

32-bit, 64-bit, and 128-bit decimal floating-point types `dec32`, `dec64`, and `dec128`, respectively, are provided.
I hope to also have the arbitrary precision support provided later,
once I have finished with the IEEE packed decimal formats.
Note: this is meant to also be used with @stevengj's excellent DecFP.jl package, which provides support for the 3 IEEE binary decimal formats.

The Dec package currently requires the Julia 0.4 release.

## Usage

`dec64` and the other types mentioned above can be constructed from strings by `parse(dec64, "123.45")` or `dec64"123.45"`, the same thing goes for `dec32` and `dec128`.

Currently, only a few of the simple functions are supported, any help fleshing this out would of course be appreciated, as well as comments on how to improve the Julia code.

I currently am figuring out how to use BinDeps, and have only been testing on 64-bit Mac OS X so far.
