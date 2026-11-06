# LineageOS 24.0: nAa-mist canonical manifest

Use `manifests/mist-sm4450.xml` as a local manifest in a **separate**
LineageOS 24.0 source checkout. Inspect for path collisions with existing
`.repo/local_manifests` first.

| Checkout path | Repository | Import status |
| --- | --- | --- |
| `device/xiaomi/mist` | [nAa-mist/device_xiaomi_mist](https://github.com/nAa-mist/device_xiaomi_mist) | Active device code |
| `vendor/xiaomi/mist` | [nAa-mist/vendor_xiaomi_mist](https://github.com/nAa-mist/vendor_xiaomi_mist) | Mist-only scaffold; no blobs |
| `device/xiaomi/sm4450-common` | [nAa-mist/device_xiaomi_sm4450-common](https://github.com/nAa-mist/device_xiaomi_sm4450-common) | 57 pinned upstream files verified |
| `vendor/xiaomi/sm4450-common` | [nAa-mist/vendor_xiaomi_sm4450-common](https://github.com/nAa-mist/vendor_xiaomi_sm4450-common) | Empty binary/vendor makefile scaffold |
| `kernel/xiaomi/sm4450` | [xiaomi-ravelin/android_kernel_xiaomi_sm4450](https://github.com/xiaomi-ravelin/android_kernel_xiaomi_sm4450) | **Temporary** core source; mist upload pending |
| `kernel/xiaomi/sm4450-modules` | [nAa-mist/kernel_xiaomi_sm4450-modules](https://github.com/nAa-mist/kernel_xiaomi_sm4450-modules) | 8,966 pinned upstream files imported |
| `kernel/xiaomi/sm4450-devicetrees` | [nAa-mist/kernel_xiaomi_sm4450-devicetrees](https://github.com/nAa-mist/kernel_xiaomi_sm4450-devicetrees) | 7,026 pinned upstream files imported |

Additional mist source destination: [nAa-mist/kernel_xiaomi_mist](https://github.com/nAa-mist/kernel_xiaomi_mist), awaiting user-uploaded actual `mist` kernel source. The [nAa-mist/kernel_xiaomi_sm4450](https://github.com/nAa-mist/kernel_xiaomi_sm4450) repository is currently documentation only and is **not** in the sync manifest.

Source pins are full commit SHAs for reproducibility. The device repo pins itself to `main` to avoid an impossible self-referential commit SHA. When a dependency is changed, update its pin **here in the device repository**.

All research belongs to [nAa-mist/mist-bringup](https://github.com/nAa-mist/mist-bringup). Do not sync that research archive as a device source. No firmware or proprietary binaries are bundled.

**Not ready to build or flash a ROM:** vendor extraction, exact hardware SKU, kernel, init, AVB, SELinux and real-device testing remain pending.
