cmake_minimum_required(VERSION 2.8.12.1)

PROJECT(project2B C CXX)
SET(VTK_DIR ~/Desktop/VTK-6.3.0/build)

find_package(VTK REQUIRED)
include(${VTK_USE_FILE})

add_executable(project2B project2B)

if(VTK_LIBRARIES)
  target_link_libraries(project2B ${VTK_LIBRARIES})
else()
  target_link_libraries(project2B vtkHybrid)
endif()

