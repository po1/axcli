cmake_minimum_required(VERSION 2.8.3)
project(axcli)

find_package(catkin REQUIRED)

catkin_package()

catkin_add_env_hooks(20.axcli SHELLS bash DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/env-hooks)

install(PROGRAMS
  bin/axcli
  DESTINATION ${CATKIN_GLOBAL_BIN_DESTINATION}
)

# generate relay-script for each program
set(EXECUTABLE ${CMAKE_CURRENT_SOURCE_DIR}/bin/axcli)
configure_file(${catkin_EXTRAS_DIR}/templates/script.sh.in
  ${CATKIN_DEVEL_PREFIX}/${CATKIN_GLOBAL_BIN_DESTINATION}/axcli
  @ONLY)
