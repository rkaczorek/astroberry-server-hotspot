cmake_minimum_required(VERSION 2.8)
PROJECT(astroberry-server-hotspot NONE)

set (VERSION_MAJOR 2)
set (VERSION_MINOR 0)
set (VERSION_RELEASE 0)

set(NM_INSTALL_DIR "/etc/NetworkManager/system-connections")

message("=========================================== $ENV{DESTDIR}/${BUILD_ROOT} ==============================================")

if (${CMAKE_SYSTEM_NAME} MATCHES "Linux")
	install(FILES ${CMAKE_CURRENT_SOURCE_DIR}/HotSpot.nmconnection DESTINATION ${NM_INSTALL_DIR})
endif()
