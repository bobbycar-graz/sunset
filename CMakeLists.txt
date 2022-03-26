set(headers
        src/sunset.h
        )

set(sources
        src/sunset.cpp
        )

idf_component_register(
        INCLUDE_DIRS
        src
        SRCS
        ${headers}
        ${sources}
)

target_compile_options(${COMPONENT_TARGET}
        PRIVATE
        -fstack-reuse=all
        -fstack-protector-all
        -Wno-unused-function
        -Wno-deprecated-declarations
        -Wno-missing-field-initializers
        -Wno-parentheses
        )



