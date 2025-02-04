cet_make_library(LIBRARY_NAME_VAR libtarget
  SOURCE MarqFitAlg.cxx
)

find_package(OpenMP EXPORT)
if(OPENMP_FOUND)
  target_link_libraries(${libtarget} PUBLIC OpenMP::OpenMP_CXX)
endif(OPENMP_FOUND)

install_headers()
install_fhicl()
install_source()
