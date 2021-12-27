cmake_minimum_required(VERSION 3.10)
project(cuda_operator)

find_package(CUDA QUIET REQUIRED)
set(CUDA_INCLUDE_DIRS /usr/local/cuda-10.2/include)
set(CUDA_LIBRARY_DIRS /usr/local/cuda-10.2/lib64)

set(CMAKE_CXX_STANDARD 11)

include_directories(${CUDA_INCLUDE_DIRS})
link_directories(${CUDA_LIBRARY_DIRS})

cuda_add_executable(cuda_operator main.cu)
