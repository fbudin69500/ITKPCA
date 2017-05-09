cmake_minimum_required(VERSION 3.0)
project(PrincipalComponentsAnalysisExample)

find_package(ITK REQUIRED COMPONENTS PrincipalComponentsAnalysis)
include(${ITK_USE_FILE})

ADD_EXECUTABLE(VectorKernelPCA VectorKernelPCA.cxx )
TARGET_LINK_LIBRARIES(VectorKernelPCA ${ITK_LIBRARIES})
