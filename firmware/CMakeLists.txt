
cmake_minimum_required(VERSION 2.8)

set(CMAKE_TOOLCHAIN_FILE cmake/ArduinoToolchain.cmake)

project(Scorpion C CXX)

set(ARDUINO_DEFAULT_BOARD diecimila) # Default Board ID, when not specified
set(ARDUINO_DEFAULT_PORT /dev/ttyUSB0) # Default Port, when not specified

#set(blink_SRCS blink.cpp)
#set(blink_LIBS blink_lib)
#set(blink_BOARD uno)
#
#generate_arduino_firmware(blink)

#generate_arduino_firmware(blink
#    SRCS main.cpp
#    BOARD uno)

set(blink_SRCS  main.cpp)
#set(blink_HDRS  blink.h)
set(blink_BOARD uno)

generate_arduino_firmware(blink)
