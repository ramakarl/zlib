SET(C_SOURCE
   ioapi.c
   mztools.c
   unzip.c
   zip.c
)

IF(WIN32)
   SET(C_SOURCE ${C_SOURCE} iowin32.c)
ENDIF()

add_library(minizip_static STATIC ${C_SOURCE})
