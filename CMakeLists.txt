project(trezor)
cmake_minimum_required(VERSION 3.20)

add_library(trezor)
target_compile_options(trezor PRIVATE -Wall -Wextra)
set_target_properties(trezor PROPERTIES C_STANDARD 11)

# target_include_directories(sample PUBLIC include)
add_subdirectory(trezor-firmware)

file(CONFIGURE OUTPUT .gitignore
  NEWLINE_STYLE UNIX
  CONTENT "*")
