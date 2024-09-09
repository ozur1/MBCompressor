cmake_minimum_required(VERSION 3.24.1)

set(CMAKE_OSX_DEPLOYMENT_TARGET "10.12" CACHE STRING "Minimum OS X deployment target")
if(WIN32)
    set(CMAKE_SYSTEM_VERSION 7.1 CACHE STRING INTERNAL FORCE) # Windows SDK for Windows 7 and up
    set(CMAKE_MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>" CACHE STRING "Runtime")
endif()

project(MultuBandComp VERSION 0.0.1)
set(CMAKE_CXX_STANDARD 20)
set(COMPANY_NAME "Ori Zur")
set(PRODUCT_NAME "MultiBand Compressor")

add_subdirectory(modules)
