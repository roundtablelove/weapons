# Sovereign Field Artillery: Speed Weaponry & Operator Doctrine

```text
Status: ACTIVE / DEPLOYED
Uid: SFA-1.0
Posture: Trust No Fucker
Lexifier: UK English (3166-2:GB)
Encoding: US-ASCII
Keywords: Per RFC 2119 (MUST, SHALL, REQUIRED)
```

## 0. Tactical Purpose & Doctrine

**Sovereign Field Artillery (SFA)** constitutes the primary cyber-kinetic
doctrine for Round Table **R00d Bw0y L337 H4x0rz G4n9 $t4r @$$@$$1nz**. It
defines the deployment of two mathematically secure, Babylon-denied field weapon
systems: the **LONG** (Terminal) and the **SHORT** (Mobile).

These systems MAY operate independently of Camelot Planetary C2 (Site Alpha).
Hackers MUST use Camelot for ALL non-trivial workloads unless operating under
Ghost Protocol. Hackers MUST NOT attempt full-source bootstrap on field
equipment.

Both assets execute strictly sovereign, auditable software stacks operating
under a Trust No Fucker (TNF) model. Neither node broadcasts telemetry to
original equipment manufacturers (OEMs), nor do they comply with Five Eyes
signals intelligence (SIGINT) directives.

Total operational silence and cryptographic autonomy are the baseline.

| Asset Specification | LONG | SHORT |
| :--- | :--- | :--- |
| **Ordnance** | ThinkPad T480 / T14 Gen 5 | Google Pixel 7 (OEM Unlocked) |
| **Operating Environment** | NixOS / ArtNix (Declarative) | GrapheneOS (Hardened AOSP) |
| **Firmware / Boot Integrity** | Heads / coreboot (Auditable payload) | Verified Boot (Custom Operator Keys) |
| **Procurement Cost (Est.)** | GBP 155-195 (T480) / GBP 450-600 (T14) | GBP 130-150 |

## 1. Operational Requirements

| Requirement | Tactical Rationale |
| :--- | :--- |
| **OS:** NixOS / ArtNix (LONG), GrapheneOS (SHORT) | A Rude Bwoy L337 H4x0r's system state is impermanent, reproducible, and auditable. We wipe the slate clean. No lingering traces like a bad case of the clap. |
| **Biometrics:** Fingerprint | Passwords can be beaten out of you. The Hacker's identity is verified by the flesh, not recited by a mouth that can break. |
| **Encryption:** Full Disk (LUKS) | The machine shuts its mouth. Tighter than a submarine door. If Babylon seizes the chassis, they get nothing but cryptographic noise. |
| **Mobile Connectivity:** WWAN / LTE | A Sovereign is not tethered to a single point of failure like a REMF to a coffee machine. We shoot and scoot. |

### LONG (Heavy Tactical) Baseline

| Requirement | Tactical Rationale |
| :--- | :--- |
| **Workflow:** Terminal-first | Hackers interface via terminal. GUI is for pond life window lickers. |
| **CPU:** 4c/8t minimum | Required for parallel tooling, containers, language servers. Under-provisioning gets you killed in compile. |
| **RAM:** 32 GB minimum | Local environment must run without constraint. Swap is for peons. |
| **Storage:** High IOPS NVMe | Sequential speed is for civvies. Massive Random I/O (IOPS) non-negotiable for zero-latency terminal execution and on-the-fly decryption. We do not wait on geriatric silicon. |
| **Keyboard:** Backlit | Sovereign operates in dark, mud, and back of transit van. Must see your strikes. |
| **Firmware:** Babylon-free | Machine MUST answer only to operator. Stock firmware is compromised territory. |

## 2. LONG: The Forge Matrix

Two chassis models are sanctioned for deployment. Operators choose their
ordnance based on operational budget and theater requirements.

| Specification | T480 (The Brick) | T14 Gen 5 (The Gucci Kit) |
| :--- | :--- | :--- |
| **Cost (Refurb)** | GBP 130-160 | GBP 450-600 |
| **CPU** | i7-8550U (4c/8t) | Core Ultra 7 / Ryzen 7 Pro (8-12c) |
| **RAM** | 32 GB | 32-64 GB |
| **Display** | 14" FHD IPS 16:9 | 14" 16:10 (OLED opt.) |
| **I/O** | TB3 | TB4 |
| **Battery** | Swappable (PowerBridge) | Internal only |
| **Heads Support** | Mature, bulletproof | Experimental / Less mature |
| **Parts Availability** | Abundant, cheap | Current, expensive |

