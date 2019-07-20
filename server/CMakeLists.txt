set(SERVER_SOURCE
    "sv_ccmds.c"
    "sv_ents.c"
    "sv_game.c"
    "sv_init.c"
    "sv_main.c"
    "sv_send.c"
    "sv_user.c"
    "sv_world.c"
)

set(SERVER_HEADER
    "."
    "../qcommon"
)

include_directories(${SERVER_HEADER})
add_library(server STATIC ${SERVER_SOURCE})
target_link_libraries(server gamex86 ctf)
target_include_directories(server PUBLIC .)
# set_source_files_properties(ctf.def PROPERTIES HEADER_FILE_ONLY true)