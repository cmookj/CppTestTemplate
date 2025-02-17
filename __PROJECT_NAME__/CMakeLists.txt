cmake_minimum_required (VERSION 3.16..3.24)
project (__PROJECT_NAME__ VERSION 0.0.1
                    DESCRIPTION "A project"
                    LANGUAGES CXX)

add_library (__PROJECT_NAME__ STATIC
    ${PROJECT_SOURCE_DIR}/src/main.cpp)

target_include_directories (__PROJECT_NAME__ PUBLIC
    ${PROJECT_SOURCE_DIR}/include)

