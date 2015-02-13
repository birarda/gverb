cmake_minimum_required(VERSION 2.8.12.2)

file(GLOB GVERB_SRCS ${CMAKE_CURRENT_SOURCE_DIR}/src/*.c)
file(GLOB GVERB_HEADERS ${CMAKE_CURRENT_SOURCE_DIR}/src/*.h)

add_library(gverb STATIC ${GVERB_SRCS})

install(TARGETS gverb DESTINATION lib)
install(FILES ${GVERB_HEADERS} DESTINATION include/gverb)