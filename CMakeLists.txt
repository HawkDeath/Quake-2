cmake_minimum_required(VERSION 3.15)
project(Quake-2)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)

add_definitions(-DWIN32 -DNDEBUG)

add_subdirectory(ctf)
add_subdirectory(game)
add_subdirectory(server)
add_subdirectory(client)
add_subdirectory(ref_soft)
add_subdirectory(ref_gl)

add_subdirectory(win32)