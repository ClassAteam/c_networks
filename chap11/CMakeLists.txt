cmake_minimum_required(VERSION 3.8 FATAL_ERROR)

project(chap11 LANGUAGES C)

find_package(libssh REQUIRED)

include(GNUInstallDirs)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_LIBDIR})
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_LIBDIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_BINDIR})

add_executable(ssh_version ssh_version.c)
add_executable(ssh_connect ssh_connect.c)

target_link_libraries(ssh_version ssh)
target_link_libraries(ssh_connect ssh)
