cmake_minimum_required(VERSION 3.5.0)
project(gnome-shell-extension-userpasswd VERSION 0.0.1)

set (USER_HOME "$ENV{HOME}")
set (UUID "userpasswd@altlinux.org")

set (EXTENSION_FILES
    ${UUID}/extension.js
    ${UUID}/metadata.json
)

add_subdirectory(${UUID}/locale)

install (FILES ${EXTENSION_FILES}
         DESTINATION /usr/share/gnome-shell/extensions/${UUID})

set(CMAKE_CLEAN_FILES ${PROJECT_NAME})
include(GNUInstallDirs)
install(CODE "execute_process(COMMAND ${CMAKE_COMMAND} -E remove ${CMAKE_BINARY_DIR}/${PROJECT_NAME})")