cmake_minimum_required(3.10)

add_library(imgui INTERFACE)
add_library(IMGUI-CMAKE ALIAS imgui)

target_include_directories(imgui 
    PUBLIC
        imgui
)

target_sources(imgui
    PRIVATE
        imgui/imgui.cpp
)
