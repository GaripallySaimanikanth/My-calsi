# For more information about using CMake with Android Studio, read the
# documentation: https://d.android.com/studio/projects/add-native-code.html

cmake_minimum_required(VERSION 3.18.1)

project("mycalsi")

add_library( # Sets the name of the library.
        mycalsi
        SHARED
        native-lib.cpp)

find_library( # Sets the name of the path variable.
        log-lib
        log)
target_link_libraries( # Specifies the target library.
        mycalsi

        ${log-lib})