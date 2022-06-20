cmake_minimum_required(VERSION 3.20)
project(qtlocation)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
find_package(Qt5 COMPONENTS Widgets Qml Quick REQUIRED)
qt5_add_resources(qml_QRC qml.qrc)
add_executable(qtlocation main.cpp ${qml_QRC})
target_link_libraries(qtlocation PRIVATE
    Qt5::Widgets
    Qt5::Qml
    Qt5::Quick
)
