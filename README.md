# FEModels.jl

[![Build Status](https://travis-ci.org/JuliaFEM/FEModels.jl.svg?branch=master)](https://travis-ci.org/JuliaFEM/FEModels.jl)[![Coverage Status](https://coveralls.io/repos/github/JuliaFEM/FEModels.jl/badge.svg?branch=master)](https://coveralls.io/github/JuliaFEM/FEModels.jl?branch=master)[![](https://img.shields.io/badge/docs-stable-blue.svg)](https://juliafem.github.io/FEModels.jl/stable)[![](https://img.shields.io/badge/docs-latest-blue.svg)](https://juliafem.github.io/FEModels.jl/latest)[![Issues](https://img.shields.io/github/issues/JuliaFEM/FEModels.jl.svg)](https://github.com/JuliaFEM/FEModels.jl/issues)

FEModels.jl is a simple interface to make it easy to fetch finite element meshes
and models from `JuliaFEM/FEModels` repository.

## Installing and testing package

```julia
Pkg.add("FEModels")
```

## Usage example

Give model name (directory name in repository) and mesh name (without .gz):

```julia
fn = fe_download("block-and-cylinder", "mesh_sparse.inp")
```

Then you should have extracted model in `block-and-cylinder/mesh_sparse.inp`.
`fn` is filename to mesh file which can then be read e.g. using `AbaqusReader.jl`:

```julia
using AbaqusReader
mesh = abaqus_read_mesh(fn)
```

## Contibuting

Contributors are needed. Todo:

* list all models in repository
* possibility to upload models or automate upload process somehow
