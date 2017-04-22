#=============================================================================#
# Author: QueezyTheGreat                                                      #
# Date:   26.04.2011                                                          #
#                                                                             #
# Description: Arduino CMake example                                          #
#                                                                             #
#=============================================================================#
set(ARDUINO_SDK_PATH /Applications/Arduino.app/Contents/Java/)
link_directories(${ARDUINO_SDK_PATH}/hardware/arduino/avr/libraries)

set(CMAKE_TOOLCHAIN_FILE cmake/ArduinoToolchain.cmake) # Arduino Toolchain


cmake_minimum_required(VERSION 2.8)
#====================================================================#
#  Setup Project                                                     #
#====================================================================#
project(ArduinoExample C CXX)

print_board_list()
print_programmer_list()

add_subdirectory(example)   #add the example directory into build
