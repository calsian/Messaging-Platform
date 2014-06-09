cmake_minimum_required (VERSION 2.6)
project (Tutorial)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++0x")

set(Boost_INCLUDE_DIR /usr/local/include)
set(Boost_LIBRARY_DIR /usr/local/lib)
INCLUDE_DIRECTORIES( ${Boost_INCLUDE_DIR} )
link_directories(${Boost_LIBRARY_DIR})

add_executable(Tutorial tutorial.cxx)

target_link_libraries( Tutorial boost_system pthread )
