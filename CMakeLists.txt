cmake_minimum_required(VERSION 3.13)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
include(pico_sdk_import.cmake)
project(rp2040feather_serprog)

pico_sdk_init()

add_executable(rp2040feather_serprog)
target_sources(rp2040feather_serprog PRIVATE main.c usb_descriptors.c)
target_link_libraries(rp2040feather_serprog PRIVATE pico_stdlib pico_unique_id hardware_spi tinyusb_device)
pico_add_extra_outputs(rp2040feather_serprog)
