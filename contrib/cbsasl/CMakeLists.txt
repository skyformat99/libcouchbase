INCLUDE_DIRECTORIES(src)
FILE(GLOB CBSASL_SRC src/*.c)
FILE(GLOB CRAM_SRC src/cram-md5/*.c)

ADD_LIBRARY(cbsasl OBJECT ${CBSASL_SRC} ${CRAM_SRC})
SET_TARGET_PROPERTIES(cbsasl
    PROPERTIES
    POSITION_INDEPENDENT_CODE TRUE
    COMPILE_FLAGS "${LCB_CORE_CFLAGS}")
