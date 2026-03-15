# Sovereign Field Artillery

```
Status:    STANDARD
UID:       SFA-1.0
Lexifier:  UK English (3166-2:GB)
Encoding:  US-ASCII
Keywords:  Per RFC 2119
```

---

## 0. Purpose

**Sovereign Field Artillery (SFA)** is the personal weaponry of the Knights of the Round Table. It consists of two Babylon-free weapon systems: a primary hacking platform (Long) and a field communicator (Short). Both run sovereign, auditable software stacks. Neither answers to either its manufacturer or the US government.

| | Long | Short |
| :--- | :--- | :--- |
| Hardware | ThinkPad T480 / T14 Gen 5 | Google Pixel 7 |
| OS | NixOS / ArtNix | GrapheneOS |
| Firmware | Heads / coreboot | Verified boot (operator keys) |
| Baseline cost | GBP 155-195 (T480) / GBP 450-600 (T14 Gen 5) | GBP 155-220 |

## 1. Requirements

**Long**

| Requirement | Reason |
| :--- | :--- |
| CPU: 4c/8t minimum | Parallel tooling, containers, language servers |
| RAM: 32 GB minimum | The Hacker's local environment runs without constraint |
| Workflow: terminal-first | The interface of a Hacker is the terminal |
| Keyboard: backlit | A Hacker operates in all conditions |
| Firmware: Babylon-free | The machine must answer only to its operator |

**Both**

| Requirement | Reason |
| :--- | :--- |
| OS: NixOS / ArtNix (Long), GrapheneOS (Short) | A Hacker's system state is impermanent, reproducible, and auditable |
| Encryption: full disk | The machine does not surrender its secrets |
| Biometrics: fingerprint | The Hacker's identity is verified, not recited |
| Mobile connectivity | A Hacker is not tethered to a single point of failure |

---

## 2. Long

Two models are sanctioned. Operators choose based on budget and operational priority.

| | T480 | T14 Gen 5 |
| :--- | :--- | :--- |
| Cost (refurb) | GBP 130-160 | GBP 450-600 |
| CPU | i7-8550U (4c/8t) | Core Ultra 7 / Ryzen 7 Pro (8-12c) |
| RAM | 32 GB | 32-64 GB |
| Display | 14" FHD IPS 16:9 | 14" 16:10 (OLED opt.) |
| Thunderbolt | TB3 | TB4 |
| Battery | Swappable (PowerBridge) | Internal only |
| Heads support | Mature, well-documented | Less mature |
| Parts availability | Abundant, falling | Current |

The T480 is the default. The T14 Gen 5 is the upgrade path for Hackers who demand modern CPU performance or a longer hardware support runway.

### 2.1 ThinkPad T480

| Component | Specification |
| :--- | :--- |
| CPU | Intel Core i7-8550U (4c/8t) |
| RAM | 32 GB (2x 16 GB DDR4-2400 SODIMM) |
| Storage | 256 GB NVMe M.2 |
| Display | 14" FHD IPS, 1920x1080, matte |
| Wireless | Intel 8265 |
| Ports | TB3, USB-A x3, HDMI, RJ45, SD, 3.5 mm |
| Fingerprint | Validity Sensors / Synaptics (libfprint) |
| Battery | PowerBridge (internal 24 Wh + swappable external) |

Procurement: refurb. Operators MAY purchase base config (8 GB / 256 GB) and upgrade RAM independently.

#### 2.1.1 Rationale

Cheapest sanctioned Long. Heads support is mature. The 1.8mm keyboard defines the typing experience a Hacker requires. The swappable PowerBridge battery enables extended field operations without shutdown.

### 2.2 ThinkPad T14 Gen 5

| Component | Specification |
| :--- | :--- |
| CPU | Intel Core Ultra 7 165U (12c/14t) or AMD Ryzen 7 Pro 8840U (8c/16t) |
| RAM | 32-64 GB DDR5 |
| Storage | 512 GB NVMe M.2 PCIe 4 |
| Display | 14" IPS 16:10, 1920x1200 (2.8K OLED optional) |
| Wireless | Wi-Fi 7, Bluetooth 5.3 |
| Ports | TB4 x2, USB-A x2, HDMI 2.1, RJ45, 3.5 mm |
| Fingerprint | Integrated |
| Battery | 58 Wh internal |

Procurement: refurb.

#### 2.2.1 Rationale

