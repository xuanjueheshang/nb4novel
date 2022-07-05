cmake_minimum_required(VERSION 3.21)

project ("NameBuilder" LANGUAGES C)
set(CMAKE_INSTALL_PREFIX ${CMAKE_SOURCE_DIR}/install)

add_executable (nb src/nb.c)

install(TARGETS nb CONFIGURATIONS Release)