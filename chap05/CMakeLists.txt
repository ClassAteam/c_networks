cmake_minimum_required(VERSION 3.8 FATAL_ERROR)

project(chap05 LANGUAGES C)

include(GNUInstallDirs)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_LIBDIR})
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_LIBDIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_BINDIR})

<<<<<<< HEAD
=======
add_executable(dns_query dns_query.c)
>>>>>>> 8aa82b20ce55c7ec64acebd5b87b2cb9912d573b
add_executable(lookup lookup.c)
