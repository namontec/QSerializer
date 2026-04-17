#add_compile_definitions(QS_HAS_JSON)

add_library(qserializer STATIC)
find_package(Qt5 COMPONENTS Xml REQUIRED)

target_include_directories(qserializer PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)

target_sources(qserializer
    PUBLIC qserializer.h
)

target_link_libraries(qserializer PUBLIC Qt${QT_VERSION_MAJOR}::Xml)
