add_compile_options(-std=c++11)
find_package(Pangolin REQUIRED)
find_package(Sophus REQUIRED)
include_directories(${Sophus_INCLUDE_DIRS})
include_directories(${Pangolin_INCLUDE_DIRS})
set (Sophus_LIBRARIES "/usr/local/lib/libSophus.so")
add_executable(trajectoryError trajectoryError.cpp)
target_link_libraries(trajectoryError ${Pangolin_LIBRARIES})
target_link_libraries(trajectoryError ${Sophus_LIBRARIES})
