cmake_minimum_required(VERSION 3.0.0)
project(steam-input-test VERSION 0.1.0)

#include(CTest)
#enable_testing()

list(APPEND CMAKE_MODULE_PATH
  "${CMAKE_SOURCE_DIR}/SteamworksSDKCI/cmake"
  )
add_subdirectory(SteamworksSDKCI/cmake)
find_package(SteamworksSDK REQUIRED)

#include_directories(${CMAKE_CURRENT_SOURCE_DIR}/SteamworksSDK)
#link_directories(${CMAKE_CURRENT_SOURCE_DIR}/SteamworksSDK)

#target_link_libraries(steam-input-test STEAMWORKSSDK::STEAMWORKSSDK)

add_executable(steam-input-test main.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
