cmake_minimum_required(VERSION 3.10)
project(FEM_Solver)

# C++ стандарт
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Пути к заголовочным файлам (Eigen и твои хедеры)
include_directories(
    "${CMAKE_SOURCE_DIR}/include"
    "C:/FEM-COURSEWORK/include"
)

# Исходники программы
add_executable(fem_solver
    main.cpp
)

# Windows настройки
if(WIN32)
    target_compile_definitions(fem_solver PRIVATE _USE_MATH_DEFINES)
endif()

# Вывод информации
message(STATUS "Project: ${PROJECT_NAME}")
message(STATUS "Include directories: ${CMAKE_SOURCE_DIR}/include")
message(STATUS "Compiler: ${CMAKE_CXX_COMPILER}")
