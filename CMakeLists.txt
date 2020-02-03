cmake_minimum_required(VERSION 2.8 FATAL_ERROR) 
project(pcd_write)

find_package(PCL 1.2 REQUIRED)
include_directories(${PCL_INCLUDE_DIRS}) 
link_directories(${PCL_LIBRARY_DIRS}) 
add_definitions(${PCL_DEFINITIONS})

include_directories(include) 
file(GLOB SOURCES "src/*.cpp")

add_executable(pcd_write ${SOURCES}) 
target_link_libraries (pcd_write ${PCL_LIBRARIES})
set_target_properties(pcd_write
    PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY "bin"
)
