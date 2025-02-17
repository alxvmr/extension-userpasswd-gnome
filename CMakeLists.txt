cmake_minimum_required(VERSION 3.5.0)
project(extension-userpasswd-gnome VERSION 0.0.1)

add_subdirectory(userpasswd@altlinux.example.com/locale)

set(CMAKE_CLEAN_FILES ${PROJECT_NAME})
include(GNUInstallDirs)
install(CODE "execute_process(COMMAND ${CMAKE_COMMAND} -E remove ${CMAKE_BINARY_DIR}/${PROJECT_NAME})")