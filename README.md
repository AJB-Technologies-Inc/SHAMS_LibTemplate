# SHAMS Library Template 📃
This repository serves as a template to create future SHAMS libs from. It has most of the base configurations set up to get a new CMake library up and going to be used as part of the SHAMS ecosystem.

## Features
- CMake already set up.
- Devcontainer config ready to use for C++ development and CMake, including installing needed tools, such as GTest.
- Github actions setup to build and run tests using CMake.
- VS Code configs setup to run project.

## How to Use
- Use github GUI or CLI to make a new repo and select this repository as a template.
- Update the root CMakeLists.txt file to change the project name, and any additional changes as needed by the lib.
- The default folder for all of the private source and headers is in the root `source` folder, this can be changed, but the root CMakeLists.txt file will need to be updated.
- The `cmake` folder container common cmake utils and also retreives external libraries that are needed by this lib. The `install_libs.cmake` file is where additional libs should be fetched.
- If using Platform.IO:
  - Modify the values in `library.json` to suite the new library.
