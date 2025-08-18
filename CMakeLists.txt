cmake_minimum_required(VERSION 3.15)

set(SUBDIR_NAME sqlite_modern_cpp)

#add_compile_options(-w)

#set_source_files_properties(hdr PROPERTIES COMPILE_FLAGS "-w")

add_library(${SUBDIR_NAME} INTERFACE hdr/sqlite_modern_cpp.h)

#set_target_properties(${SUBDIR_NAME} PROPERTIES COMPILE_FLAGS -w)
#get_target_property(OPTIONS_TO_PRINT ${SUBDIR_NAME} COMPILE_FLAGS)
#message(STATUS "Options: ${OPTIONS_TO_PRINT}")
#target_compile_options(${SUBDIR_NAME} INTERFACE -w)
#set_target_properties(${SUBDIR_NAME} PROPERTIES COMPILE_OPTIONS "${CMAKE_CXX_FLAGS} -Wall -Wextra -Wpedantic")
target_include_directories(${SUBDIR_NAME} INTERFACE hdr)

target_link_libraries(${SUBDIR_NAME} INTERFACE sqlite3)
