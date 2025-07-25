include(BuildVeyonApplication)

build_veyon_application(veyon-configurator
	NAME Configurator
	WINDOWS_ICON "data/veyon-configurator.ico"
	REQUIRE_ADMINISTRATOR_PRIVILEGES
	SOURCES
	src/AccessControlPage.cpp
	src/AccessControlPage.h
	src/AccessControlPage.ui
	src/AccessControlRuleEditDialog.cpp
	src/AccessControlRuleEditDialog.h
	src/AccessControlRuleEditDialog.ui
	src/AccessControlRuleListModel.cpp
	src/AccessControlRuleListModel.h
	src/AccessControlRulesTestDialog.cpp
	src/AccessControlRulesTestDialog.h
	src/AccessControlRulesTestDialog.ui
	src/AuthenticationPage.cpp
	src/AuthenticationPage.h
	src/AuthenticationPageTab.cpp
	src/AuthenticationPageTab.h
	src/AuthenticationPageTab.ui
	src/AuthenticationPage.ui
	src/GeneralConfigurationPage.cpp
	src/GeneralConfigurationPage.h
	src/GeneralConfigurationPage.ui
	src/main.cpp
	src/MainWindow.cpp
	src/MainWindow.h
	src/MainWindow.ui
	src/MasterConfigurationPage.cpp
	src/MasterConfigurationPage.h
	src/MasterConfigurationPage.ui
	src/NetworkObjectDirectoryConfigurationPage.cpp
	src/NetworkObjectDirectoryConfigurationPage.h
	src/NetworkObjectDirectoryConfigurationPage.ui
	src/NetworkObjectDirectoryConfigurationPageTab.cpp
	src/NetworkObjectDirectoryConfigurationPageTab.h
	src/NetworkObjectDirectoryConfigurationPageTab.ui
	src/ServiceConfigurationPage.cpp
	src/ServiceConfigurationPage.h
	src/ServiceConfigurationPage.ui
	resources/configurator.qrc)

if(VEYON_BUILD_LINUX)
	xdg_install(${CMAKE_CURRENT_BINARY_DIR}/data/veyon-configurator.desktop ${CMAKE_CURRENT_SOURCE_DIR}/data/veyon-configurator.xpm ${CMAKE_CURRENT_SOURCE_DIR}/data/veyon-configurator.png ${CMAKE_CURRENT_SOURCE_DIR}/data/veyon-configurator.svg)
	install(FILES ${CMAKE_CURRENT_BINARY_DIR}/data/io.veyon.veyon-configurator.policy DESTINATION ${CMAKE_INSTALL_PREFIX}/share/polkit-1/actions)
endif()
