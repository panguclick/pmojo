#
# Copyright 2022 The pmojo Authors.
#
cmake_minimum_required(VERSION 3.10)

project(pmojo LANGUAGES CXX)

# Output directory is correct by default for most build setups. However, when
# building Abseil as a DLL, it is important to have the DLL in the same
# directory as the executable using it. Thus, we put all executables in a single
# /bin directory.
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(CMAKE_CXX_STANDARD 17)
set(ABSL_BUILD_TESTING OFF)
set(ABSL_USE_GOOGLETEST_HEAD OFF)

add_subdirectory(base)

