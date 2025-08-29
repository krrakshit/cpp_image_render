cmake_minimum_required(VERSION 3.10)

# Set the project name
project(ImageGenerator)

# Set C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add the executable
add_executable(image_generator first.cc)

# Optional: Set compiler-specific options
if(MSVC)
    target_compile_options(image_generator PRIVATE /W4)
else()
    target_compile_options(image_generator PRIVATE -Wall -Wextra -Wpedantic)
endif()
