cmake_minimum_required(VERSION 3.10)
project(BunnyWaterSim)
set(CMAKE_CXX_STANDARD 17)

# Include and link GLFW & GLAD
include_directories(${CMAKE_SOURCE_DIR}/include /opt/homebrew/include)
link_directories(/opt/homebrew/lib)

file(GLOB SRC_FILES src/*.cpp src/glad.c)

add_executable(bunny_sim ${SRC_FILES})

target_link_libraries(bunny_sim glfw ${CMAKE_DL_LIBS})
