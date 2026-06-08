# add_library(gumdrops my_module.c)

target_include_directories(gumdrops 
    PUBLIC 
        ${CMAKE_CURRENT_SOURCE_DIR}/../include
    PRIVATE 
        ${CMAKE_CURRENT_SOURCE_DIR}
)

if(CMAKE_C_COMPILER_ID MATCHES "GNU|Clang")
    target_compile_options(gumdrops PRIVATE -Wall -Wextra -Wpedantic)
endif()