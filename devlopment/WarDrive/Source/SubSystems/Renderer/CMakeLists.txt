#set the cmake version.
cmake_minimum_required(VERSION 2.8.9)

#set the project name.
project(Renderer)

#Specify the include folder.
include_directories(
Src
Api
../../Thirdparty/SDL/include
../../Testapp/Build/assimp/include
../../Thirdparty/assimp/include
../../Thirdparty/GLM
../InputManager/Api
)

#create a SOURCES parameter, the file(GLOB...) allows for wildcard additions:
file(GLOB SOURCES "Src/*.cpp")

#generate executable from the sources
add_library(RendererLib STATIC ${SOURCES})



