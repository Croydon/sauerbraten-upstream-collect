cmake_minimum_required(VERSION 3.12)
project(sauerbraten)

set(CMAKE_CXX_STANDARD 17)

find_package(PkgConfig REQUIRED)
pkg_search_module(enet REQUIRED IMPORTED_TARGET libenet)
find_package(ZLIB REQUIRED)
find_package(SDL2 REQUIRED)
pkg_search_module(SDL2image REQUIRED IMPORTED_TARGET SDL2_image)
pkg_search_module(SDL2mixer REQUIRED IMPORTED_TARGET SDL2_mixer)

include_directories(engine)
include_directories(fpsgame)
include_directories(shared)
include_directories(${SDL2_INCLUDE_DIRS})

add_executable(sauerbraten
        engine/3dgui.cpp
        engine/bih.cpp
        engine/blend.cpp
        engine/blob.cpp
        engine/client.cpp
        engine/command.cpp
        engine/console.cpp
        engine/cubeloader.cpp
        engine/decal.cpp
        engine/dynlight.cpp
        engine/glare.cpp
        engine/grass.cpp
        engine/lightmap.cpp
        engine/main.cpp
        engine/material.cpp
        engine/menus.cpp
        engine/movie.cpp
        engine/normal.cpp
        engine/octa.cpp
        engine/octaedit.cpp
        engine/octarender.cpp
        engine/physics.cpp
        engine/pvs.cpp
        engine/rendergl.cpp
        engine/rendermodel.cpp
        engine/renderparticles.cpp
        engine/rendersky.cpp
        engine/rendertext.cpp
        engine/renderva.cpp
        engine/server.cpp
        engine/serverbrowser.cpp
        engine/shader.cpp
        engine/shadowmap.cpp
        engine/sound.cpp
        engine/texture.cpp
        engine/water.cpp
        engine/world.cpp
        engine/worldio.cpp
        fpsgame/ai.cpp
        fpsgame/client.cpp
        fpsgame/entities.cpp
        fpsgame/fps.cpp
        fpsgame/monster.cpp
        fpsgame/movable.cpp
        fpsgame/render.cpp
        fpsgame/scoreboard.cpp
        fpsgame/server.cpp
        fpsgame/waypoint.cpp
        fpsgame/weapon.cpp
        shared/crypto.cpp
        shared/geom.cpp
        shared/glemu.cpp
        shared/stream.cpp
        shared/tools.cpp
        shared/zip.cpp)

target_link_libraries(sauerbraten PkgConfig::enet PkgConfig::SDL2image PkgConfig::SDL2mixer ZLIB::ZLIB ${SDL2_LIBRARIES} -lrt -lGL)
