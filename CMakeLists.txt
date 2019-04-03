
cmake_minimum_required( VERSION 3.5.1 ) 
set (CMAKE_CXX_STANDARD 11)

project( cvVideoCapture ) 
 
 

find_package( OpenCV REQUIRED ) 
 

include_directories( ${OpenCV_INCLUDE_DIRS})
 

add_executable( cvVideoCapture src/cvVideoCapture.cpp ) 
target_link_libraries( cvVideoCapture ${OpenCV_LIBS}) 


find_package(OpenCV)

message(STATUS "OpenCV_INCLUDE_DIRS = ${OpenCV_INCLUDE_DIRS}")
message(STATUS "OpenCV_LIBS = ${OpenCV_LIBS}")
