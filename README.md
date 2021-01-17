# Hackintosh EFI for ASUS ROG Strix TRX40-E

- Mobo: ASUS ROG Strix TRX40-E Gaming
- CPU: AMD Ryzen Threadripper 3970x
- GPU: Sapphire NITRO+ RX 5700 XT
- RAM: CORSAIR VENGEANCE RGB PRO 16GB x 4 (3200)
- SSD: Samsung SSD 970 EVO Plus 500GB x 2
- Cooler: CORSAIR Hydro Series H115i PRO RGB 280mm
  - Cooler's USB port is disabled in `SSDT-USB-Mapping.aml` to work with sleeping
- Display: LG 27GN950-B / DELL U2417H / Samsung U28E850
- Extra Network Card: Fenvi BCM94360CD

Geekbench result: [1207 single-core, 25169 multi-core](https://browser.geekbench.com/v5/cpu/5450605). Faster than the most expensive [28-core Mac Pro](https://browser.geekbench.com/macs/mac-pro-late-2019-intel-xeon-w-3275m-2-5-ghz-28-cores)!

## What works

- Big Sur 11.1
- iServices (iMessage / FaceTime / etc.)
- [Continuity](https://support.apple.com/en-us/HT204681) (except Auto Unlock / Sidecar / Apple Pay)
- Sleep / Wake
- Windows / macOS dual boot
- Onboard 2.5G LAN (RTL8125)
- HDMI / DP Audio
- Multi-monitor setup

## What does not work

- Gracefully shutdown (will reboot instantly after shutdown)
- Onboard Realtek USB Audio (the sound is distorted)
- Apple Hypervisor (Docker for Mac, Parallels etc.) / Adobe ([patches](https://gist.github.com/naveenkrdy/26760ac5135deed6d0bb8902f6ceb6bd) available, but I don't use Adobe products)
- Auto Unlock (can be enabled in System Preferences but actually doesn't work)
- Sidecar (but we can use [Duet Display](https://www.duetdisplay.com/) as an alternative)
- Apple Pay (doesn't work with all Hackintoshes)
- 4K 144Hz ([a common issue in Big Sur](https://egpu.io/forums/mac-setup/4k144hz-no-longer-available-after-upgrade-to-big-sur/). 27GN950-B can only use up to 4K 95Hz without DSC)

## References

- [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [TRX40 Bare Metal discussions on macos86.it (specially, the post by _iGPU_ about how to get NVRAM working)](https://www.macos86.it/topic/3307-trx40-bare-metal-vanilla-patches-yes-it-worksbutproxmox-is-better/page/7/?tab=comments#comment-82868)
