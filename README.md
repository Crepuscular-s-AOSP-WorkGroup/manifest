# Crepuscular's AOSP Project

Only for msm8953 platform ( for a little while )

## Getting Started

To init the local repo. 

```
repo init -u https://github.com/Crepuscular-s-AOSP-WorkGroup/manifest.git -b 12.1

```

Using depth=1 to reduce the storage

```
repo init --depth=1 -u https://github.com/Crepuscular-s-AOSP-WorkGroup/manifest.git -b 12.1
```

To sync the source tree

```
repo sync --current-branch --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j `nproc`
```

## Build

Build with PixelExperience tree

```
. build/envsetup.sh

lunch aosp_<device>-< eng | userdebug >

m bacon -j$(nproc -all)
```
