# BenchmarkProfiles

A simple [Julia](http://julialang.org) package to plot performance and data profiles.

| **Documentation** | **Linux/macOS/Windows/FreeBSD** | **Coverage** |
|:-----------------:|:----------------------------------------------:|:------------:|
| [![](https://img.shields.io/badge/docs-dev-blue.svg)](https://JuliaSmoothOptimizers.github.io/BenchmarkProfiles.jl/dev) | ![CI](https://github.com/JuliaSmoothOptimizers/NLPModels.jl/workflows/CI/badge.svg?branch=master) [![Build Status](https://img.shields.io/cirrus/github/JuliaSmoothOptimizers/BenchmarkProfiles.jl?logo=Cirrus%20CI)](https://cirrus-ci.com/github/JuliaSmoothOptimizers/BenchmarkProfiles.jl) | [![codecov](https://codecov.io/gh/JuliaSmoothOptimizers/BenchmarkProfiles.jl/branch/master/graph/badge.svg?token=39PVYBcETt)](https://codecov.io/gh/JuliaSmoothOptimizers/BenchmarkProfiles.jl) |

This package contains Julia translations of original scripts by Elizabeth Dolan, Jorge Moré and Stefan Wild.
See http://www.mcs.anl.gov/~wild/dfo/benchmarking.

The original code was not accompanied by an open-source license. Jorge Moré and Stefan Wild have kindly provided their consent in writing to allow distribution of this Julia translation.
See the `consent` folder for a full transcription.

Watch out for the [pitfalls](http://dl.acm.org/citation.cfm?id=2950048) of profiles!

## How to Install

```julia
julia> Pkg.add("BenchmarkProfiles")
```

Plotting is handled by [`Plots.jl`](https://docs.juliaplots.org/latest/) so the user can choose among several available plotting backends.

## Example

```julia
julia> using BenchmarkProfiles
julia> T = 10 * rand(25,3);  # 25 problems, 3 solvers
julia> performance_profile(T, ["Solver 1", "Solver 2", "Solver 3"], title="Celebrity Deathmatch")
```

![Performance Profile](./img/random_profile.png)

## References

E. Dolan and J. Moré, *Benchmarking Optimization Software with Performance Profiles*, Mathematical Programming 91, pages 201--213, 2002. DOI [10.1007/s101070100263](http://dx.doi.org/10.1007/s101070100263).

J. J. Moré and S. M. Wild, *Benchmarking Derivative-Free Optimization Algorithms*, SIAM Journal on Optimization, 20(1), pages 172--191, 2009. DOI [10.1137/080724083](http://dx.doi.org/10.1137/080724083).
