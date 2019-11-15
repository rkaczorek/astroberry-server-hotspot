cmake_minimum_required(VERSION 2.8)
PROJECT(astroberry-server-hotspot NONE)

set (VERSION_MAJOR 2)
set (VERSION_MINOR 0)
set (VERSION_RELEASE 0)

set(NM_CONFIG_DIR "/etc/NetworkManager")

if (${CMAKE_SYSTEM_NAME} MATCHES "Linux")
	install(FILES ${CMAKE_CURRENT_SOURCE_DIR}/HotSpot.nmconnection DESTINATION ${NM_CONFIG_DIR}/system-connections)
	install(FILES ${CMAKE_CURRENT_SOURCE_DIR}/wifi-powersave-off.conf DESTINATION ${NM_CONFIG_DIR}/conf.d)
        install(FILES ${CMAKE_CURRENT_SOURCE_DIR}/wifi-enable-autohotspot.conf DESTINATION ${NM_CONFIG_DIR}/conf.d)
endif()
