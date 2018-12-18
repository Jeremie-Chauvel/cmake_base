CMAKE_MINIMUM_REQUIRED( VERSION 2.8.4 )

project(project_name)

set(PACKAGE_VERSION "1.00")
set(PACKAGE_LICENSE "GPL")
set(PROJECT_DESCRIPTION_SUMMARY "my_description")



set(CMAKE_BUILD_TYPE Debug)
set(PROJECT_CFLAGS "-std=c++17")

 
# Installation common variables

# set(INCLUDE_INSTALL_DIR "${CMAKE_INSTALL_PREFIX}/include/${CMAKE_PROJECT_NAME}/" CACHE PATH "The subdirectory to the header prefix")

# Dependencies
# can be useful help pkgConfig find pc files
# set(CMAKE_PREFIX_PATH "/usr/lib/pkgconfig/")

# find_package(PkgConfig)
# pkg_check_modules(Lib_prefix1 lib_name1 REQUIRED)
# pkg_check_modules(Lib_prefix2 lib_name2 REQUIRED)


# set(PKG_CONFIG_DEPENDS "lib_name1 lib_name2")


# Pkg-config 

# to be included by another project we need a pc file

# file(WRITE ${CMAKE_CURRENT_BINARY_DIR}/${CMAKE_PROJECT_NAME}.pc
# "
# Name: ${CMAKE_PROJECT_NAME}
# Description: ${PROJECT_DESCRIPTION_SUMMARY}
# Version: ${PACKAGE_VERSION}
# Requires: ${PKG_CONFIG_DEPENDS}
# Libs: 
# Cflags: -I${INCLUDE_INSTALL_DIR} ${PROJECT_CFLAGS}
# "
# )

# Define the path to install the pc pkg-config file
# set(PKGCONFIG_INSTALL_DIR "${CMAKE_INSTALL_PREFIX}/lib/pkgconfig/" CACHE STRING "Base directory for pkgconfig files")

# install(FILES ${CMAKE_CURRENT_BINARY_DIR}/${CMAKE_PROJECT_NAME}.pc
#     	DESTINATION ${PKGCONFIG_INSTALL_DIR})

#  Subdirectories

add_subdirectory(src)
add_subdirectory(doc)
add_subdirectory(examples)
add_subdirectory(data)