# Set env for build toolchain
```
export PATH=/mnt/e/tomato/zephyr-sdk-0.13.1/arm-zephyr-eabi/bin/:$PATH
```

# Download code
```
git https://github.com/madmachineio/FreeType.git
```

# Build
```
cd FreeType/
mkdir build/
cd build/
cmake -D CMAKE_INSTALL_PREFIX=$PWD/INSTALL -D CMAKE_DISABLE_FIND_PACKAGE_ZLIB=TRUE -D CMAKE_DISABLE_FIND_PACKAGE_BZip2=TRUE -D CMAKE_DISABLE_FIND_PACKAGE_PNG=TRUE -D CMAKE_DISABLE_FIND_PACKAGE_HarfBuzz=TRUE -D CMAKE_DISABLE_FIND_PACKAGE_BrotliDec=TRUE ../
make -j
```

# Export lib
```
make install
```
Will create INSTALL folder in build/
```
.
├── include
│   └── freetype2
│       ├── dlg
│       │   ├── dlg.h
│       │   └── output.h
│       ├── freetype
│       │   ├── config
│       │   │   ├── ftconfig.h
│       │   │   ├── ftheader.h
│       │   │   ├── ftmodule.h
│       │   │   ├── ftoption.h
│       │   │   ├── ftstdlib.h
│       │   │   ├── integer-types.h
│       │   │   ├── mac-support.h
│       │   │   └── public-macros.h
│       │   ├── freetype.h
│       │   ├── ftadvanc.h
│       │   ├── ftbbox.h
│       │   ├── ftbdf.h
│       │   ├── ftbitmap.h
│       │   ├── ftbzip2.h
│       │   ├── ftcache.h
│       │   ├── ftchapters.h
│       │   ├── ftcid.h
│       │   ├── ftcolor.h
│       │   ├── ftdriver.h
│       │   ├── fterrdef.h
│       │   ├── fterrors.h
│       │   ├── ftfntfmt.h
│       │   ├── ftgasp.h
│       │   ├── ftglyph.h
│       │   ├── ftgxval.h
│       │   ├── ftgzip.h
│       │   ├── ftimage.h
│       │   ├── ftincrem.h
│       │   ├── ftlcdfil.h
│       │   ├── ftlist.h
│       │   ├── ftlogging.h
│       │   ├── ftlzw.h
│       │   ├── ftmac.h
│       │   ├── ftmm.h
│       │   ├── ftmodapi.h
│       │   ├── ftmoderr.h
│       │   ├── ftotval.h
│       │   ├── ftoutln.h
│       │   ├── ftparams.h
│       │   ├── ftpfr.h
│       │   ├── ftrender.h
│       │   ├── ftsizes.h
│       │   ├── ftsnames.h
│       │   ├── ftstroke.h
│       │   ├── ftsynth.h
│       │   ├── ftsystem.h
│       │   ├── fttrigon.h
│       │   ├── fttypes.h
│       │   ├── ftwinfnt.h
│       │   ├── t1tables.h
│       │   ├── ttnameid.h
│       │   ├── tttables.h
│       │   └── tttags.h
│       └── ft2build.h
└── lib
    ├── cmake
    │   └── freetype
    │       ├── freetype-config-noconfig.cmake
    │       ├── freetype-config-version.cmake
    │       └── freetype-config.cmake
    ├── libfreetype.a
    └── pkgconfig
        └── freetype2.pc
```