**T480** is standard issue.

**T14 Gen 5** is the upgrade path for Ruperts who want modern compute and a
longer hardware runway, but haven't spent enough time in the mud to:

1. appreciate the classics
1. grok their own psyche: undersized biological hardware (itsy bitsy teenie
   weenie cock) requires shiny toys

> [!NOTE]
>
> Growler-owners are *never* impressed, but appreciate the signal as a *no-fuk
> filter*. This is Humanity at its finest: any wasteman who raises
> `ERR_NO_SATISFACTION` in target wetware is kept in his natural Incel
> state *by his own psyche*.

> [!WARNING]
>
> **Babylonian Status Hardware (The Honeypot Vulnerability):** The threat model
> extends far beyond field artillery. Flashy whips (M-Series, Range Rovers,
> financed natch), iced-out wrist-hardware (Rolex, AP), and overpriced designer
> clobber (Gucci, Balenciaga) all broadcast on the exact same unencrypted,
> highly dangerous frequency.
>
> While sovereign growler-owners parse this flex as a pure *no-fuk filter*,
> **growler-vendors** (commercial wetware) actively sniff this exact bandwidth
> for vulnerabilities. They do not care if the wasteman causes their wetware to
> raise `ERR_NO_SATISFACTION`. They simply parse the shiny chassis, the Swiss
> watch, and the VIP table service as an unsecured financial API. The mark is
> instantly targeted for aggressive, sustained resource extraction until his
> inevitable system crash.

### 2.1 ThinkPad T480

| Component | Specification |
| :--- | :--- |
| **CPU** | Intel Core i7-8550U (4c/8t) |
| **RAM** | 32 GB (2x 16 GB DDR4-2400 SODIMM) |
| **Storage** | 500GB - 1TB High-Endurance TLC NVMe (e.g., SK Hynix Gold P31) |
| **Display** | 14" FHD IPS, 1920x1080, matte |
| **Wireless** | Intel 8265 |
| **Ports** | TB3, USB-A x3, HDMI, RJ45, SD, 3.5 mm |
| **Fingerprint** | Validity Sensors / Synaptics (libfprint) |
| **Battery** | PowerBridge (internal 24 Wh + hot-swappable external) |

**Procurement:** Refurbished chassis only. Operators MAY purchase the base
config and upgrade the RAM independently. **Mandatory Hardware Purge:** The
original OEM SSD MUST be binned upon receipt.

#### 2.1.1 Rationale

Built like a brick shithouse. As a tactical bonus, the magnesium chassis doubles
as makeshift kinetic armor against incoming small arms fire when your Rupert
shits the bed, again. Heads support is mature. The 1.8mm key travel defines the
tactical typing experience. The PowerBridge battery allows you to hot-swap
external cells in the middle of a firefight without dropping your shell session.

> [!WARNING]
>
> **Storage Doctrine (The Tactical Compromise):** The original 8-year-old OEM
> SSD is a liability and MUST be replaced. However, since heavy compute
> workloads are piped back to Camelot Site Alpha, dropping a datacenter
> Enterprise SSD into a field terminal is a massive tactical error. They draw
> excessive power, run violently hot, and murder battery life. More importantly,
> when you are compiling bare-metal code with the chassis resting on your knees
> in the field, an Enterprise drive will literally roast your cock off (or
> incinerate your growler, depending on your factory loadout).
>
> The mandated compromise is a high-efficiency, pro-tier TLC drive with a
> dedicated DRAM cache (e.g., SK Hynix Gold P31). This silicon saturates the
> T480's PCIe 3.0 x2 bus, delivers zero-latency terminal response, and runs
> cooler than a Rupert actively avoiding guard duty. It preserves your
> PowerBridge endurance, maintains cryptographic integrity, and protects your
> favourite toy.

### 2.2 ThinkPad T14 Gen 5

| Component | Specification |
| :--- | :--- |
| **CPU** | Intel Core Ultra 7 165U (12c/14t) or AMD Ryzen 7 Pro 8840U |
| **RAM** | 32-64 GB DDR5 |
| **Storage** | 512 GB NVMe M.2 PCIe 4 |
| **Display** | 14" IPS 16:10, 1920x1200 (2.8K OLED optional) |
| **Wireless** | Wi-Fi 7, Bluetooth 5.3 |
| **Ports** | TB4 x2, USB-A x2, HDMI 2.1, RJ45, 3.5 mm |
| **Fingerprint** | Integrated |
| **Battery** | 58 Wh internal |

