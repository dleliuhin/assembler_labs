#========================================================================================

cmake_minimum_required( VERSION 3.15 )

#========================================================================================

project( assembler_labs
    LANGUAGES C ASM )

#========================================================================================

set( CMAKE_EXPORT_COMPILE_COMMANDS ON )

#========================================================================================

include( ${CMAKE_CURRENT_SOURCE_DIR}/external/external.cmake )

#========================================================================================

include_directories( ${CMAKE_SOURCE_DIR} )

include( ${CMAKE_CURRENT_SOURCE_DIR}/cfg/cfg.cmake )
include( ${CMAKE_CURRENT_SOURCE_DIR}/src/src.cmake )

#========================================================================================

add_executable( MAIN_1 src/main_1.c )
add_executable( MAIN_2 src/main_2.c )
add_executable( MAIN_3 src/main_3.c )

target_link_libraries( MAIN_1 )
target_link_libraries( MAIN_2 )
target_link_libraries( MAIN_3 )

#========================================================================================

unset ( QT_QMAKE_EXECUTABLE )

#========================================================================================
