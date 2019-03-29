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

## Files that need to be copied from the Collect edition

```
academy.ogz
academy.wpt
autumn.ogz
autumn.wpt
bt_falls.ogz
bt_falls.wpt
complex.ogz
complex.wpt
core_refuge.ogz
core_refuge.wpt
damnation.ogz
damnation.wpt
flagstone.ogz
flagstone.wpt
frozen.cfg
frozen.ogz
frozen.wpt
garden.ogz
garden.wpt
hallo.ogz
hallo.wpt
island.ogz
island.wpt
masdm.ogz
masdm.wpt
mbt12.ogz
mbt12.wpt
memento.cfg
memento.ogz
memento.wpt
nevil_c.ogz
nevil_c.wpt
nitro.ogz
nitro.wpt
nmp8.ogz
nmp8.wpt
nmp9.ogz
nmp9.wpt
ot.ogz
ot.wpt
phosgene.ogz
phosgene.wpt
shipwreck.ogz
shipwreck.wpt
shiva.ogz
shiva.wpt
subterra.ogz
subterra.wpt
tempest.ogz
tempest.wpt
thetowers.ogz
thetowers.wpt
turbine.ogz
turbine.wpt
```
