cmake_minimum_required(VERSION 3.11)
project(Imported)

include(FetchContent)

FetchContent_Declare(
  ImpoterLibTest
  GIT_REPOSITORY https://github.com/bog-dan-ro/cmake-imported-lib.git
  GIT_TAG master
)
FetchContent_MakeAvailable(ImpoterLibTest)

add_executable(Imported main.c)
target_link_libraries(Imported MyLib::Static)
