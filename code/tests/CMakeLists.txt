include_directories(../src)
include_directories(.)

add_executable(dfa_tests
    # list of tests
    dfa_test.cpp

    # list of sources of the lib   
    ../src/fsa/dfa.hpp

    # gtest sources
    gtest/gtest-all.cc
    gtest/gtest_main.cc
)

# add pthread for unix systems
if (UNIX)
    target_link_libraries(tests pthread)
endif ()
