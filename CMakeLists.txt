find_package(Threads REQUIRED)

add_library(mps code/mps.c)
target_include_directories(mps PUBLIC code)
target_link_libraries(mps Threads::Threads)
