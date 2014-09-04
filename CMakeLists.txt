cmake_minimum_required(VERSION 2.8.3)
project(test)

find_package(catkin REQUIRED)

# ------------------------------------------------------------------------------------------------
#                                          CATKIN EXPORT
# ------------------------------------------------------------------------------------------------

catkin_package(
  INCLUDE_DIRS include
  LIBRARIES ANN
)

# ------------------------------------------------------------------------------------------------
#                                              BUILD
# ------------------------------------------------------------------------------------------------

include_directories(
    include
)

add_library(ANN
    src/ANN.cpp
    src/bd_search.cpp 
    src/kd_dump.cpp         
    src/kd_search.cpp 
    src/kd_util.cpp
    src/bd_fix_rad_search.cpp 
    src/bd_tree.cpp   
    src/kd_fix_rad_search.cpp 
    src/kd_split.cpp  
    src/perf.cpp
    src/bd_pr_search.cpp   
    src/brute.cpp  
    src/kd_pr_search.cpp 
    src/kd_tree.cpp
)
