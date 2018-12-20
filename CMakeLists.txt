cmake_minimum_required(VERSION 3.6)

project(duktape)

set(DUKTAPE_SRCS src/duktape.c)

add_library(${PROJECT_NAME} STATIC ${DUKTAPE_SRCS})

install(
   TARGETS ${PROJECT_NAME}
   ARCHIVE DESTINATION lib)

install(FILES "src/duk_config.h" "src/duktape.h"
            DESTINATION ${INSTALL_DESTINATION} 
            )   