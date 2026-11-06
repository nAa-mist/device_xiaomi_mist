# Migration audit and original commit history

The original `nAa-mist/mist-bringup` repository retains the complete
original Git history **unchanged**. This device repository replays **all eight**
source commits that directly changed `device/xiaomi/mist`, in their original
chronological order, and then copies the device validation scripts and manifest.
Original source SHAs are recorded in the replay commit messages. Because the
repo root and Git parent graph changed, replayed commits have different SHAs.

The vendor initial commit is separately replayed to
[nAa-mist/vendor_xiaomi_mist](https://github.com/nAa-mist/vendor_xiaomi_mist).

## Every original mist-bringup commit (chronological)

| Original commit | Change |
| --- | --- |
| [`bf3cd94b7`](https://github.com/nAa-mist/mist-bringup/commit/bf3cd94b72be7d6c38b4d37ea29ffc899d3b608c) | Initialize mist LineageOS research repository |
| [`2b6d0953f`](https://github.com/nAa-mist/mist-bringup/commit/2b6d0953fc8d59d4218fdaafbd8b25d19c318918) | Add validated firmware-inspection workflow and mist bring-up structure |
| [`bb72dacd2`](https://github.com/nAa-mist/mist-bringup/commit/bb72dacd2182d04d8cb3650d201ab11f1bb8f62b) | Speed up firmware download with aria2 parallel segments and checksum-safe retries |
| [`fd7b9dc9f`](https://github.com/nAa-mist/mist-bringup/commit/fd7b9dc9f92e8242104a6f59cb807419e135d0e6) | Benchmark Xiaomi CDN ranges and smaller recovery source before another full transfer |
| [`73e3ee390`](https://github.com/nAa-mist/mist-bringup/commit/73e3ee390044d313da9a449af34057e8be2d29a6) | Benchmark Singapore Alibaba OSS and extra Xiaomi CDN hosts for mist firmware |
| [`c0fd061b6`](https://github.com/nAa-mist/mist-bringup/commit/c0fd061b6693ae80aaa3f1ababd66dceef172e35) | Use fastest tested mist ROM CDN, with Singapore fallback and MD5 verification |
| [`2614acdeb`](https://github.com/nAa-mist/mist-bringup/commit/2614acdeb65a11c2373033c94bac398404248a6e) | Start mist LineageOS device skeleton and verified sparse-super partition research |
| [`8b9fb5828`](https://github.com/nAa-mist/mist-bringup/commit/8b9fb5828fc5dbe481011043e66babce77c44309) | Correct filesystem signature byte literals in stage-two inspector |
| [`9b4230ecf`](https://github.com/nAa-mist/mist-bringup/commit/9b4230ecfe95a10d66c24a5e479d4527b2568e7e) | Add bounded mirror selection and reusable single-download firmware preparation |
| [`a6e92cbe5`](https://github.com/nAa-mist/mist-bringup/commit/a6e92cbe5cf2cc9be206e6cca0dc725eb18d2a0f) | Analyze all mist EROFS partitions, VINTF, init, module configs and boot ramdisks |
| [`eb96970aa`](https://github.com/nAa-mist/mist-bringup/commit/eb96970aaec9376a78ea5863fd24edf303df381e) | Launch consolidated mist bring-up with automatic mirror selection and partition cache |
| [`15b00bb67`](https://github.com/nAa-mist/mist-bringup/commit/15b00bb671a17e4decf9bfbdf503aab0b62373e4) | Prepare LineageOS extraction scaffold and bring-up tree import helper |
| [`80232373f`](https://github.com/nAa-mist/mist-bringup/commit/80232373fa1bf6c2fef5ccc951b94fa3bc94cbeb) | Document LineageOS 24.0 SM4450 common-tree compatibility checks for mist |
| [`6cb67109c`](https://github.com/nAa-mist/mist-bringup/commit/6cb67109c0c2732df84633ffac671b961be54435) | Record verified mist-specific references in SM4450 common lineage-24.0 tree |
| [`ced64f5dc`](https://github.com/nAa-mist/mist-bringup/commit/ced64f5dcb8a50d0b8d2fef1c9d3c0bf87240e29) | Stop redundant firmware download runs and auto-publish verified metadata from consolidated workflow |
| [`46d6ff479`](https://github.com/nAa-mist/mist-bringup/commit/46d6ff479439e3445f088f31e3e34380a8dd1609) | Publish verified mist stock bring-up inventory |
| [`fdf1ca3e0`](https://github.com/nAa-mist/mist-bringup/commit/fdf1ca3e0b0d26d35ba0f3878de030821cfd15cd) | Rerun bounded Xiaomi mirror speed check before considering firmware artifact upload |
| [`fb0c27bae`](https://github.com/nAa-mist/mist-bringup/commit/fb0c27bae62eb2db1c6e8765895ea5d94c4b3f3d) | Match 903 mist Global proprietary paths against LineageOS SM4450 reference and add dependency manifest |
| [`be2a42202`](https://github.com/nAa-mist/mist-bringup/commit/be2a422026bfb32a59782859a3ecf044c02892b7) | Verify mist stock-derived BoardConfig and 903 proprietary entries offline without firmware download |
| [`bf36d4608`](https://github.com/nAa-mist/mist-bringup/commit/bf36d4608ab69346bd8e486bf05349b606b66bc5) | Audit 92 unresolved mist proprietary paths using saved EROFS cache only |
| [`3c0403772`](https://github.com/nAa-mist/mist-bringup/commit/3c04037728d21ea2a54bf45832ac727e58e8c18b) | Record verified stock symlink reconciliation |
| [`b1ecf6f10`](https://github.com/nAa-mist/mist-bringup/commit/b1ecf6f105c3625ef1e227defc53342beea5c8a4) | Resolve all 995 mist stock proprietary paths using cached EROFS audit |
| [`fefebb928`](https://github.com/nAa-mist/mist-bringup/commit/fefebb9285588c196898b1617d7bb9a5aeddefa0) | Integrate verified mist BoardConfig with pinned SM4450 common tree and run one consolidated source preflight |
| [`92f781f2f`](https://github.com/nAa-mist/mist-bringup/commit/92f781f2f018272131410adb25c6cc18a1ce9a52) | Fix stale direct-platform assertion; platform is inherited from pinned common BoardConfig |
| [`07a4d63bd`](https://github.com/nAa-mist/mist-bringup/commit/07a4d63bd89649474b5c0d41a32bf340dcce49de) | Audit mist kernel load deltas, stock F2FS/AVB and VINTF choices together without firmware download |
| [`fb26242aa`](https://github.com/nAa-mist/mist-bringup/commit/fb26242aa2a0ed1d847cbdaa4b9f0074c95da0d3) | Publish one-pass mist hardware audit |
| [`371f06fdb`](https://github.com/nAa-mist/mist-bringup/commit/371f06fdb6d8a1ffb681b1875a5fa37719481a07) | Implement mist-specific VINTF and eliminate duplicate vendor blob extraction ownership |
| [`7c37022c3`](https://github.com/nAa-mist/mist-bringup/commit/7c37022c3ccb80c972067e18d3bd12ca1c15b4af) | Publish one-pass mist hardware audit |

## Ownership after migration

- `device_xiaomi_mist`: the eight original device revisions, full current device tree, verification/test tools and the SM4450 dependency manifest.
- `vendor_xiaomi_mist`: original vendor README and the mist-only vendor skeleton.
- `mist-bringup`: all historical research, firmware testing workflows, stock metadata and reports. **No code history was erased.**

No additional Git repositories have yet been created for the shared SM4450 common/kernel/modules/device-tree source.
