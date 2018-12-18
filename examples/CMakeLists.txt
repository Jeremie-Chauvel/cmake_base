# Make sure the compiler can find include files from our library.
include_directories (${CMAKE_SOURCE_DIR}/src)

file(
	GLOB 
	usage_examples
	*.cpp
)

foreach(f ${usage_examples})
  get_filename_component(exampleName ${f} NAME_WE) 
  add_executable (${exampleName} ${f}) 
  set_target_properties (${exampleName} PROPERTIES LINKER_LANGUAGE CXX)
  set_target_properties (${exampleName} PROPERTIES COMPILE_FLAGS   "${PROJECT_CFLAGS} -Wall")
  # to add a lib:
  # target_include_directories(${exampleName} PUBLIC ${Lib_prefix1_INCLUDE_DIRS})
  # target_link_libraries (${exampleName} ${Lib_prefix1_LDFLAGS})
  install(PROGRAMS ${CMAKE_CURRENT_BINARY_DIR}/${exampleName}
    DESTINATION bin
    RENAME ${CMAKE_PROJECT_NAME}-${exampleName})
endforeach(f)

