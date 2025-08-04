add_library(${PROJECT_NAME} STATIC
        BLGUI.cpp
)

# Namespace-Alias
add_library(BLGUI::BLGUI ALIAS BLGUI)

# Add Include-Path
target_include_directories(BLGUI
        PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/../include>
        PRIVATE
        ${CMAKE_CURRENT_SOURCE_DIR}
)
