cmake_minimum_required(VERSION 3.6)

project(duktape)

set(DUKTAPE_SRCS src/duktape.c)

add_library(${PROJECT_NAME} STATIS ${DUKTAPE_SRCS})

install(
   TARGETS ${PROJECT_NAME}
   ARCHIVE DESTINATION lib
   )

install(FILES "duk_config.h" "duktape.h"
            DESTINATION ${INSTALL_DESTINATION} 
            )   