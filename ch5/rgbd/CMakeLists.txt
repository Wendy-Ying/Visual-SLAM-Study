add_compile_options(-std=c++11)

find_package(Sophus REQUIRED)
include_directories(${Sophus_INCLUDE_DIRS})
set (Sophus_LIBRARIES "/usr/local/lib/libSophus.so")

find_package(Pangolin REQUIRED)

add_executable(joinMap joinMap.cpp)
target_link_libraries(joinMap ${OpenCV_LIBS} ${Pangolin_LIBRARIES} ${Sophus_LIBRARIES})
