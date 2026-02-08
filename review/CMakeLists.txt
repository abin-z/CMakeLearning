cmake_minimum_required(VERSION 3.15)

project(TestExe VERSION 0.1.2)

add_executable(TestExe tutorial.cxx)

set(MathFunctions_DIR E:/projects/CMakeLearning/cmake-3.31.11-tutorial-source/Step11/install/lib/cmake/MathFunctions)

find_package(MathFunctions REQUIRED)

# target_include_directories(TestExe PRIVATE "${MathFunctions_DIR}/include")
# target_link_directories(TestExe PRIVATE "${MathFunctions_DIR}/lib")
# target_link_directories(TestExe PRIVATE "${MathFunctions_DIR}/bin")

# link libraries
target_link_libraries(TestExe PRIVATE MathFunctions)