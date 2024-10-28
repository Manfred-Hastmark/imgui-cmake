CMake support for ImGui
=======================

The actual [ImGui repository](https://github.com/ocornut/imgui) is referred as a
submodule. The submodule tracks the docking branch of the
[ImGui repo](https://github.com/ocornut/imgui) which means it's still tied to a specific
commit but it's easier to update. So you can always execute:

```shell
git submodule update --remote
```

to get the latest commits before configuring/installing the library.

Usage:
------

Add the directory to this repository to your CMakeLists.txt 
and then add imgui to your target.

```cmake
add_subdirectory(${PATH_TO_REPO}/imgui-cmake)
target_link_libraries(<target> <PRIVATE|PUBLIC|INTERFACE> imgui)
```
