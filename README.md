# Hackintosh EFI for ROG Strix TRX40-E

- Mobo: ROG Strix TRX40-E Gaming
- CPU: AMD Ryzen Threadripper 3970x
- GPU: Sapphire NITRO+ RX 5700 XT
- RAM: CORSAIR VENGEANCE RGB PRO 16GB x 4 (3200)
- SSD: Samsung SSD 970 EVO Plus 500GB x 2
- Cooler: CORSAIR Hydro Series H115i PRO RGB 280mm (USB need to be disconnected to make sleep working)
- Display: LG 27GN950-B
- Extra Network Card: Fenvi BCM94360CD

## What works

- Big Sur 11.1
- iServices (iMessage / FaceTime / etc.)
- [Continuity](https://support.apple.com/en-us/HT204681) (except Auto Unlock / Sidecar / Apple Pay)
- Sleep / Wake
- Windows / macOS dual boot
- Onboard 2.5G LAN (RTL8125)

## What does not work

- Shutdown (will instant reboot after shutdown)
- Apple Hypervisor (Docker for Mac, Parallels etc.) / Adobe ([patches](https://gist.github.com/naveenkrdy/26760ac5135deed6d0bb8902f6ceb6bd) available, but I don't use Adobe products)
- Auto Unlock (can be enabled in System Preferences but actually doesn't work)
- Sidecar (but we can use [Duet Display](https://www.duetdisplay.com/) as an alternative)
- Apple Pay (doesn't work with all Hackintoshes)
- 4K 144Hz ([a common issue in Big Sur](https://egpu.io/forums/mac-setup/4k144hz-no-longer-available-after-upgrade-to-big-sur/). 27GN950-B can only use up to 4K 95Hz without DSC)
