cmake_minimum_required(VERSION 2.6)

PROJECT(SpinBoxDelegate)

FIND_PACKAGE(Qt4 REQUIRED)
INCLUDE(${QT_USE_FILE})

QT4_WRAP_CPP(MOCSrcs delegate.h)

include_directories(${include_directories} ${CMAKE_CURRENT_SOURCE_DIR} ${CMAKE_CURRENT_BINARY_DIR})

ADD_EXECUTABLE(SpinBoxDelegate main.cpp
delegate.cpp
${MOCSrcs}
)
TARGET_LINK_LIBRARIES(SpinBoxDelegate ${QT_LIBRARIES})
