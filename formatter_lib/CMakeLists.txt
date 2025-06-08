# formatter_lib/CMakeLists.txt

cmake_minimum_required(VERSION 3.10)
project(formatter CXX) # Добавил CXX

# Устанавливаем требуемый стандарт C++
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_library(formatter STATIC
    formatter.cpp
    # formatter.h  <-- Заголовочные файлы не нужно указывать здесь
)

# Указываем, что заголовочные файлы этой библиотеки доступны публично
# для тех, кто будет линковаться с этой библиотекой.
target_include_directories(formatter PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
