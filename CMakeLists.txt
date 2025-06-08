cmake_minimum_required(VERSION 3.10)
project(lab04 CXX)

# Устанавливаем требуемый стандарт C++ для всего проекта
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_subdirectory(formatter_lib)
add_subdirectory(formatter_ex_lib)
add_subdirectory(solver_lib)
add_subdirectory(hello_world_application)

add_dependencies(hello_world formatter_ex solver)

include(CPackConfig.cmake)
include(CPack)