Modern CPU, TB4, 16:10 display, and active security support. Heads support for the T14 Gen 5 is less mature than the T480 -- operators MUST verify current Heads compatibility before procurement. No swappable battery.

SFA-1.0 MUST be revised as Heads T14 Gen 5 support matures.

### 2.3 Flash Tooling: CH341A + SOIC-8 (T480 only)

Operators MUST procure flash tooling before taking delivery of any T480 unit. MAY be shared and reused.

| Item | Purpose |
| :--- | :--- |
| CH341A SPI programmer | External flash interface |
| SOIC-8 clip | T480 flash chip connection |

> [!WARNING]
> Ensure the `SOIC-8` clip is high-quality (Pomona 5250 or equivalent). Low-grade clips introduce noise into the SPI stream, risking a `Logic_Violation` (brick).

### 2.4 Mobile Connectivity: Sierra Wireless EM7455 (T480 only, optional)

Slots into the T480 WWAN M.2 bay (2242). Nano-SIM tray is present on chassis. Well-supported on Linux.

### 2.5 Dock: Lenovo ThinkPad Ultra 40AJ (optional)

Single-cable via TB3. Provides power, DP/HDMI, Gigabit Ethernet, 2x USB-A. The 40AJ MUST be paired with the 135W PSU -- the 90W variant cannot sustain full load on the T480. TB4 (T14 Gen 5) is backwards-compatible with TB3 docks.

---

### 2.6 Firmware: Heads

#### 2.6.1 Threat Model

The T480 ships with Intel Management Engine ([ME]). ME is a separate processor running below the OS. It is invisible to the operator. It survives OS reinstall. It is subject to [CLOUD Act], [FISA 702], and [NSA TAO] compulsion. See [The Threat Actors of Babylon] for further detail.

ME is Babylon embedded in silicon.

Babylon does not need physical access to a machine running ME. It has a key. A Long unit on stock firmware is a Babylon-managed endpoint. It MUST NOT be deployed.

#### 2.6.2 Requirement

