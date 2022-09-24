cmake_minimum_required(VERSION 3.23)
project(c_gtk4_template C)

set(CMAKE_C_STANDARD 99)

find_package(PkgConfig REQUIRED)
pkg_check_modules(GTK4 REQUIRED gtk4)

include_directories(${GTK4_INCLUDE_DIRS})
link_directories(${GTK4_LIBRARY_DIRS})

add_definitions(${GTK4_CFLAGS_OTHER})

add_executable(c_gtk4_template src/main.c)

target_link_libraries(c_gtk4_template ${GTK4_LIBRARIES})
