# headers:
file(GLOB headers   project_name*.hpp)
install(FILES   ${headers} DESTINATION include/${CMAKE_PROJECT_NAME})

# cpp, compile a lib:

# file(GLOB lib_files project_name*.cpp)

# add_library(${CMAKE_PROJECT_NAME} SHARED ${lib_files})

# target_include_directories(${CMAKE_PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
# target_compile_options(${CMAKE_PROJECT_NAME} PUBLIC -std=c++11)

# install(TARGETS ${CMAKE_PROJECT_NAME} DESTINATION lib)

