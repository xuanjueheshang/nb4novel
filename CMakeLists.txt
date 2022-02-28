cmake_minimum_required(VERSION 3.21)

project ("NameBuilder" LANGUAGES C)
set(CMAKE_INSTALL_PREFIX "E:/CMakeProjects/NameBuilder-CMD/install")
set(CMAKE_MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>")

set(SFILE "src/nb.c") # 材料
add_executable (nb ${SFILE})

install(TARGETS nb CONFIGURATIONS Release DESTINATION .)