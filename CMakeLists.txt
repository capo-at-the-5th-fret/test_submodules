cmake_minimum_required(VERSION 3.26)

project(test_submodules LANGUAGES CXX)

add_subdirectory(extern/fmt)

add_executable(test_submodules
    
    main.cpp
    
)

target_compile_features(test_submodules PUBLIC cxx_std_23)
target_link_libraries(test_submodules PUBLIC fmt::fmt)
