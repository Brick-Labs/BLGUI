add_library(${PROJECT_NAME} STATIC
        Interface.cpp
)

# Namespace-Alias
add_library(Interface::Interface ALIAS Interface)

# Add Include-Path
target_include_directories(Interface
        PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/../include>
        PRIVATE
        ${CMAKE_CURRENT_SOURCE_DIR}
)
