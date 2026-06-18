# M5Shark — Device Owner Guide

**Complete setup, device reference, firmware paths, troubleshooting, and safety notes for the M5Shark hardware ecosystem.**

> ⚖️ **For lawful education, development, repair, interoperability study, and authorized testing only.**
> Own it. Have permission. Use the right antenna/accessory. Stay in the lab. Stop if the device behaves unexpectedly.

📄 **Domantas Uba edition PDF:** [`M5Shark-Owner-Guide.pdf`](M5Shark-Owner-Guide.pdf) — this repository mirrors it as searchable, linkable documentation.

---

## Table of Contents

1. [How to Use This Guide](#1-how-to-use-this-guide)
2. [From Box to First Safe Use](#2-from-box-to-first-safe-use)
3. [Product Family Overview](#3-product-family-overview)
4. [Device Chooser](#4-device-chooser)
5. [Device Family Details](#5-device-family-details)
6. [Modules, Accessories & Shared UI](#6-modules-accessories--shared-ui)
7. [Firmware & Setup Paths](#7-firmware--setup-paths)
8. [M5Shark — Flipper-Style Firmware Guide](#8-m5shark--flipper-style-firmware-guide)
9. [Bruce-Style Setup Flow](#9-bruce-style-setup-flow)
10. [Universal RF Research Tool](#10-universal-rf-research-tool)
11. [Quick Start & Troubleshooting](#11-quick-start--troubleshooting)
12. [FAQ & Help Checklist](#12-faq--help-checklist)
13. ["No Factory Keys Found" Notice](#13-no-factory-keys-found-notice)
14. [Reference Links](#14-reference-links)
15. [Safety & Legal Notice](#15-safety--legal-notice)

---

## 1. How to Use This Guide

This guide helps you **identify the right device family**, **choose the correct firmware path**, **use accessories safely**, and **troubleshoot common setup problems**.

| Principle | What it means |
|---|---|
| **Start correctly** | Identify your exact device family *before* using firmware, accessories, or setup links. |
| **Use safe workflows** | Begin with receive-first learning, owned devices, lab demos, and authorized testing only. |
| **Universal RF reference** | The Universal RF section is framed for compliance review, shielded-lab study, and safety planning. |
| **Help built in** | Quick start, firmware paths, FAQ, troubleshooting, and official reference links are all included. |

- **12** device families covered
- **5+** firmware paths (Flipper-style, Bruce, Marauder, Chameleon, SDR, board-specific)
- **100% authorization-first** — use only with permission, owned devices, and controlled environments

---

## 2. From Box to First Safe Use

Follow this path **before** updating firmware, connecting accessories, or starting any RF, RFID, NFC, IR, Wi-Fi, BLE, SDR, or GPIO workflow.

| Step | Owner action | What the guide provides |
|---|---|---|
| **1. Identify** | Check exact product family, board revision, and included accessories. | Device chooser, product details, model & firmware warnings. |
| **2. Inspect** | Check battery area, USB-C cable, SD card, antenna connector, enclosure, and screen. | Quick start, safety checklist, heat & charging notes. |
| **3. Setup** | Use only the firmware path that matches the exact device family. | Flipper, Bruce, Marauder, Chameleon, SDR, board-specific links. |
| **4. Learn** | Start with receive-first, demo, scan, log, or owned-device workflows. | Mode map, shared menu map, safe lab mode explanations. |
| **5. Troubleshoot** | If something fails, check exact model, firmware screen, cable, SD card, accessory. | Troubleshooting table, FAQ, owner-friendly explanations. |

**Before flashing anything:** confirm the exact model, board revision, and the current **About/Firmware** screen.

---

## 3. Product Family Overview

| Product family | Best for | Before first use |
|---|---|---|
| **M5Shark / SHARK RF** | Portable RF research and Flipper-style learning. | Confirm hardware revision, charge battery, insert microSD, use compatible firmware only. |
| **ESP32 / Bruce / Marauder devices** | Open-source ESP32 lab tools for Wi-Fi/BLE/RF education. | Choose the exact board target before flashing. Use owned networks and lab devices only. |
| **Chameleon Ultra V2** | RFID/NFC training, tag technology study, authorized lab testing. | Use only with tags, cards, and systems you own or are permitted to assess. |
| **H4 + R10 SDR** | Receive-first spectrum learning and SDR exploration. | Start receive-first, check antenna selection, follow local RF rules. |
| **Universal RF Research Tool** | Compliance-review, antenna planning, shielded-lab RF education. | Operate only in lawful, approved, controlled, shielded environments with a responsible operator. |

> **Responsible-use note:** Do not use any device for bypassing systems, attacking public networks, disrupting signals, or using third-party cards/remotes. Keep all activity focused on education, repair, diagnostics, interoperability, and authorized testing.

---

## 4. Device Chooser

| Device family | Type | Best fit / main use |
|---|---|---|
| **M5Shark / SHARK RF** | Portable RF research multi-tool | RF, NFC, RFID, IR, GPIO, authentication demos, hardware learning, authorized security education. |
| **ESP32-DIV V2.0** | ESP32-S3 multi-band handheld toolkit | Wi-Fi/BLE learning, 2.4 GHz research, Sub-GHz study, IR lab work, SD logging, touchscreen demos. |
| **RF CLOWN V2.0** | ESP32/nRF24 RF research board | 2.4 GHz protocol learning, portable RF experiments, firmware study, OLED menu demos, classroom RF. |
| **nRFBox-v3** | ESP32 wireless RF research tool | 2.4 GHz observation, BLE discovery, channel scanning, protocol study, open-source firmware learning. |
| **Mini ESP32 Marauder** | ESP32 Marauder family device | Wi-Fi/BLE education, wireless diagnostics, CTF labs, portable learning workflows. |
| **ESP32 Marauder** | ESP32 Marauder family device | Wireless security training, lab scanning, educational demos, firmware exploration. |
| **ESP32-C5 Marauder / Flipper Expansion** | Expansion board / standalone module | Flipper expansion, ESP wireless learning, GPS-assisted demos, large-screen viewing, authorized 433 MHz lab tests. |
| **Chameleon Ultra V2** | RFID/NFC reader, writer, emulator | Authorized RFID/NFC training, card technology study, lab tag testing, access-control education. |
| **T-Embed CC1101 Plus / TDeck Plus** | Advanced ESP32-S3 RF handheld | Larger-screen RF learning, keyboard/control workflows, Sub-GHz study, portable protocol labs. |
| **NM-RF-Hat for Bruce CYD** | RF expansion hat | Adds CC1101, nRF24, and PN532-style learning modules to compatible CYD/Bruce setups. |
| **H4 + R10 SDR** | SDR / portable spectrum platform | SDR learning, receive-first spectrum viewing, signal education, firmware exploration. |
| **Universal RF Research Tool** | Multi-band lab platform | Bench learning, controlled shielded-lab review, antenna planning, RF safety education. |

---

## 5. Device Family Details

Every family follows the same owner structure: **purpose · hardware notes · safe use · interface idea.**

### M5Shark / SHARK RF Research Device
- **Purpose:** RF, NFC, RFID, IR, GPIO, authentication demos, hardware learning, authorized security education.
- **Hardware:** STM32 64 MHz · 315/433 MHz RF · SMA female antenna port · 1.37″ monochrome LCD · USB-C · microSD up to 256 GB · 2000 mAh Li-Po · ≈ 94 × 44 × 22 mm.
- **Firmware truth:** Positioned as a Flipper Zero alternative. Use **only** firmware confirmed for the exact M5Shark / SHARK hardware revision. Do not install random forks or firmware for a different board.
- **Screen map:** RF · IR · NFC · RFID · GPIO · Files · About/Help and safety prompts.

### ESP32-DIV V2.0 Development Board
- **Purpose:** Wi-Fi/BLE learning, 2.4 GHz research, Sub-GHz study, IR lab work, SD logging, touchscreen demos.
- **Hardware:** ESP32-S3 · 16 MB flash · 2.8″ ILI9341 touchscreen · SD slot · USB-C · 3× nRF24 modules · 1× CC1101 module · RGB LEDs · buzzer · battery system.
- **Safe use:** Keep transmit-capable features lab-only; verify battery, antenna, and board revision before flashing.
- **UI idea:** Touchscreen tabs — Wireless, RF, IR, Logs, Settings, Help. Default to receive-first demos.

### RF CLOWN V2.0
- **Purpose:** 2.4 GHz protocol learning, portable RF experiments, firmware study, OLED menu demos, classroom RF concepts.
- **Hardware:** ESP32-WROOM-32U · triple nRF24 layout · OLED display · 3 tactile buttons · NeoPixel status indicator · IPEX antenna connectors.
- **Safe use:** Use receive-first workflows; do not frame as a disruption/interference tool.
- **UI idea:** Three-button UI (Back, Select, Next) with a persistent status-LED meaning table.

### nRFBox-v3
- **Purpose:** 2.4 GHz observation, BLE discovery, channel scanning, protocol study, open-source firmware learning.
- **Hardware:** ESP32 WROOM32U · nRF24 wireless modules · OLED interface · onboard controls · compact enclosure.
- **Safe use:** Limit to owned devices and lab environments; avoid nuisance traffic or disruption.
- **UI idea:** Channel view — channel, signal level, mode, log status, battery, help.

### Mini ESP32 Marauder
- **Purpose:** Wi-Fi/BLE education, wireless diagnostics, CTF labs, portable learning.
- **Hardware:** ESP32-based Marauder firmware device; controls/screen depend on variant.
- **Safe use:** Use only on networks and devices you own or are authorized to test.
- **UI idea:** Firmware-first map — Wi-Fi, BLE, Files, Logs, Settings, Update.

### ESP32 Marauder
- **Purpose:** Wireless security training, lab scanning, educational demos, firmware exploration.
- **Hardware:** ESP32-based device for the Marauder firmware ecosystem; details vary by build.
- **Safe use:** Keep guidance educational and authorization-first.
- **UI idea:** Consistent menu labels across Marauder devices for easy switching.

### ESP32-C5 Marauder / Flipper Expansion Module
- **Purpose:** Flipper expansion, ESP wireless learning, GPS-assisted demos, large-screen field viewing, authorized 433 MHz lab tests.
- **Hardware:** 4-in-1 concept — ESP module · 433 MHz RF · GPS · 2.8″ display · external antennas · rechargeable battery (version-dependent).
- **Safe use:** Confirm compatibility before connecting to another device; protect GPIO pins and avoid unknown targets.
- **UI idea:** Connection-state screens — Standalone, Connected, GPS Ready, RF Ready, Battery.

### Chameleon Ultra V2
- **Purpose:** Authorized RFID/NFC training, card technology study, lab tag testing, access-control education.
- **Hardware:** Dual-frequency RFID/NFC ecosystem covering common LF/HF study workflows with USB-C/Bluetooth control (build-dependent).
- **Safe use:** Only test tags, cards, and systems you own or are permitted to assess.
- **UI idea:** Card-state labels — Read, Saved, Emulate, Write, Locked, Error.

### T-Embed CC1101 Plus / TDeck Plus
- **Purpose:** Larger-screen RF learning, keyboard/control-heavy workflows, Sub-GHz study, portable protocol labs.
- **Hardware:** ESP32-S3 family with display and RF options; CC1101 and nRF24 compatibility depend on build.
- **Safe use:** Match firmware to the exact board; match antennas to the region and frequency band.
- **UI idea:** Mode dashboard — battery, region profile, antenna reminder, storage status, firmware version.

### NM-RF-Hat for Bruce CYD
- **Purpose:** Adds CC1101, nRF24, and PN532-style learning modules to compatible CYD/Bruce setups.
- **Hardware:** Expansion-hat concept; exact wiring/compatibility depend on CYD board revision.
- **Safe use:** Verify pinout, voltage, and firmware target before powering the hat.
- **UI idea:** Accessory-detect screen — module present, voltage OK, antenna present, storage ready.

### H4 + R10 SDR Device
- **Purpose:** Software-defined radio learning, receive-first spectrum viewing, signal education, firmware exploration.
- **Hardware:** H4 + R10 two-in-one SDR family with display, controls, USB-C / SDR host features (model-dependent).
- **Safe use:** Keep guidance **receive-first** unless you have legal authority and understand RF rules.
- **UI idea:** Spectrum screens — frequency, mode, gain, recording status, legal reminder.

### Universal RF Research Tool / Universal Signal RF Platforms
- **Purpose:** Bench learning, controlled shielded-lab review, antenna planning, RF safety education, product comparison.
- **Hardware:** Handheld aluminum unit with cooling fan, internal battery, channel switches, indicator lights, charging socket.
- **Safe use:** **Compliance review only.** RF-shielding or interference-capable equipment requires expert legal and technical review before import or operation. See [Section 10](#10-universal-rf-research-tool).

---

## 6. Modules, Accessories & Shared UI

### Modules & accessories

| Accessory | Role | Owner note |
|---|---|---|
| CC1101 Wireless Module | Sub-GHz RF module | Use 3.3 V logic, correct antenna, legal bands only. |
| nRF24L01+PA+LNA Module | 2.4 GHz module | Use stable 3.3 V power and an antenna matched to 2.4 GHz. |
| 2.4 GHz Wi-Fi/Bluetooth Antenna | Antenna accessory | Match SMA/RP-SMA connector type and frequency band. |
| Micro SD Card Module | Storage accessory | Use for logs, configs, profiles, and safe files. |
| PCB Protoboard | Prototyping board | Use for low-voltage electronics practice and safe bench wiring. |

### Shared menu map

| Menu | What you see |
|---|---|
| **Home** | Device status, battery, storage, active accessory, quick actions. |
| **Learn** | Short explanations for RF, IR, NFC, RFID, GPIO, SDR, and safety basics. |
| **Tools** | Device-specific feature groups with safety labels and accessory reminders. |
| **Files** | Saved profiles, logs, captures, notes, import/export. |
| **Settings** | Brightness, language, storage, firmware, region profile, reset. |
| **Help** | Safety checklist, troubleshooting, help info, glossary. |

**Safe Lab Mode** is the default experience — it favors receive-first learning, logs, classroom demos, and owned-device tests.

---

## 7. Firmware & Setup Paths

> ⚠️ A firmware image for a *similar-looking* device can break display, buttons, storage, radio modules, or boot behavior. **Match the exact device family first.**

| Device family | Recommended path |
|---|---|
| **M5Shark / SHARK** | Use the firmware path supplied for the SHARK RF device. For Flipper ecosystem firmware, use only a build confirmed for the exact M5Shark / SHARK hardware revision. |
| **Bruce-compatible products** | Use the Bruce website, web flasher, GitHub, or M5Burner where a matching device build exists. Bruce is for compatible ESP32 devices, *not* every STM32/SHARK device. |
| **ESP32-DIV V2.0** | Use ESP32-DIV project resources and hardware notes for the exact board revision. |
| **RF CLOWN V2.0** | Use RF-Clown releases and board-specific firmware. |
| **nRFBox-v3** | Use nRFBox project resources for the exact nRFBox version. |
| **ESP32 Marauder family** | Use the ESP32 Marauder getting-started guide and matching releases. |
| **Chameleon Ultra V2** | Use Chameleon Ultra firmware, app, CLI, and documentation. |
| **H4 + R10 SDR** | Use SDR/Mayhem-style documentation for the exact device revision. |
| **Universal RF Research Tool** | No generic firmware. Treat the manual as a hardware/owner safety reference; verify exact model, charger, and legal compliance before any lab evaluation. |

**Before flashing:** confirm the exact model, board revision, and the current About/Firmware screen.

---

## 8. M5Shark — Flipper-Style Firmware Guide

The M5Shark Device is a Flipper-style RF learning device. **Use only firmware confirmed for the exact M5Shark / SHARK hardware revision.**

| Firmware / tool | Best use | Owner guidance |
|---|---|---|
| **Official Flipper Zero firmware** | Default choice — stable updates, recovery, standard tools. | Use Flipper Mobile App, qFlipper, or Flipper Lab. Choose **Release** for normal users. |
| **Release / RC / Dev channels** | Release = stable, RC = testing, Dev = newest but may be unstable. | Use qFlipper advanced controls or the Flipper Mobile App channel selector. |
| **Flipper Lab web updater** | Browser tool for updates, apps, file management. | Connect by USB, open Flipper Lab, select device, follow prompts. |
| **qFlipper desktop updater** | Windows/macOS/Linux backup, restore, update, recovery. | Install qFlipper, connect with a data USB cable, insert microSD, choose Release, update. |
| **Unleashed firmware** | Popular custom firmware for advanced users. | Use the official project release/installer only. |
| **Momentum firmware** | Modern custom firmware (features from Unleashed, continuity from Xtreme). | Use the Momentum site/repo install instructions; verify the exact device target first. |
| **RogueMaster firmware** | Custom firmware with bundled apps/plugins. | Use official releases or web installer; back up files first. |
| **Xtreme firmware (legacy)** | Legacy reference only. | Use only when you intentionally need a legacy build and understand rollback/recovery. |

### Owner install flow
1. Confirm the exact M5Shark / SHARK hardware revision; use only firmware marked compatible with that exact target.
2. Charge the device, insert a known-good microSD card, use a **data-capable** USB cable.
3. **Back up** files, keys, remotes, databases, and saved profiles before changing firmware.
4. Normal users: start with the official **Release** channel via qFlipper, Flipper Mobile App, or Flipper Lab.
5. Custom firmware: download only from the official project website or GitHub release page, then follow that project's installer.
6. After flashing: verify firmware name/version and test screen, buttons, storage, IR, NFC/RFID, and RF menus.
7. If an update fails: stop installing custom builds and recover with official qFlipper before trying another package.

---

## 9. Bruce-Style Setup Flow

For products compatible with Bruce: **choose the exact target → flash safely → test basic functions → learn the menus.**

| Topic | Owner guidance |
|---|---|
| **Web flasher** | Open the Bruce web flasher in Chrome/Edge, connect a compatible device, select the exact target, follow prompts. |
| **M5Burner** | Install M5Burner, connect the device, choose the correct category, search **Bruce**, download & burn the matching firmware. |
| **Local binary** | Advanced only — use device-specific binaries when you know the exact target and recovery method. |
| **Recovery** | If the device won't boot, restore a known-good build for that exact model before trying another image. |
| **Main menus** | Wi-Fi, BLE, IR, Sub-GHz/RF tools, files, scripts, settings, updates, logs, device info (where available). |
| **File transfer** | SD card, USB file manager, or the device web interface. Keep backups before firmware updates. |
| **Web interface** | Some builds expose `bruce.local` when device and computer share a network. |
| **OTA updates** | Where available, update from device settings after connecting Wi-Fi and backing up files. |
| **Safe lab use** | Start with scanning, learning, logging, owned-device IR profiles, and classroom demos. |

> **Compatibility note:** Bruce is only for Bruce-compatible ESP32 products. M5Shark / SHARK RF devices use the Flipper-style workflow in [Section 8](#8-m5shark--flipper-style-firmware-guide).

---

## 10. Universal RF Research Tool

> 🛑 This section is a **compliance-review and shielded-lab reference**, *not* an operating guide for public-space interference. Use only as a controlled-lab RF education and compliance reference. **Do not use it to affect public or private communications.**

### Technical details (from the source manual)
- **Identity:** Treated here as the *Universal RF Research Tool*, part of the Universal RF / Universal Signal RF lab-platform family — not a separate product listing.
- **Description:** Portable full-band RF research/compliance platform — aluminum enclosure, active cooling fan, power indicator, side controls, antenna/channel switch bank, charging socket.
- **Manual-listed evaluation areas:** CDMA/GSM/DCS/PHS, 2G/3G/4G/5G, Wi-Fi 2.4 GHz & 5.8 GHz, GPS/BD-GPS, VHF, UHF. *References only — they do not create permission to transmit, block, or interfere.*
- **Power & runtime:** Built-in battery, ≈ 2–3 h runtime, ≈ 4 h full charge. AC/home charging and vehicle charging where the adapter allows.
- **Physical:** Host 165 × 97 × 45 mm · package 240 × 250 × 69 mm · kit weight ≈ 1.11 kg.
- **Heat note:** The aluminum shell transfers heat, so normal warmth can occur. **Stop using** if heat becomes unusual, the fan stops, charging behaves abnormally, or the enclosure is damaged.

### Safe Universal RF flow
1. Confirm the product is lawful to possess, import, and operate in your location.
2. Use only in an **authorized shielded lab**, compliance bench, classroom, or controlled environment where RF interference cannot affect others.
3. Do **not** operate near emergency services, cellular networks, GPS/GNSS receivers, aviation, public-safety systems, hospitals, vehicles, schools, or shared public spaces.
4. Inspect enclosure, charger, fan, switches, and accessories before any authorized lab evaluation.
5. Keep power off while checking accessories; stop immediately if the unit becomes unusually hot or unstable.
6. Keep approval records: test location, time, operator, and purpose.

---

## 11. Quick Start & Troubleshooting

### Universal quick start
1. Identify the exact device family before using any firmware or accessory.
2. Charge the device and inspect cables, antenna, battery area, and enclosure.
3. Use only the antenna/accessory intended for the selected mode.
4. Start with receive-first or demo modes before any advanced lab workflow.
5. Log what was tested, where, and who approved it.
6. Power down and store the device in its case after use.

### Troubleshooting

| Problem | First check |
|---|---|
| Device will not power on | Charge with a known-good 5 V USB source and data/charge cable; inspect the battery area. |
| Computer does not detect the device | Use a data-capable cable, another USB port, and the correct driver/firmware tool. |
| Storage not detected | Reinsert the card, test a known-good card, confirm a compatible file system. |
| Weak or unstable radio behavior | Check antenna type, connector tightness, distance, obstacles, battery, local interference. |
| Wrong menus or missing feature | Confirm the exact firmware build and accessory compatibility for that family. |
| Device becomes hot | Stop testing, power down, disconnect charging, inspect before reuse. |
| Universal RF heat / fan issue | Power down, keep channels off, disconnect charger, let it cool, contact M5Shark help if abnormal. |

---

## 12. FAQ & Help Checklist

| Question | Answer |
|---|---|
| **Does this work with Flipper Zero firmware?** | For the M5Shark / SHARK RF device, use only firmware confirmed for the exact hardware revision. Not every community fork or older build will work. |
| **Is Bruce firmware for all devices?** | No. Bruce is for compatible ESP32 devices and matching board builds. Always select the exact target before flashing. |
| **Can I test public networks/signals?** | No. Use only owned devices, your own lab equipment, or targets where you have clear written permission. |
| **Why are menus different after an update?** | The wrong/incompatible build may be installed. Restore the known-good firmware for that exact model, then retest. |
| **Can the Universal RF Research Tool be used anywhere?** | No. It is a compliance-review/lab reference device. Use only where purchase, import, possession, and operation are legal and shielded/authorized. |

### Before changing firmware
- [ ] Exact device model and hardware revision confirmed
- [ ] Known-good data USB cable and a charged battery
- [ ] Known-good microSD inserted (when firmware/apps need storage)
- [ ] About/Firmware screen checked before installing a different build
- [ ] For RF/RFID/NFC: accessory, tag, remote, or network is owned by you or authorized for testing

---

## 13. "No Factory Keys Found" Notice

Some Flipper-style firmware shows: *"No Factory Keys Found. Secure Enclave is damaged. Some apps will not work."* on compatible M5Shark-style hardware. **This does not mean the device is physically broken.**

| Owner question | Clear answer |
|---|---|
| Is my M5Shark damaged? | **No.** This is normally a firmware-compatibility notice, not hardware failure. The device can still boot, open menus, read files, and use compatible features. |
| What should I do on the screen? | Press **OK / Back / Continue** to skip the warning and enter the main menu. Don't panic or keep reinstalling random builds. |
| Will everything work? | Normal functions work with the correct firmware, SD card, cable, and accessories. Some official Flipper security apps that require original factory keys may show limits. |
| Why does it appear? | Some firmware checks for original Flipper factory keys / secure-enclave data. A compatible M5Shark may not use the same key system, so the notice appears. |
| What not to do | Do not install unknown key-replacement tools and do not flash random firmware repeatedly. Use only the correct path for your exact hardware revision. |

**Fast owner steps:** press OK to enter the menu → check buttons, screen, microSD, Files, RF/IR/NFC/RFID menus, settings → use the firmware recommended for your exact revision → if only one app fails, treat it as an app/firmware compatibility issue → contact M5Shark help only if the device cannot boot, buttons fail, storage isn't detected, or the warning blocks normal menus.

---

## 14. Reference Links

> Use official firmware sources wherever possible. For custom firmware, use official project pages and verify the exact target. **Do not install random payload packs or unknown files.**

### Flipper-style firmware & tools
| Resource | Link |
|---|---|
| Official Flipper Zero firmware | https://github.com/flipperdevices/flipperzero-firmware |
| Flipper Zero downloads | https://flipperzero.one/update |
| Flipper firmware update guide | https://docs.flipper.net/zero/basics/firmware-update |
| Flipper Lab (web) | https://lab.flipper.net/ |
| Apps Catalog | https://lab.flipper.net/apps |
| qFlipper documentation | https://docs.flipper.net/zero/qflipper |
| qFlipper GitHub | https://github.com/flipperdevices/qFlipper |
| App troubleshooting docs | https://docs.flipper.net/zero/apps/troubleshoot |
| Developer documentation | https://developer.flipper.net |
| uFBT build tool | https://github.com/flipperdevices/flipperzero-ufbt |
| Official IR database | https://github.com/flipperdevices/IRDB |
| Awesome Flipper Zero | https://github.com/djsime1/awesome-flipperzero |
| Awesome-Flipper website | https://awesome-flipper.com |

### Custom Flipper firmware
| Project | Link |
|---|---|
| Unleashed firmware | https://github.com/DarkFlippers/unleashed-firmware |
| Momentum firmware | https://github.com/Next-Flip/Momentum-Firmware · https://momentum-fw.dev/ |
| RogueMaster firmware | https://github.com/RogueMaster/flipperzero-firmware-wPlugins · [releases](https://github.com/RogueMaster/flipperzero-firmware-wPlugins/releases) |
| Xtreme firmware (legacy) | https://github.com/Flipper-XFW/Xtreme-Firmware |

### ESP32 / Bruce / Marauder / SDR
| Resource | Link |
|---|---|
| Bruce website | https://bruce.computer/ |
| Bruce web flasher | https://bruce.computer/flasher |
| Bruce firmware GitHub | https://github.com/BruceDevices/firmware |
| M5Burner | https://docs.m5stack.com/en/uiflow/m5burner/intro |
| ESP32 Marauder getting started | https://github.com/justcallmekoko/ESP32Marauder/wiki/getting-started |
| ESP32 Marauder GitHub | https://github.com/justcallmekoko/ESP32Marauder |
| ESP32-DIV hardware wiki | https://github.com/cifertech/ESP32-DIV/wiki/Hardware |
| nRFBox GitHub | https://github.com/cifertech/nRFBox |
| RF-Clown releases | https://github.com/cifertech/RF-Clown/releases |
| Chameleon Ultra GitHub | https://github.com/RfidResearchGroup/ChameleonUltra |
| SDR Mayhem firmware wiki | https://github-wiki-see.page/m/portapack-mayhem/mayhem-firmware/wiki |

### Component datasheets
| Resource | Link |
|---|---|
| CC1101 technical reference | https://www.ti.com/product/CC1101 |
| nRF24L01+ specification | https://www.sparkfun.com/datasheets/Wireless/Nordic/nRF24L01P_Product_Specification_1_0.pdf |

### Product pages (m5shark.com)
| Product | Link |
|---|---|
| M5Shark Device | https://m5shark.com/products/m5shark-device-flipper-zero-alternative |
| ESP32-DIV V2.0 | https://m5shark.com/products/esp32-div-v2-0 |
| nRFBox-v3 | https://m5shark.com/products/nrfbox-v3-based-on-esp32 |
| Chameleon Ultra V2 | https://m5shark.com/products/chameleon-ultra-contactless-smart-card-emulator-rfid-smart-chip-reader-3xcuid-uid-keychain-compliant-to-nfc-read-writer |
| Mini ESP32 Marauder | https://m5shark.com/products/esp32-marauder |
| ESP32-C5 Marauder | https://m5shark.com/products/esp32-c5-marauder-working-with-flipper-zero |
| Universal RF Research Tool | https://m5shark.com/products/universal-rf-device-compliance-review |
| NM-RF-Hat for Bruce CYD | https://m5shark.com/products/nm-rf-hat-for-bruce-cyd |
| H4 + R10 SDR Device | https://m5shark.com/products/h4-r10-two-in-one-sdr-device |
| T-Embed CC1101 Plus | https://m5shark.com/products/t-embed |
| CC1101 Wireless Module | https://m5shark.com/products/cc1101-wireless-module-with-sma-antenna-wireless-transceiver-module-for-315-433-868-915mhz |

*(Full product/accessory link list is in the [PDF guide](M5Shark-Owner-Guide.pdf), Section 13.)*

---

## 15. Safety & Legal Notice

This guide is for **lawful education, development, repair, interoperability study, and authorized testing**. It is **not** permission to test systems, signals, cards, remotes, locks, computers, or networks without authorization.

**Owner responsibility:** You are responsible for local laws, radio-frequency rules, access-control rules, privacy rules, import restrictions, battery safety, and permission to test. If you are unsure whether a test is allowed, **do not run it** until you have permission and understand the rules.

### The simple rule
> **Own it. Have permission. Use the right antenna/accessory. Stay in the lab. Stop if the device behaves unexpectedly.**

### Final owner checklist
- [ ] Identify the exact M5Shark device family before using firmware or accessories
- [ ] Use only owned or authorized devices, tags, remotes, networks, signals, and lab equipment
- [ ] Start with receive-first learning, safe demo modes, logs, and basic checks
- [ ] Back up files before firmware updates; use the correct target for your hardware revision
- [ ] Stop immediately if the device overheats, charging behaves abnormally, or a test is not clearly allowed

---

<sub>📄 Mirrored from the official **M5Shark Device Owner Guide** PDF. Verify exact device, region rules, and firmware target before use. Licensed under [MIT](LICENSE) for the documentation in this repository.</sub>
