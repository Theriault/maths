# Maths

[![Go Reference](https://pkg.go.dev/badge/github.com/theriault/maths.svg)](https://pkg.go.dev/github.com/theriault/maths)
[![Go](https://github.com/Theriault/maths/actions/workflows/go.yml/badge.svg)](https://github.com/Theriault/maths/actions/workflows/go.yml)
[![Go Report Card](https://goreportcard.com/badge/github.com/theriault/maths)](https://goreportcard.com/report/github.com/theriault/maths)

maths includes mathematical functions not defined in the standard Go math package.

## Installation

```sh
go get github.com/theriault/maths 
```

## What's Included

### Combinatorics

```go
import "github.com/theriault/maths/combinatorics"
```

```go
// Factorial: n!
combinatorics.Factorial(10) // will return uint64(3628800)

// Falling factorial + partial permutations
combinatorics.FallingFactorial(8, 3) // will return uint64(336)
combinatorics.PartialPermutations(8, 3) // will return uint64(336)

// Primorial
combinatorics.Primorial(30) // will return uint64(6469693230)

// Rising factorial
combinatorics.RisingFactorial(2, 3) // will return uint64(24)
```

### Number Theory

```go
import "github.com/theriault/maths/numbertheory"
```

```go
// Aliquot sum
numbertheory.AliquotSum(60) // will return uint64(108)

// Möbius function
numbertheory.Mobius(70) // will return int8(-1)

// Number of divisors
numbertheory.NumberOfDivisors(48) // will return uint64(10)

// Politeness
numbertheory.Politeness(32) // will return uint64(0)

// Polygonal numbers
numbertheory.PolygonalNumber(3, 4) // will return uint64(10)
numbertheory.PolygonalRoot(3, 10) // will return float64(4)
numbertheory.PolygonalSides(4, 10) // will return float64(3)

// Prime factorize any uint64
numbertheory.PrimeFactorization(184756) // will return []uint64{2, 2, 11, 13, 17, 19}

// Radical
numbertheory.Radical(60) // will return uint64(30)

// Sum of divisors
numbertheory.SumOfDivisors(48) // will return uint64(10)

// Euler's totient
numbertheory.Totient(68) // will return uint64(32)

// Jordan's totient
numbertheory.TotientK(60, 2) // will return uint64(2304)
```

### Statistics

```go
import "github.com/theriault/maths/statistics"
```

```go
// Means
statistics.Mean(1, 1000) // will return float64(500.5)
statistics.GeometricMean(1, 1000) // will return float64(31.62...)
statistics.HarmonicMean(1, 1000) // will return float64(1.99...)
```