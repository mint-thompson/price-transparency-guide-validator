cmake_minimum_required(VERSION 3.10)
include(CMakePrintHelpers)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
project(SchemaValidator)
add_executable(SchemaValidator schemavalidator.cpp)
target_include_directories(SchemaValidator PUBLIC
    "${CMAKE_CURRENT_LIST_DIR}/rapidjson/include"
    "${CMAKE_CURRENT_LIST_DIR}/tclap/include"
)
target_link_libraries(SchemaValidator stdc++fs)

cmake_print_properties(TARGETS ${PROJECT_NAME} PROPERTIES INCLUDE_DIRECTORIES)