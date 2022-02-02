# Awesome Dell XPS
Tips to improve your experience with Dell XPS 7590 and other Dell laptops.

Disclaimer: all these instructions are written for Dell Vostro 7590 which is (almost) sharing the chassis with Dell XPS 7590 and Dell Inspiron 15 7000. Repository name says XPS for clickbait reasons since it's a much more popular model. Most (if not all) instructions are applicable for Dell XPS 7590 and many other Dell models as well.

# Fixes

## Touchpad not working after sleep

https://www.dell.com/community/XPS/XPS-15-7590-touchpad-does-not-respond-sometimes/td-p/7655356/page/7

## Laptop is hot in sleep mode and drains battery

Use hibernate instead of sleep

## Coil whine

Undervolting and underclocking using Throttlestop
https://www.ultrabookreview.com/31385-the-throttlestop-guide/

MSI Afterburner for undervolting GPU

On Windows 10 with disabled virtualisation requires Bios 1.5.1 or lower.
On Windows 11 with virtualization enabled, it requires more steps - see here: https://www.techpowerup.com/forums/threads/throttlestop-dead-on-windows-11.284102/page-3

https://github.com/tianocore/tianocore.github.io/wiki/Getting-Started-with-EDK-II
https://github.com/tianocore/tianocore.github.io/wiki/Windows-systems

https://www.reddit.com/r/XPS/comments/sh02yr/undervolting_my_9510_11800h_with_windows_11_and/
https://brendangreenley.com/undervolting-2020-dell-laptops-like-the-vostro-7500-and-more-tips-to-improve-thermals-battery-life-and-speed/

## Annoying fans

https://github.com/AaronKelley/DellFanManagement

# Thermal modding

https://www.reddit.com/r/Dell/comments/g2qbco/xps_15_custom_heatsink_solution_to_overheating_to/

# XPS vs Vostro vs Inspiron

Only major differences are shown

| | XPS 7590 | Vostro 7590 | Inspiron 7590 |
| -- |  -- | -- | -- |
| Display | FHD 500 nits or touch UHD 500 nits or OLED UHD 400 nits | FHD 300 nits or UHD 400 nits | FHD 300 nits or UHD 500 nits |
| Weight | 1.8 Kg | 1.9 Kg | 1.8 Kg |
| Material | Aluminium with carbon-fiber | Aluminium | Magnesium |
| Keyboard | 80 keys | 101 keys | 101 keys |
| Top CPU | Up to i9-9980HK | i9-9880H listed on site but not seen on the market | i9-9880H listed on site but not seen on the market |
| Chipset | CM246 | HM370 | HM370 |
| Card-Reader | SD | microSD | microSD |
| USB type A | 2 ports | 3 ports | 3 ports |
| Wireless (upgradeable) | WiFi 6 | WiFi 5 | WiFi 5 |
| M.2 Storage | 1 slot | 2 slots | 2 slots |
| security-cable slot (wedge-shaped) | yes | no | no |
| Support | https://www.dell.com/support/manuals/en-us/xps-15-7590-laptop/xps-15-7590-setup-and-specifications/dimensions-and-weight?guid=guid-7df32f47-45cf-4a08-ad99-b01eec4f3ce6&lang=en-us | https://www.dell.com/support/manuals/en-us/vostro-15-7590-laptop/vos7590_setupspecs/dimensions-and-weight?guid=guid-5c33f917-293a-4bb4-a06c-f72cc5f41548&lang=en-us | https://www.dell.com/support/manuals/en-us/inspiron-15-7590-laptop/inspiron-7590-setup-and-specifications/dimensions-and-weight?guid=guid-7df32f47-45cf-4a08-ad99-b01eec4f3ce6&lang=en-us |


# Configuration

Make sure to choose option without HDD - it comes with big battery

# Upgrades

Dell provides great instructions on assembly/disassembly: https://dl.dell.com/topicspdf/vostro-15-7590-laptop_owners-manual_en-us.pdf
You can upgrade storage (2 slots M.2 2280 PCIe Gen 3.0x4 NVMe, up to 32 Gbps, no limit on capacity), memory (2 slots SODIMM DDR4 2666 MHz up to 64Gb), wireless module (1 slot M.2 2230, upgradeable to WiFi 6E and beyond)

## Storage

Since only PCIe Gen 3 is supported, there's no need to invest into Gen4+ SSDs.
Ideal SSD must have speed close to PCIe Gen3 saturation and be efficient in terms of temperature and power consumption.

Good choise: SK Hynix Gold P31 (up to 2Tb) - https://ssd.skhynix.com/gold_p31/

RAID-0 while possible won't give you any speed improvements due to saturation of PCIe bus as well - https://www.youtube.com/watch?v=DWBvDt96ZTc

## Memory

Even if Dell states that 64Gb is only supported on certain models, in fact it does work not only on XPS series but also on Inspiron / Vostro series.

DDR4 SO-DIMM 2666 MHz is supported.
Any casual CL19 memory would work, however you will face issues with low-latency "gaming" memory.
For example Patriot Viper Steel memory with timings 18-18-18-43 would not work, while Corsair Vengeance with timings 18-19-19-39 will work just fine.
If you want to squeeze maximum performance out of your laptop, check carefully if memory would work and make sure you can return it if not.

People on reddit collated a table of supported RAM for the 9570 (previous) generation: https://www.reddit.com/r/Dell/comments/8r55ys/9570_working_ram_kits/

## Wireless

Update to WiFi 6 is possible. No details yet

# BIOS

While addressing certain security issues, most recent BIOS updates disable undervolting.
Make sure you're using BIOS version 1.5.1 if you want to do undervolting.

# Links
1. https://www.youtube.com/playlist?list=PLwkH-8urcGm6rxc99tk75eZq_veJe0SUq
2. https://github.com/AaronKelley/DellFanManagement
3. https://www.dell.com/support/home/en-uk/product-support/product/vostro-15-7590-laptop/docs
4. https://ark.intel.com/content/www/us/en/ark/products/191045/intel-core-i79750h-processor-12m-cache-up-to-4-50-ghz.html
