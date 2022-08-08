cmake_minimum_required(VERSION 3.18)
project(application9 C)

set(CMAKE_C_STANDARD 11)
FIND_PACKAGE(PkgConfig REQUIRED)
PKG_CHECK_MODULES(GTK3 REQUIRED gtk+-3.0)

INCLUDE_DIRECTORIES(${GTK3_INCLUDE_DIRS})
LINK_DIRECTORIES(${GTK3_LIBRARY_DIRS})
include_directories(.)

add_executable(application9
        exampleapp.c
        exampleapp.h
        exampleappprefs.c
        exampleappprefs.h
        exampleappwin.c
        exampleappwin.h
        main.c
        resources.c)
TARGET_LINK_LIBRARIES(application9 ${GTK3_LIBRARIES})
