cmake_minimum_required(VERSION 3.8 FATAL_ERROR)

project(chap09 LANGUAGES C)

find_package(OpenSSL REQUIRED)

include(GNUInstallDirs)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_LIBDIR})
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_LIBDIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_BINDIR})

add_executable(openssl_version openssl_version.c)
add_executable(https_simple https_simple.c)

target_link_libraries(openssl_version OpenSSL::Crypto)
target_link_libraries(https_simple OpenSSL::Crypto OpenSSL::SSL)
