# The following lines of boilerplate have to be in your project's
# CMakeLists in this exact order for cmake to work correctly
cmake_minimum_required(VERSION 3.5)

if(NOT DEFINED ENV{IDF_PATH})
    message(FATAL_ERROR "IDF_PATH environment variable is not set")
endif()

# Asegúrate de usar la toolchain correcta para ESP32-C3
set(CMAKE_TOOLCHAIN_FILE $ENV{IDF_PATH}/tools/cmake/toolchain-esp32c3.cmake)

include($ENV{IDF_PATH}/tools/cmake/project.cmake)

project(hello_world)

