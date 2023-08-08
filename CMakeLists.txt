cmake_minimum_required(VERSION 3.3)
project(imaging_msgs)

set(CMAKE_CXX_STANDARD 14)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(std_msgs REQUIRED)


 rosidl_generate_interfaces(${PROJECT_NAME}
                            msg/HdrImagingMetadata.msg
                            msg/ImagingMetadata.msg
                          DEPENDENCIES
                            std_msgs )

 ament_export_dependencies(rosidl_default_runtime)

 ament_package()
