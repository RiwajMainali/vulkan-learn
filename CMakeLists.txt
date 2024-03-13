
cmake_minimum_required(VERSION 3.22)
project(vulkan)

# Find the GLFW library
find_package(glfw3 3.3 REQUIRED)
find_package(glm REQUIRED)
find_package(Vulkan REQUIRED)

# Add the include path for Vulkan
include_directories(${Vulkan_INCLUDE_DIRS} ${GLM_INCLUDE_DIRS})

# Define your executable
add_executable(${PROJECT_NAME} main.cpp)

# Link your application with the Vulkan library
target_link_libraries(${PROJECT_NAME} glfw Vulkan::Vulkan)
