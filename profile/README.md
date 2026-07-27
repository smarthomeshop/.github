<div align="center">

<img src="https://avatars.githubusercontent.com/u/143031118?v=4" width="112" alt="SmartHomeShop.io logo">

# SmartHomeShop.io

**Our products run 100% locally on your own network, with software that is fully open source.**
**Every product is designed, developed and built in the Netherlands.**

[![Shop](https://img.shields.io/badge/Shop-smarthomeshop.io-00a676?style=for-the-badge)](https://smarthomeshop.io)
[![Documentation](https://img.shields.io/badge/Docs-docs.smarthomeshop.io-2563eb?style=for-the-badge)](https://docs.smarthomeshop.io)
[![Firmware](https://img.shields.io/badge/Firmware-Web%20Flasher-f97316?style=for-the-badge)](https://smarthomeshop.io/en/firmware)
[![Discord](https://img.shields.io/badge/Support-Discord-5865f2?style=for-the-badge)](https://smarthomeshop.io/discord)

</div>

---

SmartHomeShop.io builds smart home products for people who want reliable sensor data in Home
Assistant without a mandatory cloud account or subscription. Our devices are designed around
ESPHome, local control, OTA firmware updates and practical installation guides.

Most firmware repositories contain production ESPHome packages, hardware-specific YAML files,
changelogs and ESP Web Tools manifests. You can use the factory firmware, switch supported devices
between WiFi and Ethernet variants, or adopt the device in ESPHome when you want to customize the
configuration yourself.

## Energy And Water

| Product | What it does | Highlights | Links |
| --- | --- | --- | --- |
| **P1MeterKit** | Reads DSMR P1 smart meter telegrams for electricity, solar return and gas monitoring. | ESPHome, WiFi, DSMR v4/v5, local Home Assistant entities, optional USB-C power for older meters. | [Repo](https://github.com/smarthomeshop/p1meterkit) / [Docs](https://docs.smarthomeshop.io/en/p1meterkit/) / [Product](https://p1meterkit.nl/en) |
| **P1SplitterKit** | Splits one DSMR P1 port into five active outputs for multiple readers. | Active signal amplification, electrically isolated outputs, DSMR v2-v5, no software required. | [Docs](https://docs.smarthomeshop.io/en/p1splitterkit/) / [Product](https://smarthomeshop.io/en/products/p1splitterkit) |
| **WaterP1MeterKit** | Combines P1 energy reading and water meter monitoring in one device. | WiFi, Ethernet, PoE, detachable water sensor, expansion port for leak or door sensors, local firmware variants. | [Repo](https://github.com/smarthomeshop/waterp1meterkit) / [Docs](https://docs.smarthomeshop.io/en/waterp1meterkit-v2/) / [Product](https://waterp1meterkit.nl/en) |
| **WaterMeterKit** | Tracks a compatible analog water meter in Home Assistant. | Magnetic water meter sensing, absolute meter totals, temperature and humidity, WiFi, USB-C power. | [Repo](https://github.com/smarthomeshop/watermeterkit) / [Docs](https://docs.smarthomeshop.io/en/watermeterkit-v2/) / [Product](https://watermeterkit.nl/en) |
| **WaterFlowKit** | Measures flow rate, total usage and water temperature on individual pipes. | Up to four flow inputs on v2, multiple YF-series sensor sizes, WiFi/Ethernet firmware, local and app-sync variants. | [Repo](https://github.com/smarthomeshop/waterflowkit) / [Docs](https://docs.smarthomeshop.io/en/waterflowkit/) / [Product](https://waterflowkit.nl/en) |

## Room Sensors

Each hardware revision has its own firmware folder, so the configuration that matches your device
stays visible. The revisions differ in more than looks, which is why they are listed separately.

| Product | Presence | Air quality | Network | Voice | Links |
| --- | --- | --- | --- | --- | --- |
| **UltimateSensor v1** | LD2450 mmWave tracking + PIR | CO2, temperature, humidity, lux, VOC/NOx, optional SPS30 particulate matter | WiFi, Ethernet, PoE | - | [Repo](https://github.com/smarthomeshop/ultimatesensor/tree/main/ultimatesensor-v1) / [Docs](https://docs.smarthomeshop.io/en/ultimatesensor/) / [Product](https://ultimatesensor.nl/en) |
| **UltimateSensor v2** | LD2412 presence + PIR, optional LD2450 or LD2460 multi-target tracking | CO2, temperature, humidity, lux, VOC/NOx, optional SPS30 particulate matter | WiFi, Ethernet, PoE | Microphone and speaker for Home Assistant Voice | [Repo](https://github.com/smarthomeshop/ultimatesensor/tree/main/ultimatesensor-v2) / [Docs](https://docs.smarthomeshop.io/en/ultimatesensor-v2/) / [Product](https://ultimatesensor.nl/en) |
| **UltimateSensor Mini v1** | LD2450 mmWave tracking | CO2, temperature, humidity, lux, VOC/NOx, optional SPS30 particulate matter | WiFi | Microphone and speaker for Home Assistant Voice | [Repo](https://github.com/smarthomeshop/ultimatesensor-mini/tree/main/ultimatesensor-mini-v1) / [Docs](https://docs.smarthomeshop.io/en/ultimatesensor-mini/) / [Product](https://ultimatesensor.nl/en/mini) |
| **UltimateSensor Mini v2** | LD2412 presence, optional LD2450 or LD2460 multi-target tracking | CO2, temperature, humidity, lux, VOC/NOx, optional SPS30 particulate matter | WiFi, Ethernet, Thread | - | [Repo](https://github.com/smarthomeshop/ultimatesensor-mini/tree/main/ultimatesensor-mini-v2) / [Docs](https://docs.smarthomeshop.io/en/ultimatesensor-mini-v2/) / [Product](https://ultimatesensor.nl/en/mini) |
| **CeilSense** | mmWave presence, invisible in the ceiling | Lux, pressure, optional CO2, temperature and humidity | WiFi, Ethernet, PoE, 110-240 VAC or USB-C | - | [Repo](https://github.com/smarthomeshop/ceilsense) / [Docs](https://docs.smarthomeshop.io/en/ceilsense/) / [Product](https://ceilsense.nl/en) |

> **Looking for voice?** The microphone and speaker moved between revisions. On the Mini they are
> part of v1 and not of v2; on the full UltimateSensor it is the other way around, so v2 is the one
> that talks. Every revision measures the same air quality, so pick the one whose presence detection
> and voice support match what you want.

## Firmware And Updates

- **Factory firmware:** flash or update supported devices from the [SmartHomeShop firmware page](https://smarthomeshop.io/en/firmware) with ESP Web Tools.
- **ESPHome packages:** use the YAML packages in each product repository when you want to manage firmware from your own ESPHome dashboard.
- **Network variants:** supported products provide WiFi, Ethernet and sometimes PoE or Thread builds. Some repositories also include SmartHomeShop App sync variants next to the fully local firmware.
- **Hardware revisions:** product repositories keep separate folders for each hardware revision, so the matching configuration stays visible and auditable.
- **Changelogs:** firmware-facing release notes live in the product repositories, usually in `CHANGELOG.md` and GitHub Releases.

## Components And Tooling

| Repository | Purpose |
| --- | --- |
| [smarthomeshop/ld2412](https://github.com/smarthomeshop/ld2412) | Reusable ESPHome integration work for the HLK-LD2412 mmWave presence module used across SmartHomeShop products. |
| [smarthomeshop/ld2460](https://github.com/smarthomeshop/ld2460) | ESPHome external component and packages for the HLK-LD2460 multi-target tracking radar upgrade. |
| [smarthomeshop/home-assistant-integration](https://github.com/smarthomeshop/home-assistant-integration) | Home Assistant integration for SmartHomeShop.io devices: room designer, smart energy planning and per-product insights. |

## Start Here

1. Choose a product from the tables above, and the hardware revision that matches your device.
2. Follow the matching guide on [docs.smarthomeshop.io](https://docs.smarthomeshop.io).
3. Flash or update firmware from [smarthomeshop.io/en/firmware](https://smarthomeshop.io/en/firmware), or adopt the YAML in ESPHome for advanced customization.
4. Add the device to Home Assistant through the ESPHome integration.
5. For support, join the [Discord community](https://smarthomeshop.io/discord) or open an issue in the relevant repository.

## What We Care About

- Local-first operation with Home Assistant and ESPHome, with cloud and app features that stay optional.
- Clear product-specific documentation and firmware manifests.
- Hardware revisions that remain maintainable over time.
- Practical sensors for energy, water, air quality, presence and automation.

---

<div align="center">

If a SmartHomeShop project helps your setup, consider starring the repository you use.<br>
It makes the active projects easier to find for other Home Assistant users.

</div>
