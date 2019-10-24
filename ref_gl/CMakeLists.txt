set(REF_GL_SOURCE
    gl_draw.c
    gl_image.c
    gl_light.c
    gl_image.c
    gl_mesh.c
    gl_model.c
    gl_rmain.c
    gl_rmisc.c
    gl_rsurf.c
    gl_warp.c
    ../win32/glw_imp.c
    ../win32/qgl_win.c
    ../win32/q_shwin.c
    ref_gl.def
)

set(REF_GL_HEADER
    "."
    "../client"
    "../game"
    "../qcommon"
    "../win32"
    "../ref_soft"
)

include_directories(${REF_GL_HEADER})
add_library(ref_gl SHARED ${REF_GL_SOURCE})
target_link_libraries(ref_gl ctf gamex86 opengl32 winmm ws2_32)

target_include_directories(ref_gl PUBLIC .)