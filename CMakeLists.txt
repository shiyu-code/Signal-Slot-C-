cmake_minimum_required(VERSION 3.16)

project(signal-slot LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(signal-slot main.cpp
    object.h object.cpp
    moc_object.cpp)

include(GNUInstallDirs)
install(TARGETS signal-slot
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
