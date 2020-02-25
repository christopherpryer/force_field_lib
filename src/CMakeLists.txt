cmake_minimum_required(VERSION 3.4)
project(test_main
	VERSION 0.0.0
	LANGUAGES
		CXX
)

FIND_PACKAGE(Boost)
IF (Boost_FOUND)
    INCLUDE_DIRECTORIES(${Boost_INCLUDE_DIR})
    ADD_DEFINITIONS( "-DHAS_BOOST" )
ENDIF()

file(GLOB SOURCES "../tests/*.cpp" "../src/*.cpp")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../bin)
add_executable(test_main ${SOURCES})
target_link_libraries(test_main ${Boost_LIBRARIES})


