# Generated from labsmodels.pro.

#####################################################################
## labsmodelsplugin Plugin:
#####################################################################

qt_add_qml_module(labsmodelsplugin
    URI "Qt.labs.qmlmodels"
    VERSION "${CMAKE_PROJECT_VERSION}"
    CLASSNAME QtQmlLabsModelsPlugin
    SKIP_TYPE_REGISTRATION
    GENERATE_QMLTYPES
    SOURCES
        plugin.cpp
    PUBLIC_LIBRARIES
        Qt::QmlModelsPrivate
        Qt::QmlPrivate
)

#### Keys ignored in scope 1:.:.:labsmodels.pro:<TRUE>:
# CXX_MODULE = "qml"
# QML_IMPORT_VERSION = "$$QT_VERSION"
# TARGETPATH = "Qt/labs/qmlmodels"

## Scopes:
#####################################################################

qt_extend_target(labsmodelsplugin CONDITION QT_FEATURE_qml_table_model
    SOURCES
        qqmltablemodel.cpp qqmltablemodel_p.h
        qqmltablemodelcolumn.cpp qqmltablemodelcolumn_p.h
)

qt_extend_target(labsmodelsplugin CONDITION QT_FEATURE_qml_delegate_model
    SOURCES
        qqmldelegatecomponent.cpp qqmldelegatecomponent_p.h
)
