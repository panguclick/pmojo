cmake_minimum_required(VERSION 3.13.0)

cmake_policy(SET CMP0079 NEW)
cmake_policy(SET CMP0048 NEW)

set(pmojo_target_name pmojo)
project(${pmojo_target_name})

add_subdirectory(third_path/abseil-cpp)
add_subdirectory(base)
