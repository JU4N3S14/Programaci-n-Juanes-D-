cmake_minimum_required(VERSION 3.16)
project(trabajofinal) #sin comillas y en minúsculas

# 1. Recolecta todos los .cpp (incluyendo main.cpp)
file(GLOB SRC_FILES
    "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp"
    "${CMAKE_CURRENT_SOURCE_DIR}/main.cpp"
)

# 2. Declara el ejecutable
add_executable(trabajofinal ${SRC_FILES}) #Nombre del ejecutable en minúsculas y sin comillas

# 3. Indícale dónde están los headers
target_include_directories(trabajofinal   #nombre del ejecutable en minuscula y sin comillas
  PRIVATE
    "${CMAKE_CURRENT_SOURCE_DIR}/include"
)