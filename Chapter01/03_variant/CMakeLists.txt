cmake_minimum_required(VERSION 3.12)
project(03_variant)

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add the source files
add_executable(03_variant main.cpp)

# Add any additional libraries or dependencies here
find_package(Boost REQUIRED)
target_link_libraries(03_variant PRIVATE Boost::boost)

# Set the output directory for the executable
set_target_properties(03_variant PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin"
)
