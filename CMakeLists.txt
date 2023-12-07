cmake_minimum_required(VERSION 3.19)

include(pico_sdk_import.cmake)

project(ADXL335)

pico_sdk_init()

add_executable(ADXL335 ADXL335.c)

pico_enable_stdio_usb(ADXL335 1)
pico_enable_sdio_uart(ADXL335 0)

pico_add_extra_outputs(ADXL335)

target_link_libraries(ADXL335 pico_stdlib hardware_gpio hardware_adc)




