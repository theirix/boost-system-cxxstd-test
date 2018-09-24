cmake_minimum_required(VERSION 3.11)
project(main CXX)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

find_package(Boost 1.68.0 REQUIRED system)

add_executable(main main.cxx)
target_link_libraries(main PRIVATE Boost::system)
target_compile_features(main PUBLIC cxx_std_14)
