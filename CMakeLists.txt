cmake_minimum_required(VERSION 3.7)
project(Poly2Tri)
set(CMAKE_VERBOSE_MAKEFILE ON)
set(CMAKE_CXX_FLAGS "-std=c++11 -fPIC")

include_directories(
        common
        sweep
)

set(SRC

        common/shapes.cc
        sweep/cdt.cc
        sweep/advancing_front.cc
        sweep/sweep.cc
        sweep/sweep_context.cc
        )

add_library(poly2tri STATIC ${SRC})