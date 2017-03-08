cmake_minimum_required(VERSION 3.6)
project(Cdemo)

set(CMAKE_C_STANDARD 99)
set(SOURCE_FILES main.c)
add_executable(Cdemo ${SOURCE_FILES})

set(CMAKE_MODULE_PATH "/Users/zyang/CLionProjects/Cdemo/cmake-build-debug/Modules" ${CMAKE_MODULE_PATH})

find_package (libpcap)

message("ssn")

if(libpcap_FOUND)

    message(STATUS "libpcap_INCLUDE_DIRS: ${libpcap_INCLUDE_DIRS}")
    message(STATUS "libpcap_LIBRARIES: ${libpcap_LIBRARIES}")
    message(STATUS "libpcap_VERSION: ${libpcap_VERSION}")

    include_directories(${libpcap_INCLUDE_DIRS})

endif()
