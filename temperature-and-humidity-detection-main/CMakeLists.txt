cmake_minimum_required (VERSION 3.0) 
project (TandH)


include_directories(include)

find_package(wiringPi REQUIRED)


include_directories(${WIRINGPI_INCLUDE_DIRS})

add_executable (TandH_cmake temperature_and_humidity_detection.cpp )  
target_link_libraries(TandH_cmake ${WIRINGPI_LIBRARIES})
