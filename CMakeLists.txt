cmake_minimum_required(VERSION 3.14)
project(EasyDemo C)

set(CMAKE_C_STANDARD 99)

include_directories(include)

link_directories(lib)

find_package(Threads REQUIRED)

add_executable(EasyDemo main.c)

target_link_libraries(EasyDemo
        # Links the target library to the log library
        # included in the NDK.
        Threads::Threads
        easylogger
        )