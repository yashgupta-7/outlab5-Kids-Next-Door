cmake_minimum_required (VERSION 3.1.0)
set(cmake_cxx_standard 14)
project(outlab5)

add_executable(mygamestatic mygame.cpp)
include_directories(usr/local/lib)
target_link_libraries(mygamestatic MyEngineStatic)

add_executable(mygamedynamic mygame.cpp)
include_directories(usr/local/lib)
target_link_libraries(mygamedynamic MyEngineDynamic)