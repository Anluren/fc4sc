# list(APPEND FIR_SOURCES display.cpp  fir.cpp  main.cpp  stimulus.cpp)
set(FIR_SOURCES display.cpp  fir.cpp  main.cpp  stimulus.cpp)
add_executable(fir
    ${FIR_SOURCES}
)

target_link_libraries(fir SystemC::systemc)

target_include_directories(fir PRIVATE
    ${PROJECT_SOURCE_DIR}/includes)