cmake_minimum_required(VERSION 3.5)

project(vehicle_gateway_models)

find_package(ament_cmake REQUIRED)

install(
  DIRECTORY
    configs_px4
    models
  DESTINATION
    share/${PROJECT_NAME}/
)

if(BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  ament_lint_auto_find_test_dependencies()
endif()

ament_package()
