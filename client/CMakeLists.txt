set(CLIENT_SOURCE
    cl_cin.c
    cl_ents.c
    cl_fx.c
    cl_input.c
    cl_inv.c
    cl_main.c
    cl_newfx.c
    cl_parse.c
    cl_pred.c
    cl_scrn.c
    cl_tent.c
    cl_view.c
    console.c
    keys.c
    menu.c
    qmenu.c
    snd_dma.c
    snd_mem.c
    snd_mix.c
    x86.c
    ../qcommon/cmd.c
    ../qcommon/cmodel.c
    ../qcommon/common.c
    ../qcommon/crc.c
    ../qcommon/cvar.c
    ../qcommon/files.c
    ../qcommon/md4.c
    ../qcommon/pmove.c
    ../qcommon/net_chan.c
    ../game/m_flash.c
)

set(CLIENT_HEADER
    ../qcommon
)

include_directories(${CLIENT_HEADER})
add_library(client STATIC ${CLIENT_SOURCE})
target_link_libraries(client server gamex86 ctf)
target_include_directories(client PUBLIC .)
# set_source_files_properties(ctf.def PROPERTIES HEADER_FILE_ONLY true)