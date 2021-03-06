CMAKE_MINIMUM_REQUIRED(VERSION 3.0)

PROJECT(UEFIFind)

SET(PROJECT_SOURCES
 uefifind_main.cpp
 uefifind.cpp
 ../common/guiddatabase.cpp
 ../common/types.cpp
 ../common/descriptor.cpp
 ../common/ffs.cpp
 ../common/nvram.cpp
 ../common/nvramparser.cpp
 ../common/ffsparser.cpp
 ../common/ffsreport.cpp
 ../common/ffsutils.cpp
 ../common/peimage.cpp
 ../common/treeitem.cpp
 ../common/treemodel.cpp
 ../common/utility.cpp
 ../common/LZMA/LzmaDecompress.c
 ../common/LZMA/SDK/C/Bra86.c
 ../common/LZMA/SDK/C/LzmaDec.c
 ../common/Tiano/EfiTianoDecompress.c
 ../common/ustring.cpp
 ../common/sha256.c
 ../common/bstrlib/bstrlib.c
 ../common/bstrlib/bstrwrap.cpp
 ../common/zlib/adler32.c
 ../common/zlib/compress.c
 ../common/zlib/crc32.c
 ../common/zlib/deflate.c
 ../common/zlib/gzclose.c
 ../common/zlib/gzlib.c
 ../common/zlib/gzread.c
 ../common/zlib/gzwrite.c
 ../common/zlib/inflate.c
 ../common/zlib/infback.c
 ../common/zlib/inftrees.c
 ../common/zlib/inffast.c
 ../common/zlib/trees.c
 ../common/zlib/uncompr.c
 ../common/zlib/zutil.c
)

SET(PROJECT_HEADERS
 uefifind.h
 ../common/guiddatabase.h
 ../common/basetypes.h
 ../common/descriptor.h
 ../common/gbe.h
 ../common/me.h
 ../common/ffs.h
 ../common/nvram.h
 ../common/nvramparser.h
 ../common/ffsparser.h
 ../common/ffsreport.h
 ../common/ffsutils.h
 ../common/peimage.h
 ../common/types.h
 ../common/treeitem.h
 ../common/treemodel.h
 ../common/utility.h
 ../common/LZMA/LzmaDecompress.h
 ../common/Tiano/EfiTianoDecompress.h
 ../common/ubytearray.h
 ../common/ustring.h
 ../common/bootguard.h
 ../common/sha256.h
 ../common/filesystem.h
 ../common/bstrlib/bstrlib.h
 ../common/bstrlib/bstrwrap.h
 ../common/zlib/zconf.h
 ../common/zlib/zlib.h
 ../common/zlib/crc32.h
 ../common/zlib/deflate.h
 ../common/zlib/gzguts.h
 ../common/zlib/inffast.h
 ../common/zlib/inffixed.h
 ../common/zlib/inflate.h
 ../common/zlib/inftrees.h
 ../common/zlib/trees.h
 ../common/zlib/zutil.h
 ../version.h
)

ADD_DEFINITIONS(-DU_ENABLE_NVRAM_PARSING_SUPPORT -DU_ENABLE_FIT_PARSING_SUPPORT -DU_ENABLE_GUID_DATABASE_SUPPORT)

ADD_EXECUTABLE(UEFIFind ${PROJECT_SOURCES} ${PROJECT_HEADERS})

