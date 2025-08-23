cmake_minimum_required(VERSION 3.15)

set(SUBDIR_NAME sqlite_modern_cpp)

add_library(${SUBDIR_NAME} STATIC hdr/sqlite_modern_cpp.h)

set_target_properties(${SUBDIR_NAME} PROPERTIES LINKER_LANGUAGE CXX)
target_include_directories(${SUBDIR_NAME} PUBLIC hdr)

find_package(SQLite3) # Checking if sqlite3 exists
target_link_libraries(${SUBDIR_NAME} PUBLIC sqlite3)
