project(trezor-crypto)
cmake_minimum_required(VERSION 3.20)

add_library(trezor-crypto)
target_compile_options(trezor-crypto PRIVATE -Wall -Wextra)
set_target_properties(trezor-crypto PROPERTIES C_STANDARD 11)

# target_include_directories(sample PUBLIC include)
add_subdirectory(src)

file(CONFIGURE OUTPUT .gitignore
  NEWLINE_STYLE UNIX
  CONTENT "*")
