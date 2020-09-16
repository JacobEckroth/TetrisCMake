cmake_minimum_required(VERSION 3.18)

project("Tetris")
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/")




find_package(SDL2 REQUIRED)




add_executable("${PROJECT_NAME}" main.cpp Board.cpp Box.cpp HoldRectangle.cpp nextShapesHolder.cpp Piece.cpp Window.cpp)

include_directories("${PROJECT_NAME}" ${SDL2_INCLUDE_DIRS})
target_link_libraries("${PROJECT_NAME}" ${SDL2_LIBRARIES})




install(TARGETS "${PROJECT_NAME}" DESTINATION bin) #${CMAKE_INSTALL_PREFIX}/bin	#pound is comment
install (FILES main.cpp DESTINATION src) 			#${CMAKE_INSTALL_PREFIX}/src	#pound is comment
include_directories("${PROJECT_SOURCE_DIR}")		#includes the .h files



include(CTest)

add_test("test1" "${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}")

include(CPack)
