cmake_minimum_required(VERSION 3.2)
project(b2dJson C CXX)

find_package(Box2D REQUIRED)

file(GLOB_RECURSE B2DJSON_SOURCES src/*.cpp)
add_library(b2dJson ${B2DJSON_SOURCES})
set_target_properties(b2dJson PROPERTIES LINKER_LANGUAGE CXX)
target_include_directories(b2dJson PUBLIC src)
target_link_libraries(b2dJson ${BOX2D_LIBRARIES})