include(BuildVeyonPlugin)

build_veyon_plugin(filetransfer
	NAME FileTransfer
	SOURCES
	FileTransferPlugin.cpp
	FileTransferPlugin.h
	FileTransferConfiguration.h
	FileTransferConfigurationPage.cpp
	FileTransferConfigurationPage.h
	FileTransferConfigurationPage.ui
	FileTransferController.cpp
	FileTransferController.h
	FileTransferListModel.cpp
	FileTransferListModel.h
	FileTransferDialog.cpp
	FileTransferDialog.h
	FileTransferDialog.ui
	FileTransferUserConfiguration.h
	FileReadThread.cpp
	FileReadThread.h
	filetransfer.qrc
	)
