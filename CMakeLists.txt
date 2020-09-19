cmake_minimum_required(VERSION 3.11)
project(udt VERSION 4.11)

add_subdirectory(src)

install(TARGETS udt
    EXPORT udtTargets
    RUNTIME DESTINATION bin
    LIBRARY DESTINATION lib
    ARCHIVE DESTINATION lib
    INCLUDES DESTINATION include)

include(CMakePackageConfigHelpers)

write_basic_package_version_file(udtConfigVersion.cmake
                                 COMPATIBILITY SameMajorVersion)

install(FILES ${CMAKE_CURRENT_BINARY_DIR}/udtConfigVersion.cmake
        DESTINATION lib/cmake/udt)

install(EXPORT udtTargets
        FILE udtConfig.cmake
        NAMESPACE udt::
        DESTINATION lib/cmake/udt)

export(EXPORT udtTargets
       NAMESPACE udt::
       FILE udtConfig.cmake)

export(PACKAGE udt)

