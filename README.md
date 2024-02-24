# Aseprite Windows Automated Build and Release GitHub Action

[![Aseprite Windows Automated Build and Release](https://github.com/CardoPixel/aseprite_builder_reborn/actions/workflows/aseprite_builder_reborn_deploy.yml/badge.svg)](https://github.com/CardoPixel/aseprite_builder_reborn/actions/workflows/aseprite_builder_reborn_deploy.yml)

![GitHub License](https://img.shields.io/github/license/CardoPixel/aseprite_builder_reborn)

![GitHub Downloads (all assets, all releases)](https://img.shields.io/github/downloads/CardoPixel/aseprite_builder_reborn/total)

![GitHub repo size](https://img.shields.io/github/repo-size/CardoPixel/aseprite_builder_reborn)

This GitHub Action automates the process of building and releasing Aseprite for Windows. It checks out the Aseprite source code, sets up the required build environment, compiles the code, and creates a release with the compiled executable.

## Workflow Overview

The workflow is triggered manually through `workflow_dispatch`, allowing for execution at any time. It performs the following steps:

1. **Checkout Repository**: Clones the Aseprite source code with all submodules.
2. **Setup MSVC Environment**: Configures the Microsoft Visual Studio C++ environment.
3. **Install Visual Studio Components**: Installs the necessary Windows 10 SDK for building Aseprite.
4. **Setup Ninja Build System**: Installs Ninja to streamline the build process.
5. **Install CMake**: Installs CMake, required for the build configuration.
6. **Download and Setup Skia**: Downloads and sets up Skia, a core dependency for Aseprite.
7. **Compile Aseprite**: Compiles Aseprite from the source code.
8. **Upload Aseprite Artifact**: Uploads the compiled Aseprite executable as an artifact.
9. **Create Release**: Automatically creates a GitHub release and uploads the Aseprite executable.

## Usage

To use this GitHub Action in your project, create a `.github/workflows/aseprite-windows-build.yml` file in your repository and paste the content of this workflow into that file.

## Prerequisites

- A GitHub repository with Aseprite source code.
- Access to GitHub Actions in your GitHub repository.

## Inputs

This workflow does not require any inputs, as it is triggered manually via `workflow_dispatch`.

## Outputs

- **Aseprite Executable**: The compiled Aseprite executable for Windows will be available as an artifact and attached to the created GitHub release.

## Customization

You can fork this workflow and modify it as needed for your project, including changing the version of the Windows SDK or adding additional steps required for your build process.

## License

The scripts and documentation in this project are released under the MIT License.
