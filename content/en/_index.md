---
title: "go-bignum documentation"
linkTitle: "Home"
type: docs
cascade:
  type: docs
description: "Arbitrary precision in pure Go (CGO=0): correctly rounded elementary functions and constants on math/big.Float, and the oracle harness that checks them."
---

**go-bignum is arbitrary precision in pure Go.** Its library, `bigfloat`,
provides correctly rounded elementary functions and constants on Go's
`math/big.Float`, at any precision and in all six rounding modes, with no cgo
and no dependencies. Its tests replay golden fixtures certified with
[mpmath](https://mpmath.org) at high precision.

`bigfloat` is **released v0.1.0**: every function is at or below mpmath's time
on one core, and the results stay correctly rounded.

## The libraries

| Library | Status | What it does |
| --- | --- | --- |
| [bigfloat]({{< relref "bigfloat" >}}) | released v0.1.0 | roots, exponentials and logarithms, trigonometric and hyperbolic functions, `Pow` and the constants π, e, ln 2, ln 10 and γ, correctly rounded; the `oracle` package drives mpmath from Go and stores golden fixtures |

## Install

```sh
go get github.com/go-bignum/bigfloat@v0.1.0
```

The module is pure Go (`CGO_ENABLED=0`) and its `go.mod` says Go 1.27.1.

## What each library's pages hold

| Library | Pages |
| --- | --- |
| bigfloat | [overview]({{< relref "bigfloat" >}}) |
