project (glabels-batch LANGUAGES CXX)

#=======================================
# Sources
#=======================================
set (glabels-batch_sources
  main.cpp
)

#=====================================
# Target
#=====================================
add_executable (glabels-batch-qt WIN32
  ${glabels-batch_sources}
)

#target_compile_features (glabels-batch-qt
#  PUBLIC cxx_std_11
#)
set_property (TARGET glabels-batch-qt PROPERTY CXX_STANDARD 11)

target_link_libraries (glabels-batch-qt
  Model
)

#=======================================
# Install
#=======================================
install (TARGETS glabels-batch-qt RUNTIME DESTINATION bin)

