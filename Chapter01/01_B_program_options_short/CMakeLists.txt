cmake_minimum_required(VERSION 3.12)
project(01_B_program_options_short)

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add the source files
add_executable(01_B_program_options_short main.cpp)

# Add any additional libraries or dependencies here
find_package(Boost REQUIRED COMPONENTS program_options)
target_link_libraries(01_B_program_options_short PRIVATE Boost::program_options)

# Set the output directory for the executable
set_target_properties(01_B_program_options_short PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin"
)
configure_file(${CMAKE_CURRENT_SOURCE_DIR}/apples_oranges.cfg ${CMAKE_BINARY_DIR}/bin/apples_oranges.cfg COPYONLY)
