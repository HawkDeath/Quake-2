cmake_minimum_required(VERSION 3.15)
project(Quake-2)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
#set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} /SUBSYSTEM:WINDOWS /ENTRY:mainCRTStartup")

add_definitions(-DWIN32 -DNDEBUG -DC_ONLY)
# 3 different targets:
# exe - client/server, win32/linux
# render.dll - ref_soft, ref_gl
# game.dll - ctf, game

add_subdirectory(ctf)
add_subdirectory(game)
#add_subdirectory(server)
#add_subdirectory(client)
add_subdirectory(ref_soft)
add_subdirectory(ref_gl)

add_subdirectory(win32)