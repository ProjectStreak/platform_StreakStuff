# Preparing ProjectStreak for your device

You can always check out our [**device organization**](https://github.com/ProjectStreak-Devices) for reference.

# General stuff

ProjectStreak uses streak_device.mk.

If your device supports cellular data, then set this in streak_device.mk:

```Makefile
# Inherit some common ProjectStreak stuff.
$(call inherit-product, vendor/streak/config/common_full_phone.mk)
```

If it doesn't, then set this in streak_device.mk:

```Makefile
# Inherit some common ProjectStreak stuff.
$(call inherit-product, vendor/streak/config/common.mk)
```

# GApps

We are enforcing GApps by default, however you can do this after lunching your build to build the ROM without GApps:

```bash
export TARGET_BUILD_GAPPS=false
```

# Official status

To mark your build as official, set this in your streak_device.mk:

```Makefile
STREAK_BUILD_TYPE := OFFICIAL
```
