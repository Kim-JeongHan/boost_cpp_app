cmake_minimum_required(VERSION 3.12)
project(01_A_program_options_base)

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add the source files
add_executable(01_A_program_options_base main.cpp)

# Add any additional libraries or dependencies here
find_package(Boost REQUIRED COMPONENTS program_options)
target_link_libraries(01_A_program_options_base PRIVATE Boost::program_options)

# Set the output directory for the executable
set_target_properties(01_A_program_options_base PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin"
)