cmake_minimum_required(VERSION 3.14)

project(DarthReminder CXX)

set(CMAKE_CXX_STANDARD 17)

find_package(dpp REQUIRED)
find_package(nlohmann_json REQUIRED)

add_executable(DarthReminder  
    src/main.cpp
    src/bot.cpp
)

target_include_directories(DarthReminder PRIVATE include)

target_link_libraries(DarthReminder
    PRIVATE
    dpp
    nlohmann_json::nlohmann_json
)
