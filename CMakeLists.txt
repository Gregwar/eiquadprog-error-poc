cmake_minimum_required(VERSION 3.16.3)
project(poc)

link_directories("/opt/openrobots/lib/")
include_directories("/opt/openrobots/include/")

find_package (Eigen3 3 REQUIRED NO_MODULE)

add_executable(demo main.cpp file_a.cpp file_b.cpp)
target_link_libraries(demo PUBLIC eiquadprog Eigen3::Eigen)