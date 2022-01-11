cmake_minimum_required(VERSION 3.16)

project(CMakeDependentProject)

include(CMake/CPM.cmake)

set(BUILD_JUCE_PROTOTYPE_EXAMPES OFF)
set(BUILD_UNIT_TESTS OFF)

CPMAddPackage("gh:eyalamirmusic/JUCECmakeRepoPrototype#master")

add_subdirectory(Plugins)