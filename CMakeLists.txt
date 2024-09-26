cmake_minimum_required(VERSION 3.0)

project(rlImgui)

add_library(
    ${PROJECT_NAME}
    STATIC
    rlImGui.cpp
)

target_include_directories(
    ${PROJECT_NAME}
    PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)

target_compile_definitions(rlImGui PUBLIC NO_FONT_AWESOME)

target_link_libraries(
    ${PROJECT_NAME}
    PUBLIC
    imgui
    raylib
)