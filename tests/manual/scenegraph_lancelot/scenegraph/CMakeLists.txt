# Generated from scenegraph.pro.

#####################################################################
## tst_scenegraph Test:
#####################################################################

# Collect test data
list(APPEND test_data "../data")

qt_add_test(tst_scenegraph
    OUTPUT_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/.." # special case
    SOURCES
        ../../../../../qtbase/tests/baselineserver/shared/baselineprotocol.cpp ../../../../../qtbase/tests/baselineserver/shared/baselineprotocol.h
        ../../../../../qtbase/tests/baselineserver/shared/lookup3.cpp
        ../../../../../qtbase/tests/baselineserver/shared/qbaselinetest.cpp ../../../../../qtbase/tests/baselineserver/shared/qbaselinetest.h
        tst_scenegraph.cpp
    DEFINES
        QMAKESPEC=\\\"\\\"
    INCLUDE_DIRECTORIES
        ../../../../../qtbase/tests/baselineserver/shared
    PUBLIC_LIBRARIES
        Qt::Gui
        Qt::Network
    TESTDATA ${test_data}
)

## Scopes:
#####################################################################

#### Keys ignored in scope 3:.:.:scenegraph.pro:WIN32:
# TEST_HELPER_INSTALLS = ".././qmlscenegrabber.exe"

#### Keys ignored in scope 6:.:.:scenegraph.pro:else:
# TEST_HELPER_INSTALLS = ".././qmlscenegrabber"
