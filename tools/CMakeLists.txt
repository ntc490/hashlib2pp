cmake_minimum_required(VERSION 3.16)

add_executable(hello hello.cpp)
add_executable(h h.cpp)
add_executable(libtest libtest.cpp)

target_link_libraries(hello hl++)
target_link_libraries(h hl++)
target_link_libraries(libtest hl++)

# Don't normally include these in installation
# install(TARGETS hello h libtest EXPORT helloTargets
#   RUNTIME DESTINATION bin
#   )
