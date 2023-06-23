cmake_minimum_required(VERSION 3.11)
project(MulticastTool)

find_package(Qt4 4.7.2 REQUIRED QtGui QtCore QtXml QtNetwork)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(SOURCES
main.cpp
open_protocol.h
open_protocol.cpp

send_window.h
send_window.cpp

history_window.h
history_window.cpp
)

add_executable(MulticastTool WIN32 ${SOURCES})
target_link_libraries(MulticastTool PUBLIC 
    Qt4::QtCore Qt4::QtXml Qt4::QtGui Qt4::QtNetwork)
