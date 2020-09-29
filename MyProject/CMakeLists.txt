cmake_minimum_required(VERSION 3.18.2)

#set project
project(MyProjectCPP)

#set standart and flags
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -g")

file(GLOB 
	CPPS "*.cpp"
	CS   "*.c")
add_executable(${PROJECT_NAME} ${CPPS} ${CS})
