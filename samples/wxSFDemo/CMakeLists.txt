
file(GLOB SRCS
        *.cpp
        *.h
        GUI.fbp
        Images/*.bmp
        wxSF.rc
        res/*.xpm
)

add_executable(wxSFDemo ${SRCS})

# and for each of your dependent executable/library targets:
target_include_directories(wxSFDemo PRIVATE ${PROJECT_SOURCE_DIR}/include)

target_link_directories(wxSFDemo PRIVATE ${PROJECT_SOURCE_DIR}/lib/)
target_link_libraries(wxSFDemo PRIVATE wxcode__wxsf-${PROJECT_VERSION})
