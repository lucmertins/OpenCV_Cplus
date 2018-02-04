cmake_minimum_required(VERSION 2.8)
project( TrainingOpenCV )

find_package( OpenCV REQUIRED )

include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable( TrainingOpenCV TrainingOpenCV.cpp )

target_link_libraries( TrainingOpenCV ${OpenCV_LIBS} )

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)

install(TARGETS TrainingOpenCV RUNTIME DESTINATION bin)

