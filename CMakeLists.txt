cmake_minimum_required(VERSION 3.19)
project(fetch_content_test)

set(CMAKE_CXX_STANDARD 14)

add_library(car SHARED Car.cpp)
add_executable(fetch_content_test main.cpp)

target_link_libraries(
    fetch_content_test
    car
)
target_include_directories(
    car
    PUBLIC
    ./
)
