# DiffEq Developer Documentation

This is the developer documentation for the DiffEq ecosystem. It explains the common
interface and some the package internals to help developers contribute.

If you have any questions, or just want to chat about solvers/using the package, please feel free to use the [Gitter channel](https://gitter.im/JuliaDiffEq/Lobby). For bug reports, feature requests, etc., please submit an issue. If you're interested in contributing, please see the [Contributor's Guide](http://juliadiffeq.github.io/DifferentialEquations.jl/latest/internals/contributors_guide.html).

## Overview

The DiffEq ecosystem is built around the common interface. The common interface
is a type-based interface where users define problems as a type, and solvers
plug into the ecosystem by defining an algorithm to give a new dispatch to

```julia
solve(prob,alg;kwargs...)
```

There is then an ecosystem of add-on components which use the common solver interface
to add analysis tools for differential equations.

## Bleeding Edge

This package suite is still under heavy development. If you are a power user
and would like to try out the latest features, it is recommended you use the
MetaDiffEq metapackage. To do so, use the following commands:

```julia
Pkg.clone("https://github.com/tbreloff/MetaPkg.jl") # Install MetaPkg
using MetaPkg
meta_add("MetaDiffEq") # Adds all of the packages, even those unregistered
meta_checkout("MetaDiffEq") # Checks out the master branch on all of the packages
```

Note that this is for power users who are familiar with Julia. If you are having
issues, please contact Chris Rackauckas in  [the Gitter channel.](https://gitter.im/JuliaDiffEq/Lobby)

## Other Help

Even if you don't have the time to contribute new solver algorithms, there's always
ways to help! Improved plot recipes and new series recipes are
always nice to add more default plots. It is always helpful to have benchmarks
between different algorithms to see "which is best". Adding examples IJulia
notebooks to DiffEqTutorials.jl is a good way to share knowledge about DifferentialEquations.jl.
Also, please feel free to comb through the solvers and look for ways to make them
more efficient. Lastly, the documentation could always use improvements. If you
have any questions on how to help, just ask them in the Gitter!

## Contributor Guide

```@contents
Pages = [
  "contributing/contributors_guide.md",
  "contributing/adding_algorithms.md",
  "contributing/defining_problems.md",
]
Depth = 2
```

## Internal Documentation

```@contents
Pages = [
  "internals/fem_tools.md",
  "internals/extras.md",
  "internals/solver_helpers.md",
  "internals/notes_on_algorithms.md",
  "internals/tableaus.md"
]
Depth = 2
```