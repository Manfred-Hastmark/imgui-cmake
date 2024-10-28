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
        imgui/backends
)

target_sources(imgui
    PRIVATE
        imgui/imgui.cpp
        imgui/imgui_draw.cpp
        imgui/imgui_tables.cpp
        imgui/imgui_widgets.cpp
        imgui/backends/imgui_impl_glfw.cpp
        imgui/backends/imgui_impl_opengl3.cpp
)

