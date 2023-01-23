find_package(wrt-acc REQUIRED)
find_package(wrt-serial REQUIRED)

add_executable(revlights main.cpp)
target_link_libraries(revlights PRIVATE wrt::acc wrt::serial)
install(TARGETS revlights)
