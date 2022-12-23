cmake_minimum_required( VERSION 3.20 )
project( sqlite )
set( CMAKE_CXX_STANDARD 23 )

set( SOURCES
        src/sqlite3.c )

set( HEADERS
        include/Sqlite/Private/sqlite3.h
        include/Sqlite/Sqlite.h )

add_library( ${PROJECT_NAME} STATIC ${SOURCES} ${HEADERS} )
target_include_directories( ${PROJECT_NAME} PUBLIC include )
