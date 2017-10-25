project(MiniCaffe-Examples)
cmake_minimum_required(VERSION 2.8)

find_package(OpenCV REQUIRED)
include(../mini-caffe.cmake)

add_executable(deeplandmark deeplandmark/landmark.hpp deeplandmark/landmark.cpp deeplandmark/main.cpp)
target_link_libraries(deeplandmark minicaffe ${OpenCV_LIBS})

add_executable(wgan wgan/main.cpp)
target_link_libraries(wgan minicaffe ${OpenCV_LIBS})

add_executable(r-fcn r-fcn/main.cpp)
target_link_libraries(r-fcn minicaffe ${OpenCV_LIBS})

add_executable(cloud_detector cloud_detector/main.cpp)
target_link_libraries(cloud_detector minicaffe ${OpenCV_LIBS})
