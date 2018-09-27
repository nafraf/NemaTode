cmake_minimum_required(VERSION 3.10)
project(nematode)

set(CMAKE_CXX_STANDARD 11)

set(LIB_SOURCES
        src/GPSFix.cpp
        src/GPSService.cpp
        src/NMEACommand.cpp
        src/NMEAParser.cpp
        src/NumberConversion.cpp
        )

add_library(NemaTode SHARED ${LIB_SOURCES})
target_include_directories(NemaTode PRIVATE include/nmeaparse)

install(TARGETS NemaTode DESTINATION ${EXE_DIR})
