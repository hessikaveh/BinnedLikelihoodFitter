project(Fitter)
cmake_minimum_required(VERSION 2.8)
set (CMAKE_CXX_FLAGS "--std=gnu++0x ${CMAKE_CXX_FLAGS}")

include_directories(/cmsdata3/kaveh/root-6.12.04/blddir/include)
link_directories(/cmsdata3/kaveh/root-6.12.04/blddir/lib)
aux_source_directory(. SRC_LIST)
add_executable(${PROJECT_NAME} ${SRC_LIST})
target_link_libraries(${PROJECT_NAME} -lCore -lRIO -lNet -lHist -lHistPainter -lGraf -lGraf3d -lGpad -lTree -lRint -lPostscript -lMatrix -lPhysics -lMathCore -lThread -lMultiProc -pthread -lm -ldl -rdynamic
)


#target_compile_features(${PROJECT_NAME}  PRIVATE cxx_range_for)
