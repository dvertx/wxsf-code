file(GLOB SRCS 
        *.cpp
        GUI.fbp
        wxSF.rc
        *.h
        res/*.xpm
        wxxmlserializer/*.cpp
)

add_library(wxcode__wxsf-${PROJECT_VERSION} SHARED ${SRCS})

target_include_directories(wxcode__wxsf-${PROJECT_VERSION} PRIVATE ${PROJECT_SOURCE_DIR}/include)
target_link_libraries(wxcode__wxsf-${PROJECT_VERSION} ${wxWidgets_LIBRARIES})
