cmake_minimum_required(VERSION 2.4)

project(LinuxSorting C)
find_package(Threads REQUIRED)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_FLAGS "-ansi -pedantic")

add_executable(csorth ./src/csorth.c)
add_executable(csortp ./src/csortp.c)
add_executable(csortpexec ./src/csortpexec.c)
target_link_libraries(csorth ${CMAKE_THREAD_LIBS_INIT})