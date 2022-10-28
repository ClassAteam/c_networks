cmake_minimum_required(VERSION 3.8 FATAL_ERROR)

project(chap11 LANGUAGES C)

find_package(libssh REQUIRED)

include(GNUInstallDirs)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_LIBDIR})
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_LIBDIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${CMAKE_INSTALL_BINDIR})

list(APPEND execs
  ssh_version
  ssh_connect
  ssh_auth
  ssh_command
  )

foreach(_exec IN LISTS execs)
  add_executable(${_exec} ${_exec}.c)
  target_link_libraries(${_exec} ssh)
endforeach()
