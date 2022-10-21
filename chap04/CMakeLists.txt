cmake_minimum_required(VERSION 3.8 FATAL_ERROR)

project(chap04 LANGUAGES C)

include(GNUInstallDirs)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_LIBDIR})
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_LIBDIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_BINDIR})

add_executable(udp_recvfrom udp_recvfrom.c)
add_executable(udp_client udp_client.c)
add_executable(udp_sendto udp_sendto.c)
add_executable(udp_serve_toupper udp_serve_toupper.c)
