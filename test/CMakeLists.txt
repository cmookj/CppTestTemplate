# BUILD_TESTING variable is created by include(CTest)
# It is set to ON by default
if (BUILD_TESTING)
    add_executable (__PROJECT_NAME___test test.cpp)
    target_link_libraries (__PROJECT_NAME___test PRIVATE 
        __PROJECT_NAME__
        GTest::gtest_main)

    target_include_directories (__PROJECT_NAME___test PRIVATE 
        ${PROJECT_SOURCE_DIR}/__PROJECT_NAME__/include)

    include (GoogleTest)
    # Finds all the Google tests associated with the executable
    gtest_discover_tests (__PROJECT_NAME___test)
endif()

