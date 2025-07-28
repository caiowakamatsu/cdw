include(FetchContent)

FetchContent_Declare(
	catch2
	GIT_REPOSITORY 	https://github.com/catchorg/Catch2.git
	GIT_TAG 				v3.8.1
)

FetchContent_MakeAvailable(catch2)

add_executable(cwd_tests 
	image/bmp_format.cpp
	image/basic_io.cpp
)
target_link_libraries(cwd_tests PUBLIC Catch2::Catch2WithMain)

