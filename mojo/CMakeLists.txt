
set(MOJO_TARGET_NAME “mojo”)

# Compiler id for Apple Clang is now AppleClang.
if (POLICY CMP0025)
    cmake_policy(SET CMP0025 NEW)
endif (POLICY CMP0025)

# if command can use IN_LIST
if (POLICY CMP0057)
    cmake_policy(SET CMP0057 NEW)
endif (POLICY CMP0057)

# Project version variables are the empty string if version is unspecified
if (POLICY CMP0048)
    cmake_policy(SET CMP0048 NEW)
endif (POLICY CMP0048)

# option() honor variables
if (POLICY CMP0077)
    cmake_policy(SET CMP0077 NEW)
endif (POLICY CMP0077)

# Allow the user to specify the MSVC runtime
if (POLICY CMP0091)
    cmake_policy(SET CMP0091 NEW)
endif (POLICY CMP0091)

# try_compile() honors the CMAKE_CXX_STANDARD value
if (POLICY CMP0067)
    cmake_policy(SET CMP0067 NEW)
endif (POLICY CMP0067)

project(MOJO_TARGET_NAME LANGUAGES CXX)

add_subdirectory(public)

# add_library(
#     ${MOJO_TARGET_NAME}
#     ${MOJO_BUILD_CONFIGURATION_TYPE}
#     ${sources}
# )

target_link_libraries(${MOJO_TARGET_NAME}
    ${MOJO_LINK_LIBRARIES}
    ${MOJO_LINK_PLATFORM_LIBRARIES}
)