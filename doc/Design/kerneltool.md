# Design: kerneltool

## Goals
 - Provide unified tool for managing kernel configurations and artifacts.
 - Provide strong versioning checks to ensure all requested kernel artifacts and their dependencies exist and match the specified kernel.
 - Provide environment enabling repeatable custom builds of kernels and modules from source packages.
 - Provide ability to extract (and possibly build from source packages) kernel artifacts available with various distributions' packaging.
 - Provide ability to create hashed and signed manifests of all known artifacts for each kernel.
 - Provide ability to create archive(s) for or install a specified subset of artifacts in distinct target locations.
 - Provide ability to build kernel artifacts for multiple targets/configurations without conflict.
