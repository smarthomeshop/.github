<div align="center">

# SmartHomeShop.io

**Local-first smart home hardware, ESPHome firmware and Home Assistant integrations.**

[![Shop](https://img.shields.io/badge/Shop-smarthomeshop.io-00a676?style=for-the-badge)](https://smarthomeshop.io)
[![Documentation](https://img.shields.io/badge/Docs-docs.smarthomeshop.io-2563eb?style=for-the-badge)](https://docs.smarthomeshop.io)
[![Firmware](https://img.shields.io/badge/Firmware-Web%20Flasher-f97316?style=for-the-badge)](https://smarthomeshop.io/en/firmware)
[![Discord](https://img.shields.io/badge/Support-Discord-5865f2?style=for-the-badge)](https://smarthomeshop.io/discord)

</div>

SmartHomeShop.io builds smart home products for users who want reliable sensor data in Home Assistant without a mandatory cloud account or subscription. Our devices are designed around ESPHome, local control, OTA firmware updates and practical installation guides.

Most firmware repositories contain production ESPHome packages, hardware-specific YAML files, changelogs and ESP Web Tools manifests. You can use the factory firmware, switch supported devices between WiFi and Ethernet variants, or adopt the device in ESPHome when you want to customize the configuration yourself.

## Product Lineup

| Product | What it does | Highlights | Links |
| --- | --- | --- | --- |
| **P1MeterKit** | Reads DSMR P1 smart meter telegrams for electricity, solar return and gas monitoring. | ESPHome, WiFi, DSMR v4/v5, local Home Assistant entities, optional USB-C power for older meters. | [Repo](https://github.com/smarthomeshop/p1meterkit) / [Docs](https://docs.smarthomeshop.io/en/p1meterkit/) / [Product](https://p1meterkit.nl/en) |
| **P1SplitterKit** | Splits one DSMR P1 port into five active outputs for multiple readers. | Active signal amplification, electrically isolated outputs, DSMR v2-v5, no software required. | [Docs](https://docs.smarthomeshop.io/en/p1splitterkit/) / [Product](https://smarthomeshop.io/en/products/p1splitterkit) |
| **WaterP1MeterKit** | Combines P1 energy reading and water meter monitoring in one device. | WiFi, Ethernet, PoE, detachable water sensor, expansion port for leak or door sensors, local firmware variants. | [Repo](https://github.com/smarthomeshop/waterp1meterkit) / [Docs](https://docs.smarthomeshop.io/en/waterp1meterkit-v2/) / [Product](https://waterp1meterkit.nl/en) |
| **WaterMeterKit** | Tracks a compatible analog water meter in Home Assistant. | Magnetic water meter sensing, absolute meter totals, temperature and humidity, WiFi, USB-C power. | [Repo](https://github.com/smarthomeshop/watermeterkit) / [Docs](https://docs.smarthomeshop.io/en/watermeterkit-v2/) / [Product](https://watermeterkit.nl/en) |
| **WaterFlowKit** | Measures flow rate, total usage and water temperature on individual pipes. | Up to four flow inputs on v2, multiple YF-series sensor sizes, WiFi/Ethernet firmware, local and app-sync variants. | [Repo](https://github.com/smarthomeshop/waterflowkit) / [Docs](https://docs.smarthomeshop.io/en/waterflowkit/) / [Product](https://waterflowkit.nl/en) |
| **UltimateSensor** | Full room sensor for air quality, occupancy and Home Assistant voice use cases. | CO2, temperature, humidity, lux, VOC/NOx, PIR, LD2412 + LD2450 dual mmWave, optional SPS30 and LD2460, WiFi/Ethernet/PoE. | [Repo](https://github.com/smarthomeshop/ultimatesensor) / [Docs](https://docs.smarthomeshop.io/en/ultimatesensor/) / [Product](https://ultimatesensor.nl/en) |
| **UltimateSensor Mini** | Compact modular room sensor for presence and air-quality monitoring. | CO2, temperature, humidity, lux, VOC/NOx, LD2412 + LD2450 mmWave, optional SPS30 and LD2460, compact case, USB-C/PoE options. | [Repo](https://github.com/smarthomeshop/ultimatesensor-mini) / [Docs](https://docs.smarthomeshop.io/en/ultimatesensor-mini/) / [Product](https://ultimatesensor.nl/en/mini) |
| **CeilSense** | Ceiling-mounted sensor for invisible presence and environmental monitoring. | mmWave presence, lux, pressure, optional CO2/temp/humidity, WiFi, Ethernet, PoE, 110-240 VAC and USB-C power options. | [Repo](https://github.com/smarthomeshop/ceilsense) / [Docs](https://docs.smarthomeshop.io/en/ceilsense/) / [Product](https://ceilsense.nl/en) |

## Firmware And Updates

- **Factory firmware:** flash or update supported devices from the [SmartHomeShop firmware page](https://smarthomeshop.io/en/firmware) with ESP Web Tools.
- **ESPHome packages:** use the YAML packages in each product repository when you want to manage firmware from your own ESPHome dashboard.
- **Network variants:** supported products provide WiFi, Ethernet and sometimes PoE-oriented builds. Some repositories also include SmartHomeShop App sync variants next to the fully local firmware.
- **Hardware revisions:** product repositories keep separate folders for each hardware revision, so the matching configuration stays visible and auditable.
- **Changelogs:** firmware-facing release notes live in the product repositories, usually in `CHANGELOG.md` and GitHub Releases.

## Components And Tooling

| Repository | Purpose |
| --- | --- |
| [smarthomeshop/ld2412](https://github.com/smarthomeshop/ld2412) | Reusable ESPHome integration work for the HLK-LD2412 mmWave presence module used across SmartHomeShop products. |
| [smarthomeshop/ld2460](https://github.com/smarthomeshop/ld2460) | ESPHome external component and packages for the HLK-LD2460 multi-target tracking radar upgrade. |
| [smarthomeshop/home-assistant-integration](https://github.com/smarthomeshop/home-assistant-integration) | Home Assistant integration work for SmartHomeShop.io devices. |
| [ESPHome Devices](https://github.com/esphome/esphome-devices) | Public ESPHome device documentation project that can include community device entries and examples. |

## Start Here

1. Choose a product from the table above.
2. Follow the matching guide on [docs.smarthomeshop.io](https://docs.smarthomeshop.io).
3. Flash or update firmware from [smarthomeshop.io/en/firmware](https://smarthomeshop.io/en/firmware), or adopt the YAML in ESPHome for advanced customization.
4. Add the device to Home Assistant through the ESPHome integration.
5. For support, join the [Discord community](https://smarthomeshop.io/discord) or open an issue in the relevant repository.

## What We Care About

- Local-first operation with Home Assistant and ESPHome.
- Clear product-specific documentation and firmware manifests.
- Hardware revisions that remain maintainable over time.
- Practical sensors for energy, water, air quality, presence and automation.
- Optional cloud/app features without making them mandatory for local Home Assistant users.

---

If a SmartHomeShop project helps your setup, consider starring the repository you use. It makes the active projects easier to discover for other Home Assistant users.
