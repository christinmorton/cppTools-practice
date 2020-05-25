cmake_minimum_required(VERSION 3.17.2)

project(jturnerctools)

if (MSVC)
  add_compile_options(/W4)
else()
  add_compile_options(-Wall -Wextra -Wpendantic)
endif()

add_executable(intro main.cpp)
target_compile_features(intro PRIVATE cxx_lambda_init_captures)