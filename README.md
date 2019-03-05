Sauerbraten SVN head, with patches to compile on CMake and to connect to Collect servers.

Dependencies are zlib, SDL2, SDL2-mixer, SDL2-image, enet (yes it's in distro repos), some OpenGL provider (libglvnd-devel in Fedora):
```
git clone https://github.com/pisto/sauerbraten-upstream-collect.git
cd sauerbraten-upstream-collect
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
# cd into SVN head and launch build/sauerbraten from there
```
