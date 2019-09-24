cmake_minimum_required (VERSION 3.1.0)
set(CMAKE_CXX_STANDARD 14)

project (outlab5)
include_directories(myengine)

add_executable(helloworld helloworld.cpp)

add_executable(usespthread usespthread.cpp)
target_link_libraries(usespthread pthread)

add_library(MyEngineDynamic SHARED myengine/myengine.hpp myengine/myengine.cpp)

add_library(MyEngineStatic STATIC myengine/myengine.hpp myengine/myengine.cpp)

install(TARGETS MyEngineDynamic DESTINATION /usr/local/lib)

install(TARGETS MyEngineStatic DESTINATION /usr/local/lib)

install(FILES myengine/myengine.hpp DESTINATION /usr/local/include)