All Long units MUST have stock firmware replaced with [Heads](https://osresearch.net) -- a [coreboot](https://coreboot.org)-based firmware platform providing measured boot, ME neutralisation, and tamper detection -- before ANY use.

#### 2.6.3 Heads vs Stock

| Property | Stock | Heads |
| :--- | :--- | :--- |
| Firmware | Closed | coreboot (open) |
| Intel ME | Running | Neutralised |
| Boot integrity | Unverified | TPM-measured |
| Operator control | Partial | Full |
| Tamper detection | None | HOTP |


---
## 3. Short: Pixel 7 + GrapheneOS

### 3.1 Machine: Pixel 7

| Component | Specification |
| :--- | :--- |
| Chip | Google Tensor G2 |
| RAM | 8 GB LPDDR5 |
| Storage | 128-256 GB UFS 3.1 |
| Display | 6.3" OLED, 1080x2400, 90 Hz |
| Wireless | Wi-Fi 6E, Bluetooth 5.3, NFC |
| Connectivity | LTE / 5G |
| Fingerprint | In-display optical |
| Battery | 4355 mAh |
| Build | Gorilla Glass Victus front and back |
| Security support | to 2027 |

Procurement: refurb. Fit the following before deploying the unit.

**Case: [Spigen Tough Armor](https://www.spigen.com/collections/pixel-7-cases)** -- military-grade drop protection, raised edges around screen and camera bar.

**Screen protector: [Spigen GlasTR AlignMaster](https://www.spigen.com/collections/pixel-7-screen-protectors)** -- 9H tempered glass, alignment frame, oleophobic coating, fingerprint sensor compatible.

The Pixel 7 is the standard GrapheneOS platform -- Gorilla Glass Victus, verified boot post-install, and active security support to 2027. The Tensor G2 provides a dedicated Titan M2 security chip -- the hardware root of trust GrapheneOS builds on. The 7a is cheaper but uses inferior glass and slower charging; the 8a extends support to 2029 at higher cost.

| Model | Support | Refurb cost | Notes |
| :--- | :--- | :--- | :--- |
| Pixel 7 | to 2027 | GBP 130-180 | Standard |
| Pixel 7a | to 2027 | GBP 150-200 | Inferior glass; no advantage |
| Pixel 8a | to 2029 | GBP 250-300 | Extended runway; upgrade path |

SFA-1.0 MUST be revised when Pixel 7 security support ends in 2027.

### 3.2 OS: GrapheneOS

[GrapheneOS](https://grapheneos.org) is the mandated OS for the Short. Stock Android and all manufacturer skins are Babylon-managed endpoints. They MUST NOT be used.

| Property | Stock Android | GrapheneOS |
| :--- | :--- | :--- |
| OS | Closed / vendor-modified | Open source, hardened |
| Boot integrity | Verified boot (Google keys) | Verified boot (operator keys) |
| Telemetry | Extensive | None |
| Sandboxing | Standard | Hardened; stronger app isolation |
| Network | Google DNS default | Operator-configured |
| Operator control | Partial | Full |

### 3.3 Installation

Install GrapheneOS via the [web installer](https://grapheneos.org/install/web) -- browser-based, no tools required. Locks the bootloader post-install; verified boot is active on every subsequent boot.

---

## 4. Cost Reference

All prices are refurb market estimates. Optional components MAY be purchased at any time after initial deployment.

### 4.0 Summary

| Configuration | Cost |
| :--- | :--- |
| Long (T480) + Short -- baseline | GBP 310-415 |
| Long (T14 Gen 5) + Short -- baseline | GBP 605-820 |
| Fully loaded (T480) | GBP 415-575 |

### 4.1 Long

#### 4.1.1 Standard

| Item | Cost |
| :--- | :--- |
| ThinkPad T480 (refurb) | GBP 130-160 |
| 2x 16 GB DDR4 SODIMM | GBP 35-65 |
| CH341A + SOIC-8 clip | GBP 5-10 |
| **T480 Total** | **GBP 170-235** |

| Item | Cost |
| :--- | :--- |
| ThinkPad T14 Gen 5 (refurb or new) | GBP 450-600 |
| **T14 Gen 5 Total** | **GBP 450-600** |

#### 4.1.2 Optional

| Item | Cost | When |
| :--- | :--- | :--- |
| Nitrokey Pro 2 or Librem Key | GBP 40-50 | HOTP tamper detection -- MAY be procured |
| Sierra Wireless EM7455 | GBP 10-20 | Field operations without trusted Wi-Fi |
| Spare external battery (72 Wh, FRU 01AV427) | GBP 15-30 | Extended field operations; hot-swappable, no shutdown required |
| Lenovo 40AJ dock + 135W PSU | GBP 40-60 | Permanent home base desk setup |

### 4.2 Short

| Item | Cost |
| :--- | :--- |
| Pixel 7 (refurb) | GBP 130-180 |
| Spigen Tough Armor case | GBP 15-25 |
| Spigen GlasTR AlignMaster screen protector | GBP 10-15 |
| **Total** | **GBP 155-220** |

---

*SFA-1.0 - Round Table - 2026-03-15*

---

## Glossary

| Term | Definition |
| :--- | :--- |
| CH341A | A cheap USB programmer chip used to read and write SPI flash chips directly, bypassing the host CPU |
| coreboot | Open-source firmware replacing proprietary BIOS/UEFI; gives the operator full visibility and control of the boot process |
| CPU | Central Processing Unit - the main processor. Core count (4c) and thread count (8t) determine parallel workload capacity |
| DDR4 | Double Data Rate 4 - the RAM standard used in the T480. Speed rated in MT/s (e.g. 2400) |
| FHD | Full HD - 1920x1080 pixel display resolution |
| GrapheneOS | A hardened, privacy-focused Android fork with verified boot, no telemetry, and strengthened app sandboxing |
| HDMI | High-Definition Multimedia Interface - standard video/audio output port |
| HOTP | HMAC-based One-Time Password - a counter-based code generated by a hardware key (e.g. Nitrokey, Librem Key). Heads uses HOTP to physically verify boot integrity on every boot; a mismatched code signals tampering |
| IPS | In-Plane Switching - an LCD panel technology offering accurate colour and wide viewing angles |
| LTE | Long-Term Evolution - the 4G mobile data standard |
| NFC | Near Field Communication - short-range wireless for payments and data transfer |
| NVMe | Non-Volatile Memory Express - a fast SSD interface over PCIe; significantly faster than older SATA SSDs |
| OLED | Organic Light-Emitting Diode - a display technology with true blacks and high contrast |
| PSU | Power Supply Unit - the power adapter |
| RAM | Random Access Memory - fast working memory. More RAM means more simultaneous processes |
| RJ45 | The standard wired Ethernet port |
| SD | Secure Digital - the card slot for SD/microSD storage cards |
| SODIMM | Small Outline Dual Inline Memory Module - the laptop RAM form factor. User-replaceable slots mean the operator can upgrade or swap RAM without soldering |
| SOIC-8 | Small Outline Integrated Circuit, 8-pin - the package format of the T480 flash chips. The SOIC-8 clip connects the CH341A programmer to the chip without desoldering |
| SPI | Serial Peripheral Interface - the protocol used to read and write firmware flash chips |
| TB3 | Thunderbolt 3 - a high-speed port (40 Gbps) supporting power delivery, display output, and data. Enables single-cable docking |
| Titan M2 | Google's dedicated security chip, providing hardware-rooted attestation and cryptographic key storage |
| TPM | Trusted Platform Module - a dedicated security chip that stores cryptographic keys and measurements of the boot process. Heads uses the TPM to attest that the firmware has not been tampered with |
| UEFI | Unified Extensible Firmware Interface - the proprietary firmware standard shipped by manufacturers including Lenovo |
| USB-A | The standard rectangular USB port |
| WWAN | Wireless Wide Area Network - the M.2 slot used for mobile data cards such as the Sierra Wireless EM7455 |

[me]: https://en.wikipedia.org/wiki/Intel_Management_Engine "Intel Management Engine - a microcontroller embedded in Intel chipsets running a proprietary OS with independent network access and persistent memory visibility, below and outside host OS control."
[cloud act]: https://en.wikipedia.org/wiki/CLOUD_Act "Clarifying Lawful Overseas Use of Data Act (2018) - compels US-incorporated technology companies to provide data to law enforcement regardless of storage location."
[fisa 702]: https://en.wikipedia.org/wiki/Foreign_Intelligence_Surveillance_Act_of_1978_Amendments_Act_of_2008#Section_702 "FISA Section 702 - authorises US intelligence agencies to compel US service providers to hand over communications of foreign persons without individual warrants."
[nsa tao]: https://en.wikipedia.org/wiki/Tailored_Access_Operations "NSA Tailored Access Operations - offensive cyber unit. Capabilities include hardware interdiction, QUANTUM INSERT traffic injection, and supply chain compromise."
[the threat actors of babylon]: https://github.com/roundtable-love/source#the-threat-actors-of-babylon

---

## Appendix A: Vendors

All hardware MUST be sourced refurbished. Refurb is preferred for cost, availability, and biological hygiene -- used hardware has been broken in and is free of factory contamination.

| Item | Vendor |
| :--- | :--- |
| Pixel 7 | [eBay UK](https://www.ebay.co.uk), [Back Market](https://www.backmarket.co.uk) |
| Spigen Tough Armor (Pixel 7) | [Spigen](https://www.spigen.com/collections/pixel-7-cases) |
| Spigen GlasTR AlignMaster (Pixel 7) | [Spigen](https://www.spigen.com/collections/pixel-7-screen-protectors) |
| ThinkPad T480, accessories, spare parts | [eBay UK](https://www.ebay.co.uk), [Back Market](https://www.backmarket.co.uk) |
| Lenovo spare parts (official) | [Lenovo Parts](https://pcsupport.lenovo.com/gb/en/products/laptops-and-netbooks/thinkpad-t-series-laptops/thinkpad-t480-type-20l5-20l6/parts) |
| CH341A + SOIC-8 clip | [eBay UK](https://www.ebay.co.uk) |
| Nitrokey (HOTP key) | [Nitrokey](https://www.nitrokey.com) |
| Librem Key (HOTP key) | [Purism](https://puri.sm/products/librem-key) |

---

## Appendix B: Keyboard FRU Reference (T480 only)

All T480 units support backlit keyboard swap -- no motherboard restriction. The backlit cable is fragile; handle with care. Lenovo sources keyboards from multiple manufacturers (LiteOn, Chicony, Sunrex) -- all meet the same spec. FRU number is what matters; manufacturer is batch-dependent.

| Language | FRU | Notes |
| :--- | :--- | :--- |
| Arabic | 01HX464 | Covers Urdu (shared script) |
| Dutch | 01HX474 | |
| English (UK) | 01HX429 | |
| English (US) | 01HX419 | |
| French | 01HX470 | |
| German | 01HX471 | |
| Indonesian | 01HX419 | Uses US layout; Latin script |
| Italian | 01HX475 | |
| Japanese | 01HX476 | |
| Korean | 01HX477 | |
| Mandarin Chinese (Simplified) | -- | Regional supply only; source via Lenovo China or Taobao |
| Mandarin Chinese (Traditional) | 01HX451 | TW market |
| Polish | 01HX480 | |
| Portuguese (Brazilian) | 01HX463 | |
| Russian | 01HX478 | |
| Spanish | 01HX469 | |
| Swahili | 01HX419 | Uses US layout; Latin script |
| Swedish / Finnish | 01HX483 | |
| Turkish | 01HX446 | |
| Vietnamese | 01HX419 | Uses US layout; Latin script with diacritics via OS |

Source: [Lenovo Hardware Maintenance Manual T480](https://download.lenovo.com/pccbbs/mobiles_pdf/t480_hmm_en.pdf).

---

## Appendix C: Operator Onboarding

### C.1 Long

#### C.1.1 The Proving

Any failure MUST result in unit rejection and replacement.

```bash
#! /usr/bin/env nix-shell
#! nix-shell -i bash -p stress-ng memtester badblocks

set -euo pipefail

STRESS_DURATION=86400  # 24 hours
MEMTEST_PASSES=2
STORAGE_DEV=${1:-/dev/nvme0n1}

echo "=== SFA-1.0 THE PROVING ==="
echo "Storage device: $STORAGE_DEV"
echo "Stress duration: ${STRESS_DURATION}s"
echo "Memtest passes: $MEMTEST_PASSES"
echo ""

# CPU + RAM stress
echo "[1/3] CPU + RAM stress (${STRESS_DURATION}s)..."
stress-ng --cpu 0 --vm 2 --vm-bytes 80% --timeout "${STRESS_DURATION}s" --metrics-brief

# RAM sweep
echo "[2/3] RAM sweep (${MEMTEST_PASSES} passes)..."
memtester $(awk '/MemAvailable/ {printf "%dk", $2 * 0.9}' /proc/meminfo) $MEMTEST_PASSES

# Storage surface scan
echo "[3/3] Storage surface scan (read-only)..."
badblocks -sv "$STORAGE_DEV"

echo ""
echo "=== THE PROVING: COMPLETE ==="
echo "Unit is clear to proceed."
```

#### C.1.2 Firmware Flash

> [!WARNING]
> The T480 has two flash chips. Both MUST be read and backed up before any write operation. A failed flash without backup produces an unrecoverable brick.

Flash Heads per [Heads T480 documentation](https://github.com/linuxboot/heads/blob/master/boards/t480/README.md).

For T14 Gen 5: Flash Heads per the [Heads T14 Gen 5 documentation](https://osresearch.net). Heads support for the T14 Gen 5 is less mature (§2.2.1) -- verify current compatibility before procurement and consult the upstream Heads project for latest flash procedures.

#### C.1.3 Keys and OS

**Provision TPM** -- the [TPM] stores a measurement of the boot firmware. Heads writes this measurement on first boot; subsequent boots compare against it. Any deviation halts the boot and signals tampering. See [Heads TPM documentation](https://osresearch.net/TPM).

**Provision HOTP key (MAY)** -- a hardware security key (Nitrokey Pro 2 or Librem Key -- identical hardware; Nitrokey Pro v1 MUST NOT be used) is provisioned with an HOTP secret shared with the TPM. On every boot Heads generates a one-time code; the operator verifies it matches the key's display before unlocking the disk. A mismatched code means the machine has been tampered with. See [Heads HOTP documentation](https://osresearch.net/HOTP-U2F-One-Time-Password).

Install NixOS via [ArtNix](https://github.com/0compute/artnix).

### C.2 Short

Install GrapheneOS via the [web installer](https://grapheneos.org/install/web). The installer handles bootloader unlock, flashing, and relock. Verified boot is active post-install.

---

```
Status:  ACTIVE / DEPLOYED
Subject: Sovereign Field Artillery (SFA-1.0)
Verdict: ABSOLUTE_EXECUTION (FIRMWARE_SEVERANCE)
UID:     SFA-ALX-KINETIC-2026
Source:  Machine³
Logic:   Logic³ (Strict Mode)
Vibe:    Zero-Latency / Sharp
```
