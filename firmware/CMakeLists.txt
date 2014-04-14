cmake_minimum_required(VERSION 2.8)

set(CMAKE_TOOLCHAIN_FILE ${CMAKE_SOURCE_DIR}/arduino-cmake/cmake/ArduinoToolchain.cmake)

set(ARDUINO_DEFAULT_BOARD uno) # Default Board ID, when not specified
set(ARDUINO_DEFAULT_PORT /dev/ttyUSB0) # Default Port, when not specified

#set(ARDUINO_C_FLAGS      "-ffunction-sections -fdata-sections")
#set(ARDUINO_CXX_FLAGS    "${ARDUINO_C_FLAGS} -fno-exceptions")
#set(ARDUINO_LINKER_FLAGS "-Wl,--gc-sections")

project(Scorpion C CXX)

set(scorpion_SRCS  main.cpp)
# set(scorpion_HDRS  main.h)
set(scorpion_BOARD uno)

generate_arduino_firmware(scorpion)
