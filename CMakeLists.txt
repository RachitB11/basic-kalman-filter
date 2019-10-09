cmake_minimum_required(VERSION 2.8.4)
project(kalman)
find_package(Eigen3 REQUIRED)
find_package(OpenCV REQUIRED)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

include_directories(${EIGEN3_INCLUDE_DIRS} ${OpenCV_INCLUDE_DIRS})

add_executable(kalman-test kalman.cpp kalman-test.cpp)
target_link_libraries( kalman-test ${OpenCV_LIBS} )

add_executable(sample_cv_plot sample_cv_plot.cpp)
target_link_libraries( sample_cv_plot ${OpenCV_LIBS} )
