# build-artifacts-archive

## Repository Overview

This repository is used for archiving and backing up personal build artifacts, including various compiled products for multiple systems such as Linux, Windows, and HarmonyOS. It facilitates subsequent reuse and avoids redundant compilations.

The repository content is for personal use only, including binary files, library files, and application packages.

## Repository Structure

A naming convention of "artifact name - system - instruction set - bit width - version" is adopted, combined with a lightweight directory structure:

```plaintext
build-artifacts-archive/
├─ README.md          # This documentation file
├─ OpenSSL/           # Directory categorized by artifact name
│  ├─ v1.1.1/         # Version subdirectory
│  │  ├─ openssl-linux-x86_64-64bit.tar.gz
│  │  └─ openssl-win-x86_64-64bit.zip
│  └─ v3.2.0/
│     ├─ openssl-linux-x86_64-64bit.tar.gz
│     ├─ openssl-linux-arm64-64bit.tar.gz
│     └─ openssl-ohos-arm64-64bit-phone.hap
├─ Utils-Lib/
│  └─ ...
└─ App-Core/
   └─ ...
```

## File Naming Convention

The unified naming format is: `[artifact name]-[system identifier]-[instruction set]-[bit width]-[version number].[extension]`

## System Identifiers

* Linux: linux

* Windows: win

* HarmonyOS: ohos (HarmonyOS requires additional device type annotation)

## Common Instruction Sets

* x86_64: 64-bit x86 architecture

* x86: 32-bit x86 architecture

* arm64: 64-bit ARM architecture

* riscv64: 64-bit RISC-V architecture

## Bit Width Identifiers
* 64bit: 64-bit

* 32bit: 32-bit

## Example Filenames

|Filename|Description|
|--|--|
|openssl-linux-x86_64-64bit-v3.2.0.tar.gz	|Linux system, x86_64 instruction set, 64-bit, OpenSSL v3.2.0 version|
|utils-lib-win-x86-32bit-v2.0.0.lib	|Windows system, x86 instruction set, 32-bit, Utils-Lib v2.0.0 version|
|app-core-ohos-arm64-64bit-phone-v1.5.0.hap	|HarmonyOS system, arm64 instruction set, 64-bit, phone device, App-Core v1.5.0 version|
|driver-ohos-x86_64-64bit-sim-v2.0.0.so	|HarmonyOS system, x86_64 instruction set, 64-bit, simulator, driver v2.0.0 version|


## Artifact Information Description

Each compressed package or artifact directory contains an info.txt file recording the following key information:

* Compilation time

* Compiler and version (e.g., gcc 12.2, VS2022, DevEco Studio 4.0)

* Dependent libraries and versions
* Compilation parameters (key configurations)

## Version Management

* Version numbers follow semantic versioning: major.minor.patch (e.g., v1.0.0)

* Different versions of the same artifact are distinguished by version subdirectories

* Important updates will be recorded in the "Changelog" section of this README

## Changelog

## Copyright Information

The content of this repository is for personal archiving. When using the content of this repository, please retain the original project copyright information. Detailed terms can be found in the LICENSE file in the repository root directory.

## Notes

This repository is for personal archiving only

Some artifacts may depend on specific system environments. Please refer to the corresponding info.txt before use