CMAKE_MINIMUM_REQUIRED(VERSION 2.6)
PROJECT(wt)

# definitions
#

# includes
SET(includes
    "../../include"
    )
INCLUDE_DIRECTORIES(${includes})

# sources
FILE(GLOB sources_c "../../posix/*.c")
FILE(GLOB support_c "../../support/*.c")
FILE(GLOB cursor_c "../../cursor/*.c")
FILE(GLOB packing_c "../../packing/*.c")
FILE(GLOB log_c "../../log/*.c")
FILE(GLOB config_c "../../config/*.c")

# targets
ADD_LIBRARY (wt STATIC ${sources_c} ${support_c} ${cursor_c} ${packing_c} ${log_c} ${config_c})