cmake_minimum_required(VERSION 3.16.3...3.19.7 FATAL_ERROR)

project(VolumeFlipper)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://www.slicer.org/wiki/Documentation/Nightly/Extensions/VolumeFlipper")
set(EXTENSION_CATEGORY "MeiqiTools")
set(EXTENSION_CONTRIBUTORS "HHX (cad420)")
set(EXTENSION_DESCRIPTION "体数据翻转工具")
set(EXTENSION_ICONURL "https://www.example.com/Slicer/Extensions/VolumeFlipper.png")
set(EXTENSION_SCREENSHOTURLS "https://www.example.com/Slicer/Extensions/VolumeFlipper/Screenshots/1.png")
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(Flipper)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