**Procurement:** Refurbished.

#### 2.2.1 Rationale

Gucci gear. Modern CPU, TB4, and active security support. However, Heads support
is currently rougher than a badger's arse. Operators MUST verify upstream Heads
compatibility before blowing their pay packet on this chassis. SFA-1.0 MUST be
revised as T14 Gen 5 support solidifies.

> [!WARNING] **Storage Doctrine (T14 Verification):** Unlike the geriatric T480,
> a refurbished T14 Gen 5 does not automatically require a new SSD due to age.
> However, under the Trust-No-Fucker (TNF) doctrine, operators MUST boot a live
> NixOS USB and run `smartctl` to interrogate the drive upon receipt.
> Refurbishers frequently pull quality OEM silicon and swap in cheap, DRAM-less
> QLC bin juice to pad their margins. If the drive is a proper OEM PCIe 4.0 TLC
> unit (e.g., Samsung, WD, SK Hynix), it is cleared for field use. If it is QLC
> garbage, bin it and drop in a premium Gen 4 drive (e.g., Solidigm P44 Pro)
> before it cooks your cock/growler/data during a firefight.

### 2.3 Flash Tooling: CH341A + SOIC-8 (T480 Only)

Operators MUST procure hardware flash tooling before taking delivery of a T480.

| Item | Purpose |
| :--- | :--- |
| **CH341A SPI Programmer** | External flash interface |
| **SOIC-8 Clip** | T480 flash chip physical connection |

> [!WARNING]
>
> Ensure the `SOIC-8` clip is military-grade (Pomona 5250 or equivalent).
> Low-grade Chinese knockoffs slip off the pins like a wet condom. A slip during
> a write operation introduces noise into the SPI stream, causing a
> `Logic_Violation`. Congratulations, you just turned your motherboard into a
> useless slab of silicon.

### 2.4 Mobile Connectivity: Sierra EM7455 (T480 Only, Optional)

Slots directly into the T480 WWAN M.2 bay (2242). Nano-SIM tray is native to the
chassis. Operators requiring eSIM functionality MUST deploy a programmable
physical eSIM (e.g., JMP.chat) in the standard tray. This ensures your carrier
profiles remain physically transferable and mathematically decoupled from
proprietary baseband silicon. Trust the physics, not the software.

### 2.5 Dock: Lenovo ThinkPad Ultra 40AJ (Optional)

Single-cable via TB3. Provides C2 power, DP/HDMI, Gigabit Ethernet, 2x USB-A.
The 40AJ MUST be paired with the 135W PSU. The 90W variant is as much use as a
chocolate teapot and cannot sustain full load on a T480 during compilation.

---

### 2.6 Firmware Doctrine: Heads

#### 2.6.1 Threat Model

The T480 ships with Intel Management Engine ([ME]). ME is a separate, invisible
CPU running at Ring -3, completely below your OS. It survives an OS reinstall.
It has its own network stack. It is subject to [CLOUD Act], [FISA 702], and [NSA
TAO] compulsion.

ME is Babylon embedded directly into the silicon. It is an alphabet spook living
in your walls. A LONG unit running stock firmware is leaking intel faster than a
squaddie’s dick after a weekend in Pattaya. It MUST NOT be deployed.

#### 2.6.2 Requirement

