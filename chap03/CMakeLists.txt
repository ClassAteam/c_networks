cmake_minimum_required(VERSION 3.8 FATAL_ERROR)

project(chap03 LANGUAGES C)

include(GNUInstallDirs)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_LIBDIR})
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_LIBDIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_BINDIR})

add_executable(time_server time_server.c)
add_executable(time_server_ipv6 time_server_ipv6.c)
add_executable(time_server_dual time_server_dual.c)
