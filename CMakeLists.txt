cmake_minimum_required(VERSION 2.8.4)
set(CMAKE_TOOLCHAIN_FILE ${CMAKE_SOURCE_DIR}/cmake/ArduinoToolchain.cmake)
set(PROJECT_NAME arduino_shift_registers)
project(${PROJECT_NAME})

set(${CMAKE_PROJECT_NAME}_BOARD mega)
set(${CMAKE_PROJECT_NAME}_PORT /dev/cu.usbmodem14131)
set(mega.build.mcu atmega2560)
set(mega.upload.protocol wiring)
set(mega.upload.speed 115200)

set(${CMAKE_PROJECT_NAME}_SKETCH arduino_shift_registers.ino)
generate_arduino_firmware(${CMAKE_PROJECT_NAME})
