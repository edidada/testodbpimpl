cmake_minimum_required(VERSION 3.13)
project(testodbpimpl)

set(CMAKE_CXX_STANDARD 11)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -DDATABASE_MYSQL")

add_executable(testodbpimpl driver.cxx person.cxx person-odb.cxx)

target_link_libraries(testodbpimpl libodb-mysql.so)

target_link_libraries(testodbpimpl libodb.so)