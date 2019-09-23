cmake_minimum_required(VERSION 2.8.3)
project(wired)

#set(CMAKE_BUILD_TYPE "RelWithDebInfo")
#set(CMAKE_BUILD_TYPE Debug)

## Find catkin macros and libraries
find_package(catkin REQUIRED COMPONENTS
  ed
  wire_core
  wire_msgs
)

#find_package(PCL REQUIRED)
#find_package(OpenCV REQUIRED)

# Generate messages in the 'msg' folder
#add_message_files(
#  FILES
#)

# Generate services in the 'srv' folder
#add_service_files(
#  FILES
#)

# Generate added messages and services with any dependencies listed here
#generate_messages(
#  DEPENDENCIES
#)

###################################
## catkin specific configuration ##
###################################
catkin_package(
  INCLUDE_DIRS include
  #LIBRARIES ed_core ed_io
 #   CATKIN_DEPENDS geometry_msgs message_runtime
)

###########
## Build ##
###########

include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)


# ------------------------------------------------------------------------------------------------
#                                          ED CORE
# ------------------------------------------------------------------------------------------------


# ------------------------------------------------------------------------------------------------
#                                               PLUGINS
# ------------------------------------------------------------------------------------------------



# ------------------------------------------------------------------------------------------------
#                                                TOOLS
# ------------------------------------------------------------------------------------------------


# ------------------------------------------------------------------------------------------------
#                                               EXAMPLE PLUGIN
# ------------------------------------------------------------------------------------------------


add_library(ed_mulitple_hypothesis_plugin
  src/multiple_hypothesis_plugin.cpp
)
target_link_libraries(ed_mulitple_hypothesis_plugin ${catkin_LIBRARIES})
#add_dependencies(ed_mulitple_hypothesis_plugin ${${PROJECT_NAME}_EXPORTED_TARGETS})

#add_library(ed_mulitple_hypothesis_plugin src/multiple_hypothesis_plugin.cpp)
#add_library(ed_custom_properties_plugin examples/custom_properties/custom_properties_plugin.cpp)

# ------------------------------------------------------------------------------------------------
#                                                TESTS
# ------------------------------------------------------------------------------------------------