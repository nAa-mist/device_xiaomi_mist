# Integrating the canonical nAa-mist repositories

Paths within a complete LineageOS 24.0 / Android 17 source checkout:

| Project | Repository | Checkout path |
| --- | --- | --- |
| Device | [device_xiaomi_mist](https://github.com/nAa-mist/device_xiaomi_mist) | `device/xiaomi/mist` |
| Mist-only vendor | [vendor_xiaomi_mist](https://github.com/nAa-mist/vendor_xiaomi_mist) | `vendor/xiaomi/mist` |
| Shared SM4450 common | [xiaomi-ravelin/android_device_xiaomi_sm4450-common](https://github.com/xiaomi-ravelin/android_device_xiaomi_sm4450-common) | `device/xiaomi/sm4450-common` |
| SM4450 kernel | xiaomi-ravelin source (pinned in manifest) | `kernel/xiaomi/sm4450` |
| SM4450 modules | xiaomi-ravelin source (pinned in manifest) | `kernel/xiaomi/sm4450-modules` |
| SM4450 device trees | xiaomi-ravelin source (pinned in manifest) | `kernel/xiaomi/sm4450-devicetrees` |
| Shared vendor binaries | to be extracted into `vendor/xiaomi/sm4450-common` | Not provided |

Place `manifests/mist-sm4450.xml` in `.repo/local_manifests/` after verifying
your LineageOS manifest has no duplicate project paths.

Clone the two nAa-mist repositories into their checkout paths. Do not separately
checkout the old `mist-bringup/device/xiaomi/mist` directory.

The `device.mk` file inherits the shared SM4450 common config and optionally
loads `vendor/xiaomi/mist/mist-vendor.mk`; no device-only blobs are extracted yet.

The original history and all stock inspection data stay in
[nAa-mist/mist-bringup](https://github.com/nAa-mist/mist-bringup).
**No firmware is downloaded by the new device preflight.**

This tree has never completed a full ROM compile or real-device boot test.
