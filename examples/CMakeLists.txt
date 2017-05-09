if(NOT ITK_SOURCE_DIR)
  find_package(ITK REQUIRED COMPONENTS PrincipalComponentsAnalysis)
  include(${ITK_USE_FILE})
else()
  include_directories( ${PrincipalComponentsAnalysis_SOURCE_DIR}/Source )
endif()

ADD_EXECUTABLE(VectorKernelPCA VectorKernelPCA.cxx )
TARGET_LINK_LIBRARIES(VectorKernelPCA ${PrincipalComponentsAnalysis_LIBRARIES})

