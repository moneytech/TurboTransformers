add_library(benchmark_helper benchmark_helper.cpp)
target_link_libraries(benchmark_helper tt_kernels tt_core catch2_test_main)

add_executable(activation_benchmark activation_benchmark.cpp)
target_link_libraries(activation_benchmark benchmark_helper)

add_executable(matmul_benchmark matmul_benchmark.cpp)
target_link_libraries(matmul_benchmark benchmark_helper)

add_executable(layernorm_benchmark layernorm_benchmark.cpp)
target_link_libraries(layernorm_benchmark benchmark_helper)

add_executable(softmax_benchmark softmax_benchmark.cpp)
target_link_libraries(softmax_benchmark benchmark_helper)

add_executable(transpose_benchmark transpose_benchmark.cpp)
target_link_libraries(transpose_benchmark benchmark_helper)
