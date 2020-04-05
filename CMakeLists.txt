cmake_minimum_required (VERSION 3.1.0)

project( RTWeekend
    VERSION 3.0.0
    LANGUAGES CXX
)

#set to c++11
set (CMAKE_CXX_STANDARD 11)

#Source
set ( COMMON_ALL
    src/common/rtweekend.h
    src/common/ray.h
    src/common/vec3.h
    
)

set ( SOURCE_ONE_WEEKEND
    ${COMMON_ALL}
    src/weekend/hittable.h
    src/weekend/hittable_list.h
    src/weekend/sphere.h
    src/weekend/main.cc
)

#Executables
add_executable(inOneWeekend     ${SOURCE_ONE_WEEKEND})

include_directories(src/common)