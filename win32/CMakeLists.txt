# exe - client/server, win32/linux

set(QCOMMON_SRC
	../qcommon/cmd.c
	../qcommon/cmodel.c
	../qcommon/common.c
	../qcommon/crc.c
	../qcommon/cvar.c
	../qcommon/files.c
	../qcommon/md4.c
	../qcommon/net_chan.c
	../qcommon/pmove.c
	../game/q_shared.c)

set(CLIENT_SRC
	../game/m_flash.c
	../client/cl_cin.c
	../client/cl_ents.c
	../client/cl_fx.c
	../client/cl_input.c
	../client/cl_inv.c
	../client/cl_newfx.c
	../client/cl_parse.c
	../client/cl_pred.c
	../client/cl_scrn.c
	../client/cl_tent.c
	../client/cl_view.c
	../client/console.c
	../client/keys.c
	../client/menu.c
	../client/qmenu.c
	../client/snd_dma.c
	../client/snd_mem.c
	../client/snd_mix.c
	../client/x86.c
	../client/cl_main.c)

set(SERVER_SRC
	../server/sv_ccmds.c
	../server/sv_ents.c
	../server/sv_game.c
	../server/sv_init.c
	../server/sv_send.c
	../server/sv_user.c
	../server/sv_world.c
	../server/sv_main.c)

set(QUAKE2_SOURCE
    cd_win.c
	conproc.c
	#glw_imp.c
	in_win.c
	net_wins.c
	q_shwin.c
	#qgl_win.c
	#rw_ddraw.c
	#rw_dib.c
	#rw_imp.c
	snd_win.c
	sys_win.c
	vid_dll.c
	vid_menu.c
)

set(QUAKE2_HEADER
    "./"
    "../ref_gl"
    "../ref_soft"
    "../client"
    "../game"
    "../qcommon"
)

include_directories(${QUAKE2_HEADER})

add_executable(${PROJECT_NAME} ${QUAKE2_SOURCE} ${CLIENT_SRC} ${SERVER_SRC} ${QCOMMON_SRC})
target_link_libraries(${PROJECT_NAME} opengl32 winmm ws2_32) #gamex86 client server opengl32 winmm ws2_32)
#gamex86 client server
