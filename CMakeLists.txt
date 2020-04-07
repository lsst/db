cmake_minimum_required(VERSION 3.1)
project(db)

file(GENERATE OUTPUT ${CMAKE_CURRENT_BINARY_DIR}/python/lsst/db/version.py CONTENT "\
__version__ = 'unknown'
__all__ = ('__version__',)
")

install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/python/ DESTINATION ${CMAKE_INSTALL_PREFIX}/python)
install(DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/python/ DESTINATION ${CMAKE_INSTALL_PREFIX}/python)
