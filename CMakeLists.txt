cmake_minimum_required(VERSION 3.21)

project(DirectXMath
    LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_library(DirectXMath INTERFACE)

target_include_directories(
    DirectXMath INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/Inc/ ${CMAKE_CURRENT_SOURCE_DIR}/Extensions/ ${CMAKE_CURRENT_SOURCE_DIR}/MatrixStack/ ${CMAKE_CURRENT_SOURCE_DIR}/XDSP/
)

add_library(razer::DxMath ALIAS DirectXMath)
