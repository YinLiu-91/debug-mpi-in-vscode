cmake_minimum_required(VERSION 3.11)

project(mpiTutorial)

find_package(MPI) 

set( CMAKE_BUILD_TYPE "Debug")


# include_directories("/usr/lib/x86_64-linux-gnu/openmpi/include")
include_directories(SYSTEM ${MPI_INCLUDE_PATH})


add_executable(hello-mpi hello-mpi.cpp)


target_link_libraries(hello-mpi ${MPI_CXX_LIBRARIES}) # this must be  MPI_CXX_LIBRARIES for cpp file