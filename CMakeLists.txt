## linux ou windows + wsl ubuntu apenas
## por favor não tentem com mingw ou msvc (compiladores do windows)

cmake_minimum_required(VERSION 3.2)
project(Autocomplete)

include(./ncurses.cmake)

#com ncurses
add_executable(extra
               src/main.cpp)
target_include_directories(extra
                           ./include
                           ${NCURSES_INCLUDES}/ncurses)
target_link_libraries(extra ncurses)


#sem ncurses
add_executable(words_complete_correct
               src/main.cpp
              )
target_include_directories(basico 
                           ./include)

