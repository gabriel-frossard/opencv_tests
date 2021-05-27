cmake_minimum_required( VERSION 2.8 )
set(CMAKE_BUILD_TYPE Release)
project (project)

include_directories(/usr/include/OGRE/)

SET(OpenCV_DIR /installation/OpenCV-master/lib/cmake/opencv4)

find_package(OpenCV 4.0.0 REQUIRED COMPONENTS core imgproc highgui)


add_executable(main_detection src/main_detection.cpp)
target_link_libraries(main_detection ${OpenCV_LIBS})
