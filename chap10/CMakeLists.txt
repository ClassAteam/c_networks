cmake_minimum_required(VERSION 3.8 FATAL_ERROR)

project(chap10 LANGUAGES C)

find_package(OpenSSL REQUIRED)

include(GNUInstallDirs)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_LIBDIR})
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_LIBDIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_BINDIR})

add_executable(https_server https_server.c)

target_link_libraries(https_server OpenSSL::Crypto OpenSSL::SSL)
