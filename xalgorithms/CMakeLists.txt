set(source_files
    )

set (test_files
    )

add_library(xalgorithms ${source_files})

target_include_directories(xalgorithms PUBLIC ./include)

add_executable(xalgorithms_test
    ${test_files}
    )

target_link_libraries(xalgorithms_test PRIVATE Catch2::Catch2WithMain)
target_link_libraries(xalgorithms_test PRIVATE xalgorithms)
