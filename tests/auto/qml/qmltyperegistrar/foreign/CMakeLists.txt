# Generated from foreign.pro.

#####################################################################
## foreign Generic Library:
#####################################################################

qt_add_cmake_library(foreign
    STATIC
    SOURCES
        foreign.cpp foreign.h
    PUBLIC_LIBRARIES
        Qt::Core
)
# special case begin
qt_enable_autogen_tool(foreign "moc" ON)
qt6_generate_meta_types_json_file(foreign)
# special case end

#### Keys ignored in scope 1:.:.:foreign.pro:<TRUE>:
# TEMPLATE = "lib"

## Scopes:
#####################################################################
