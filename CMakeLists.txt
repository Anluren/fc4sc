# if SystemC or Gtest is not installed in system directory, then following 
# variable should be set.
# SYSTEMC_HOME - installation directory of SystemC
# GTEST_HOME  - installation directory of GoogleTest
cmake_minimum_required(VERSION 3.13)

project(fc4sc)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# set(CMAKE_MODULE_PATH ${SYSTEMC_HOME} ${GTEST_HOME})

if(${SYSTEMC_HOME}) 
    list(APPEND CMAKE_MODULE_PATH ${SYSTEMC_HOME})
endif()

if(${GTEST_HOME}) 
    list(APPEND CMAKE_MODULE_PATH ${GTEST_HOME})
endif()

set(CMAKE_MODULE_PATH ${SYSTEMC_HOME} ${GTEST_HOME})
include(CMakePackageConfigHelpers)


find_package(SystemCLanguage REQUIRED)
find_package(GTest REQUIRED)

add_subdirectory(examples/fir)
add_subdirectory(test/fc4sc)
