target_sources(mavsdk
    PRIVATE
    ftp.cpp
    ftp_impl.cpp
    fs.cpp
    crc32.cpp
)

target_include_directories(mavsdk PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:include>
    )

install(FILES
    include/plugins/ftp/ftp.h
    DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/mavsdk/plugins/ftp
)
