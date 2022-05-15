cmake_minimum_required(VERSION 3.21)

project ("NameBuilder" LANGUAGES C)
set(CMAKE_INSTALL_PREFIX "E:/CMakeProjects/NameBuilder/install")
set(CMAKE_MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>")

add_executable (nb src/nb.c)

install(TARGETS nb CONFIGURATIONS Release DESTINATION .)