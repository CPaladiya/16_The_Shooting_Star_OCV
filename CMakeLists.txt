cmake_minimum_required(VERSION 3.0.0)
project(ShootingStar)

find_package(OpenCV REQUIRED) #also notice O and C,V are capital
#by using required keyword we are telling cmake that OpenCV is required dependency
#and not an optional one, so if cmake doesnt find one, it will give an error
#if we dont use REQUIRED keyword, cmake will treat it as an optional requirement

add_executable(ShootingStar main.cpp)

target_include_directories(ShootingStar PRIVATE ${OpenCV_INCLUDE_DIRS})
target_link_libraries(ShootingStar PRIVATE ${OpenCV_LIBS})

#message("OpenCV Include directories : " ${OpenCV_INCLUDE_DIRS})
#message("OpenCV libraries : " ${OpenCV_LIBS})



