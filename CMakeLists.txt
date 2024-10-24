cmake_minimum_required(VERSION 3.10)

add_library(imgui)
add_library(IMGUI-CMAKE ALIAS imgui)

set_target_properties(imgui
    PROPERTIES
        CXX_STANDARD 11
)

target_include_directories(imgui 
    PUBLIC
        imgui
)

target_sources(imgui
    PRIVATE
        imgui/imgui.cpp
)
