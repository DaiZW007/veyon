include(BuildVeyonPlugin)

build_veyon_plugin(desktopservices
	NAME DesktopServices
	SOURCES
	DesktopServiceObject.cpp
	DesktopServicesConfigurationPage.cpp
	DesktopServicesConfigurationPage.ui
	DesktopServicesFeaturePlugin.cpp
	StartAppDialog.cpp
	StartAppDialog.h
	StartAppDialog.ui
	OpenWebsiteDialog.cpp
	OpenWebsiteDialog.h
	OpenWebsiteDialog.ui
	DesktopServiceObject.h
	DesktopServicesConfiguration.h
	DesktopServicesConfigurationPage.h
	DesktopServicesFeaturePlugin.h
	desktopservices.qrc
	)
