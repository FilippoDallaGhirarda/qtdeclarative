# Generated from qqmlapplicationengine.pro.

#####################################################################
## tst_qqmlapplicationengine Test:
#####################################################################

# Collect test data
file(GLOB_RECURSE test_data_glob
    RELATIVE ${CMAKE_CURRENT_SOURCE_DIR}
    data/*)
list(APPEND test_data ${test_data_glob})

qt_add_test(tst_qqmlapplicationengine
    SOURCES
        ../../shared/util.cpp ../../shared/util.h
        tst_qqmlapplicationengine.cpp
    INCLUDE_DIRECTORIES
        ../../shared
    PUBLIC_LIBRARIES
        Qt::CorePrivate
        Qt::GuiPrivate
        Qt::Network
        Qt::QmlPrivate
    TESTDATA ${test_data}
)

# Resources:
set(tst_qqmlapplicationengine_resource_files
    "data/i18n/qml.qm"
    "data/loadTranslation.qml"
)

qt_add_resource(tst_qqmlapplicationengine "tst_qqmlapplicationengine"
    PREFIX
        "/"
    FILES
        ${tst_qqmlapplicationengine_resource_files}
)


#### Keys ignored in scope 2:.:.:tst_qqmlapplicationengine.pro:<TRUE>:
# TRANSLATIONS = "data/i18n/qml_ja.ts"

## Scopes:
#####################################################################

qt_extend_target(tst_qqmlapplicationengine CONDITION ANDROID OR IOS
    DEFINES
        QT_QMLTEST_DATADIR=\\\":/data\\\"
)

qt_extend_target(tst_qqmlapplicationengine CONDITION NOT ANDROID AND NOT IOS
    DEFINES
        QT_QMLTEST_DATADIR=\\\"${CMAKE_CURRENT_SOURCE_DIR}/data\\\"
)
add_subdirectory(testapp)
