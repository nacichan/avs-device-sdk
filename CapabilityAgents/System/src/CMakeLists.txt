add_definitions("-DACSDK_LOG_MODULE=system")

add_library(AVSSystem SHARED
    "${CMAKE_CURRENT_LIST_DIR}/EndpointHandler.cpp"
    "${CMAKE_CURRENT_LIST_DIR}/UserInactivityMonitor.cpp")

target_include_directories(AVSSystem
    PUBLIC "${AVSSystem_SOURCE_DIR}/include")

target_link_libraries(AVSSystem AVSCommon)

# install target
asdk_install()