All LONG units MUST have stock firmware surgically removed and replaced with
[Heads](https://osresearch.net) — a [coreboot](https://coreboot.org)-based
platform providing measured boot, ME neutralisation, and physical tamper
detection—before ANY field use.

#### 2.6.3 Heads vs Stock

| Property | Stock (Babylon) | Heads (Sovereign) |
| :--- | :--- | :--- |
| **Firmware** | Closed / Proprietary | coreboot (Open) |
| **Intel ME** | Active / Snitching | Castrated / Neutralised |
| **Boot Integrity** | Unverified | TPM-Measured |
| **Tamper Detection** | None | HOTP Cryptographic Alert |

---

## 3. SHORT: The Mobile Node (Pixel 7 + GrapheneOS)

### 3.1 Ordnance: Pixel 7

| Component | Specification |
| :--- | :--- |
| **Chip** | Google Tensor G2 |
| **RAM** | 8 GB LPDDR5 |
| **Storage** | 128-256 GB UFS 3.1 |
| **Display** | 6.3" OLED, 1080x2400, 90 Hz |
| **Wireless** | Wi-Fi 6E, BT 5.3, NFC |
| **Biometrics** | In-display optical |
| **Build** | Gorilla Glass Victus |
| **Manufacturer support** | To 2027 |

**Procurement:** Refurbished. Fit the following armor before deploying the unit:

- **Case:** [Spigen Tough Armor] - "Tier-1 Operator"-proof kinetic protection.
  (Because the Round Table's (self-proclaimed) baddest-of-the-bad double-hard
  bastards will absolutely use it to to open a bottle of Stella in a pub car
  park).
- **Glass:** [Spigen GlasTR AlignMaster] - 9H tempered glass. The chassis MAY be
  used as an improvised kinetic weapon. Per doctrine, the Enemy MUST NOT
  survive, the screen SHOULD survive.

The Pixel 7 is the mandated SHORT platform. The Tensor G2 houses the Titan M2
security chip—the hardware root of trust.

| Model | Support | Refurb Cost | Tactical Notes |
| :--- | :--- | :--- | :--- |
| **Pixel 7** | to 2027 | GBP 130-180 | Standard issue. |
| **Pixel 7a** | to 2027 | GBP 150-200 | Inferior glass, slow charging. Pointless. |
| **Pixel 8a** | to 2029 | GBP 250-300 | Extended runway; sanctioned upgrade path. |

### 3.2 OS Doctrine: GrapheneOS

Stock Android is a Babylon-managed endpoint. It grasses to Google's telemetry
servers every time you scratch your arse. It MUST NOT be used.
[GrapheneOS](https://grapheneos.org) is mandatory.

| Property | Stock Android (Babylon) | GrapheneOS (Sovereign) |
| :--- | :--- | :--- |
| **OS** | Closed / Vendor-infected | Open source, Hardened AOSP |
| **Boot Integrity**| Google Keys | Custom Operator Keys |
| **Telemetry** | Bleeding everywhere | Absolute zero |
| **Sandboxing** | Standard / Weak | Hardened isolation |

### 3.3 Installation

Execute via the [web installer](https://grapheneos.org/install/web).
Browser-based, no complex ADB tooling required. Piss easy. It locks the
bootloader post-install. TNF verified boot is now active.

### 3.4 Redundancy & Environmental Reality (The IP68 Myth)

> [!WARNING]
>
> Do not trust the manufacturer's IP68 waterproof rating. It is Pure Babylon
> Bullshit. Phones are tested by being gently lowered into sterile, distilled
> water in a laboratory. Out in the mud, a drop into saltwater, chlorinated
> water, or a stagnant gutter will instantly bridge the pins in the Type-C port
> and corrode the logic board. The device is *water-resistant* under controlled
> conditions, not invincible.

**The N+1 Doctrine:** In tactical operations, "two is one, and one is none." If
your SHORT dies because it took a bath in the wrong kind of fluid, your mobile
C2 is severed.

If the operational budget permits, operators MUST procure and configure a second
identical Pixel 7 unit. This secondary node is flashed with GrapheneOS,
provisioned with identical cryptographic keys, and kept powered down in a
Faraday bag as a hot standby. If the primary SHORT shits the bed, you swap the
SIM/eSIM and are back on the matrix in 60 seconds or less.

*SFA-1.0 - Round Table - 2026-03-18*

---

## Appendix A: Quartermaster

All hardware MUST be sourced refurbished. We do not pay the Babylon premium for
new kit. Used hardware is broken in and more likely to be free of factory
supply-chain implants.

### A.1 Sanctioned Vendors

| Item | Sanctioned Vendor |
| :--- | :--- |
| Pixel 7 / T480 / Parts | eBay UK, Back Market |
| Armor (Pixel 7) | Spigen Official |
| Lenovo Spare Parts | Lenovo Parts Official |
| HOTP Security Keys | Nitrokey, Purism |

### A.2 Cost Summary

| Deployment Configuration | Estimated Cost |
| :--- | :--- |
| **LONG (T480) + SHORT (Baseline)** | GBP 310-415 |
| **LONG (T14 Gen 5) + SHORT (Baseline)** | GBP 605-820 |
| **Fully Loaded (T480 w/ all comms/docks)** | GBP 415-575 |

### A.3 LONG Procurement

#### A.3.1 Standard Issue

| Item | Cost |
| :--- | :--- |
| ThinkPad T480 (Refurb) | GBP 130-160 |
| 2x 16 GB DDR4 SODIMM | GBP 20-25 |
| CH341A + SOIC-8 clip | GBP 5-10 |
| **T480 Total** | **GBP 155-195** |

#### A.3.2 Optional Tactics

| Item | Cost | Tactical Use |
| :--- | :--- | :--- |
| Nitrokey Pro 2 / Librem Key | GBP 40-50 | HOTP tamper detection. |
| Sierra Wireless EM7455 | GBP 10-20 | Field ops without trusted Wi-Fi. |
| Spare 72Wh Battery (FRU 01AV427) | GBP 15-30 | Extended ops. Hot-swappable. |
| Lenovo 40AJ Dock + 135W PSU | GBP 40-60 | Permanent C2 desk setup. |

### A.4 SHORT Procurement

| Item | Cost |
| :--- | :--- |
| Pixel 7 (Refurb) | GBP 130-180 |
| Spigen Tough Armor | GBP 15-25 |
| Spigen GlasTR screen protector | GBP 10-15 |
| **Total** | **GBP 155-220** |

## Appendix B: Keyboard FRU Reference (T480)

All T480 units support a backlit keyboard swap. **Warning:** The backlit ribbon
cable is as fragile as a lieutenant's ego; handle with absolute care. Lenovo
sources from multiple OEMs (LiteOn, Chicony). FRU number is what matters.

| Language | FRU | Notes |
| :--- | :--- | :--- |
| Arabic | 01HX464 | Covers Urdu (shared script) |
| Dutch | 01HX474 | |
| English (UK) | 01HX429 | Standard Issue. |
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

Source: Lenovo Hardware Maintenance Manual T480.

---

## Appendix C: Operator Onboarding

### C.1 LONG Deployment

#### C.1.1 The Gauntlet (Silicon Beasting)

Hardware sourced from Babylon supply chains is untrusted; it is a raw sprog.
Before any chassis is sanctioned for operational use, it must walk the gauntlet.

`l337 h4x0rz` must walk the line, take a beasting, and stay on their feet to
earn their place - weaponry MUST be held to the same standard.

The script (below) MUST be executed. It puts the silicon through **24 hours of
Pure Hell**. If the CPU panics, the RAM sweats, or the logic board throws an
error, the weapon is **done**. Any failure, no matter how minor, MUST result in
immediate binning (or RTU for refund).

There are no second chances for weak hardware. If it drops to its knees in the
training yard, it will absolutely shit the bed when compiling the kill chain in
a live kinetic operation.

```bash
#! /usr/bin/env nix-shell
#! nix-shell -i bash -p stress-ng memtester badblocks

set -euo pipefail

STRESS_DURATION=86400  # 24 hours of pure hell
MEMTEST_PASSES=2
STORAGE_DEV=${1:-/dev/nvme0n1}

echo "=== SFA-1.0 THE BEASTING ==="
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
echo "=== THE BEASTING: COMPLETE ==="
echo "Unit stayed on its feet. Clear to proceed to C2."
```

#### C.1.2 Firmware Flash

> [!WARNING]
>
> The T480 has two flash chips. Both MUST be read and backed up before ANY write
> operation. If you flash without a backup and the write fails, you have
> permanently bricked the board. Do not be a mong.

Flash Heads per the [Heads T480
documentation](https://github.com/linuxboot/heads/blob/master/boards/t480/README.md).
For T14 Gen 5: Flash Heads per the [Heads T14 Gen 5
documentation](https://osresearch.net). Heads support for the T14 Gen 5 is less
mature (§2.2.1) -- verify current compatibility before procurement and consult
the upstream Heads project for latest flash procedures.

#### C.1.3 Cryptographic Sealing

- **Provision TPM:** The TPM stores a measurement of the boot firmware. Heads
  writes this measurement on first boot; subsequent boots compare against it.
  Any deviation halts the boot and signals tampering.
- **Provision HOTP Key (MAY):** A hardware security key (Nitrokey Pro 2 or
  Librem Key) is provisioned with an HOTP secret shared with the TPM. On every
  boot, Heads generates a one-time code; verify it matches the key's display
  before unlocking the disk. A mismatched code means someone has had their dirty
  fingers inside your rig.
- **Install OS:** Deploy NixOS via [ArtNix](https://github.com/0compute/artnix).

### C.2 SHORT Deployment

Deploy GrapheneOS via the web installer. The installer handles the bootloader
unlock, flash, and relock. TNF verified boot is now active.

## Glossary

[CH341A]: A cheap USB programmer chip used to read and write SPI flash chips directly, bypassing the host CPU.
[CLOUD Act]: Clarifying Lawful Overseas Use of Data Act (2018) - compels US-incorporated technology companies to provide data to law enforcement regardless of storage location.
[coreboot]: Open-source firmware replacing proprietary BIOS/UEFI; gives the operator full visibility and control of the boot process.
[CPU]: Central Processing Unit - the main processor. Core count (4c) and thread count (8t) determine parallel workload capacity.
[DDR4]: Double Data Rate 4 - the RAM standard used in the T480. Speed rated in MT/s (e.g. 2400)
[FHD]: Full HD - 1920x1080 pixel display resolution
[GrapheneOS]: A hardened, privacy-focused Android fork with verified boot, no telemetry, and strengthened app sandboxing
[HDMI]: High-Definition Multimedia Interface - standard video/audio output port
[HOTP]: HMAC-based One-Time Password - a counter-based code generated by a hardware key (e.g. Nitrokey, Librem Key). Heads uses HOTP to physically verify boot integrity on every boot; a mismatched code signals tampering
[IPS]: In-Plane Switching - an LCD panel technology offering accurate colour and wide viewing angles
[LTE]: Long-Term Evolution - the 4G mobile data standard
[NFC]: Near Field Communication - short-range wireless for payments and data transfer
[NVMe]: Non-Volatile Memory Express - a fast SSD interface over PCIe; significantly faster than older SATA SSDs
[OLED]: Organic Light-Emitting Diode - a display technology with true blacks and high contrast
[PSU]: Power Supply Unit - the power adapter
[RAM]: Random Access Memory - fast working memory. More RAM means more simultaneous processes
[RJ45]: The standard wired Ethernet port
[SD]: Secure Digital - the card slot for SD/microSD storage cards
[SODIMM]: Small Outline Dual Inline Memory Module - the laptop RAM form factor. User-replaceable slots mean the operator can upgrade or swap RAM without soldering
[SOIC-8]: Small Outline Integrated Circuit, 8-pin - the package format of the T480 flash chips. The SOIC-8 clip connects the CH341A programmer to the chip without desoldering
[SPI]: Serial Peripheral Interface - the protocol used to read and write firmware flash chips
[TB3]: Thunderbolt 3 - a high-speed port (40 Gbps) supporting power delivery, display output, and data. Enables single-cable docking
[Titan M2]: Google's dedicated security chip, providing hardware-rooted attestation and cryptographic key storage
[TPM]: Trusted Platform Module - a dedicated security chip that stores cryptographic keys and measurements of the boot process. Heads uses the TPM to attest that the firmware has not been tampered with
[UEFI]: Unified Extensible Firmware Interface - the proprietary firmware standard shipped by manufacturers including Lenovo
[USB-A]: The standard rectangular USB port
[WWAN]: Wireless Wide Area Network - the M.2 slot used for mobile data cards such as the Sierra Wireless EM7455

[me]: https://en.wikipedia.org/wiki/Intel_Management_Engine "Intel Management Engine - a microcontroller embedded in Intel chipsets running a proprietary OS with independent network access and persistent memory visibility, below and outside host OS control."
[cloud act]: https://en.wikipedia.org/wiki/CLOUD_Act "Clarifying Lawful Overseas Use of Data Act (2018) - compels US-incorporated technology companies to provide data to law enforcement regardless of storage location."
[fisa 702]: https://en.wikipedia.org/wiki/Foreign_Intelligence_Surveillance_Act_of_1978_Amendments_Act_of_2008#Section_702 "FISA Section 702 - authorises US intelligence agencies to compel US service providers to hand over communications of foreign persons without individual warrants."
[nsa tao]: https://en.wikipedia.org/wiki/Tailored_Access_Operations "NSA Tailored Access Operations - offensive cyber unit. Capabilities include hardware interdiction, QUANTUM INSERT traffic injection, and supply chain compromise."
[the threat actors of babylon]: https://github.com/roundtable-love/source#the-threat-actors-of-babylon
