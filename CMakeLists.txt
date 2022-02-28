##############################################################
cmake_minimum_required(VERSION 3.21) #qt6 required

set(CMAKE_TOOLCHAIN_FILE "D:/VCPKG/scripts/buildsystems/vcpkg.cmake")
set(VCPKG_TARGET_TRIPLET "x64-windows-static")
add_definitions(-DUNICODE "-D_UNICODE")
##############################################################

project ("NameBuilder" LANGUAGES C)
set(CMAKE_INSTALL_PREFIX "E:/CMakeProjects/NameBuilder-CMD/install")
set(CMAKE_MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>")
# set(CMAKE_MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>DLL")

set(SFILE "src/nb.c") # 材料
add_executable (nb ${SFILE})

install(TARGETS nb CONFIGURATIONS Release DESTINATION .)