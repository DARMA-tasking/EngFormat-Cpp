add_executable(test_eng_format lest.hpp test_eng_format.cpp)
target_link_libraries(test_eng_format EngFormat-Cpp)

add_test(test_eng_format test_eng_format)