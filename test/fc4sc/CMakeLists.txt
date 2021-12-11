set(TEST_SOURCES
basic_control_test.cpp
basic_coverpoint_definitions.cpp
basic_cross_bins_filtering.cpp
basic_cross_options_test.cpp
basic_cvg_at_least_test.cpp
basic_cvg_goal_test.cpp
basic_cvg_weight_test.cpp
basic_cvp_at_least_test.cpp
basic_cvp_goal_test.cpp
basic_cvp_sample_condition_test.cpp
basic_cvp_sample_expression_test.cpp
basic_cvp_weight_test.cpp
bin_array_test.cpp
cvg_get_inst_coverage_edge_cases.cpp
cvp_get_bin_hit_count_test.cpp
cvp_get_inst_coverage_edge_cases.cpp
flexible_bin_array_test.cpp
illegal_bin_test.cpp
intervals.cpp
main.cpp
random_test_1.cpp
)

add_executable(test
    ${TEST_SOURCES}
)

target_link_libraries(test SystemC::systemc GTest::gtest)

target_include_directories(test PRIVATE
    ${PROJECT_SOURCE_DIR}/includes)