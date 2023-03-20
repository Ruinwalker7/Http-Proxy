cmake_minimum_required(VERSION 3.0.2)
project(exam1)

set(libproxy_parse_src src/proxy_parse.c)

INCLUDE_DIRECTORIES(
    "${PROJECT_SOURCE_DIR}/include"
)
add_library(proxy_parse STATIC ${libproxy_parse_src})
# SET_TARGET_PROPERTIES(proxy_parse PROPERTIES CLEAN_DIRECT_OUTPUT 1)

# LINK_DIRECTORIES()
add_executable(proxy   src/proxy.c)
target_link_libraries(proxy proxy_parse)