# Overview of subTerra System Tools

## Security
 - **Utilize Web-of-Trust type semantics.**
 - **Hash and sign all artifacts at the lowest appropriate layer.**
 - **Hash and sign known combinations of artifacts.**
 - **Optionally require all artifacts to be countersigned by specific trusted keys.**
 - **Allow creation of immutable deployment environments where appropriate.**
 - **Minimize complexity of auditing.**
 - **Provide for complete logging.**


## Testing Framework

### Goals
 - **Provide regression testing between existing and new versions at each tier in the system.**
 - **Provide explicit testing for presence of known/previously-fixed issues across all tiers of the system.**
 - **Build and package all debug symbols for use in finding API/ABI changes as well as deeper debugging tasks.**
 - **Sign tested combinations of specific builds of packages and their full dependency trees.**


## Bootstrap Environment

### Goals
 - **One bootstrap environment per target environment (of which a single host may have more than one).**
 - **Provide minimal functional build environment needed to build propper packages for the specified target environment.**
 - **Create repeatable builds for each target environment.**
 - **Specifically intended to be used in the creation of repeatable builds of packages for each target environment.**
 - **Audit exact combinations of tools for bootstrap target environment and only sign the bootstrap configuration after it passess all testing.**


## Package Building

### Goals
 - **Use modular build architecture allowing use of various sources for build scripts.**
 - **All builds are handled as cross-builds in sterile environment defined by their build dep chain only**
 - **Make builds repeatable wherever possible - non-repeatable builds will require explicit whitelisting to be fully packaged.**
 - **Allow subsets of a package to be isolated and installed independently where applicable.


## Package Management

### Goals
 - **Provide minimal, robust dependency resolution algorithms.**
 - **Utilize filesystem and archive xattr support wherever practical to maintain file-local metadata for each managed file.**
 - **Provide a unified caching database interface to expected filesystem state.**
 - **Allow for the installation of multiple instances and/or versions of the same package in different locations of the same host.**
 

## Configuration Management

### Goals
 - **Allow admin and/or users to select which set of packages provides the active environment, on either a system-wide, user, or process tree level.**


## Image Building

### Goals

 - **Allow creation of individualized fully configured images for direct deployment.**
 - **Allow multiple images to coexist in the bootloader, optionally utilizing the same configuration and/or data.**
 - **Allow creation of bare-metal or VM raw disk images.**


