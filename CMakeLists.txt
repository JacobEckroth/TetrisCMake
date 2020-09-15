cmake_minimum_required(VERSION 3.18)

project("Tetris")


add_executable("${PROJECT_NAME}" main.cpp)

install(TARGETS "${PROJECT_NAME}" DESTINATION bin) #${CMAKE_INSTALL_PREFIX}/bin	#pound is comment
install (FILES main.cpp DESTINATION src) 			#${CMAKE_INSTALL_PREFIX}/src	#pound is comment

