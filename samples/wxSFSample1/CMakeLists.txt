file(GLOB SRCS
        *.cpp
        *.h
        wxSF.rc
        res/*.xpm
)

add_executable(wxSFSample1 ${SRCS})

# and for each of your dependent executable/library targets:
target_include_directories(wxSFSample1 PRIVATE ${PROJECT_SOURCE_DIR}/include)

target_link_directories(wxSFSample1 PRIVATE ${PROJECT_SOURCE_DIR}/lib/)
target_link_libraries(wxSFSample1 PRIVATE wxcode__wxsf-${PROJECT_VERSION})
