# Roadmap

This document states what our next goal is, and which objectives we have to
accomplish to consider the goal as "done". This document should evolve as we
make progress.

## Current goal

**Goal**: cross-compiling to `nvptx` from the Tier-1 `x86_64` targets should
always work. This moves `nvptx` from a Tier-3 to a Tier-2 target.

## Objectives

**Main objective**: create an example host crate that links to a device crate
containing a simple kernel using some `core::arch::nvptx` intrinsics and math
function. Launch the kernel from the host crate using `cuda-sys`. 

Compiling these crates from the `x86_64` Tier-1 targets should never fail. That
is, PRs to `rustc`, `libcore` (`stdsimd`, etc.) that would break the build for
this example crate should not be merge-able - that is, the CI systems of
`rustc`, `stdsimd`, etc. will detect this and fail.

Our current goal is only about making sure that cross-compiling always works.
That is, ensuring that the host crate actually runs correctly and passes a
run-time tests, e.g., with the kernel running on a real GPU, is not necessary to
achieve our goal and is not part of the objective - it could be our next goal.

This main objective is split into 4 sub-objectives:

**compiler**: we need to make sure that the compiler is always able to compile
`nvptx` kernels without erroring. We should add tests for this, and enable those
in Rust's CI. This would be codegen tests, compile-pass tests, etc. No run-time
tests at this point.

**library**: we need to make sure that the `nvptx` intrinsics (e.g.
`syncthreads`) always compile. We need to add tests to `stdsimd` to build these
intrinsics. 

**linker**: we need to make sure that linking `nvptx` to the host crate always
work, we need to test this, and we need to make sure that rustc changes are
blocked on not breaking this.

**testing**: our first focus is on getting the toolchain to an "always builds"
state. However, "always builds" is not very useful if nothing works at run-time.
We should implement ways of testing that the `ptx` code generated is correct,
without doing run-time tests.
