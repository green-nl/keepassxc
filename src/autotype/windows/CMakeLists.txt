set(autotype_win_SOURCES
    AutoTypeWindows.cpp
)

add_library(keepassx-autotype-windows MODULE ${autotype_win_SOURCES})
target_link_libraries(keepassx-autotype-windows keepassx_core ${autotype_LIB} Qt5::Core Qt5::Widgets)
install(TARGETS keepassx-autotype-windows
        BUNDLE DESTINATION . COMPONENT Runtime
LIBRARY DESTINATION ${PLUGIN_INSTALL_DIR} COMPONENT Runtime)
