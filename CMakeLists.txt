cmake_minimum_required(VERSION 3.21)

# project
project(imgui_text_edit)

add_library(imgui_text_edit STATIC ${imgui_text_edit_SOURCE_DIR}/TextEditor.cpp)

target_include_directories(
  imgui_text_edit SYSTEM
  PUBLIC "$<BUILD_INTERFACE:${imgui_text_edit_SOURCE_DIR}>")

target_link_libraries(imgui_text_edit PUBLIC imgui)
