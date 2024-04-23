cmake_minimum_required(VERSION 3.15)
project(image2ascii CXX)

find_package(CURL CONFIG REQUIRED)
find_package(stb CONFIG REQUIRED)
find_package(fmt CONFIG REQUIRED)

add_executable(image2ascii src/main.cpp)

target_link_libraries(image2ascii PRIVATE CURL::libcurl)
target_link_libraries(image2ascii PRIVATE stb::stb)
target_link_libraries(image2ascii PRIVATE fmt::fmt)
