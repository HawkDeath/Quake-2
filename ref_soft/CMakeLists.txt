set(REF_SOFT_SOURCE
    "r_aclip.c"
    "r_alias.c"
    "r_bsp.c"
    "r_draw.c"
    "r_edge.c"
    "r_image.c"
    "r_light.c"
    "r_main.c"
    "r_misc.c"
    "r_model.c"
    "r_part.c"
    "r_poly.c"
    "r_polyse.c"
    "r_rast.c"
    "r_scan.c"
    "r_sprite.c"
    "r_surf.c"
    "../win32/rw_imp.c"
    "../win32/q_shwin.c"
    "../win32/rw_dib.c"
    "../win32/rw_ddraw.c"
    "ref_soft.def"
)

set(REF_SOFT_HEADER
    "."
    "../client"
    "../game"
    "../qcommon"
    "../win32"
)

include_directories(${REF_SOFT_HEADER})
add_library(ref_soft SHARED ${REF_SOFT_SOURCE})
target_link_libraries(ref_soft client server ctf gamex86 winmm ws2_32)

target_include_directories(ref_soft PUBLIC .)