include(BuildVeyonApplication)

build_veyon_application(veyon-service
	NAME Service
	SOURCES
	src/main.cpp)

if(VEYON_BUILD_LINUX)
	configure_file(${CMAKE_CURRENT_SOURCE_DIR}/veyon.service.in ${CMAKE_CURRENT_BINARY_DIR}/veyon.service @ONLY)
	if(NOT SYSTEMD_SERVICE_INSTALL_DIR)
		set(SYSTEMD_SERVICE_INSTALL_DIR /lib/systemd/system)
	endif()
	install(FILES ${CMAKE_CURRENT_BINARY_DIR}/veyon.service DESTINATION ${SYSTEMD_SERVICE_INSTALL_DIR})
endif()
