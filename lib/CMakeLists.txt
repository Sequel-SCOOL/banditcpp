set(CMAKE_BUILD_TYPE Debug)  # Debug or Release. Used for libraries

# Include headers
include_directories("include/sublib1"
                    "include/sublib2")

# Adding sources manually
# set(SOURCES src/mainapp.cpp src/student.cpp)

# Addint all .cpp files as source
# file(GLOB SOURCES "src/*.cpp")  # if there are no subfolders
file(GLOB SOURCES "src/*/*.cpp")

# Generate shared library from the code
add_library(mylib SHARED ${SOURCES})
