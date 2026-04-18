# JTEC 68HC16 XDF v30 — Address Map & Verification Report

**Binary:** v130_flash (firmware 102397) | **XDF:** v30 | **Total entries:** 120 (101 tables + 19 scalars)


---


## Verification Legend

| Symbol | Meaning |
|:---:|:---|
| ✅ **Confirmed** | Address matches a real binary table header via code path verification |
| 🔶 **Code-linked, name unverified** | Address points at a real code-referenced table, but purpose not yet traced |
| 📎 **Axis ref** (read-only) | Normalizer/axis table — editing misaligns dependent lookups |
| ⚠️ **Unverified** | Title-flagged unverified in XDF; caution |
| ❌ **No code link** | No LDX pointer in binary — requires investigation |

---


## Part 1 — Tables (grouped by category)


### Fuel - Warmup/Enrichment  (6 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$2724` | Table | ECT Normalizer $2724 (9pt, alt) [READ-ONLY] | 9×2 × 8b | 📎 Axis ref (read-only) |
| `$2B87` | Table | Base Fuel PW EGR Off | 17×9 × 16b | ✅ Confirmed |
| `$2CBD` | Table | Base Fuel PW EGR On | 17×9 × 16b | ✅ Confirmed |
| `$2F13` | Table | Fuel Multiplier RPM | 17×2 × 8b | ✅ Confirmed |
| `$33F3` | Table | ECT Normalizer $33F3 (9pt, dup) [READ-ONLY] | 9×2 × 8b | 📎 Axis ref (read-only) |
| `$3CCE` | Table | ECT Normalizer $3CCE (9pt) [READ-ONLY] | 9×2 × 8b | 📎 Axis ref (read-only) |

### Fuel - Injector  (5 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$26A9` | Table | After-Start Enrich ECT | 8×2 × 8b | ✅ Confirmed |
| `$2E03` | Table | Air Enrichment Factor | 9×2 × 8b | ✅ Confirmed |
| `$2E53` | Table | Part Throttle Enrichment | 17×9 × 8b | ✅ Confirmed |
| `$2FC8` | Table | Warmup Enrichment Time | 9×9 × 8b | ✅ Confirmed |
| `$301C` | Table | Warmup Enrichment MAP | 9×9 × 8b | ✅ Confirmed |

### Power Enrichment  (1 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$2DF0` | Table | Battery Voltage Correction | 8×2 × 8b | ✅ Confirmed |

### Spark - Timing  (3 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$2EED` | Table | PE MAP Threshold | 7×2 × 8b | ✅ Confirmed |
| `$2F00` | Table | PE Vacuum Threshold | 9×2 × 8b | ✅ Confirmed |
| `$2FB3` | Table | Enrichment Decay Timer | 8×2 × 8b | 🔶 Code-linked, name unverified |

### Spark - Modifiers  (3 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$2861` | Table | Main Spark EGR Off | 17×9 × 8b | ✅ Confirmed |
| `$28FD` | Table | Main Spark EGR On | 17×9 × 8b | ✅ Confirmed |
| `$2999` | Table | Warm Spark | 17×9 × 8b | ✅ Confirmed |

### Accel Enrichment  (10 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$277B` | Table | Idle Spark Drive | 9pt × 8b | ✅ Confirmed |
| `$278E` | Table | Idle Spark PN | 6pt × 8b | ✅ Confirmed |
| `$2A35` | Table | WOT Spark Modifier | 16×9 × 8b | ✅ Confirmed |
| `$2AD1` | Table | ECT Critical Spark | 9×9 × 8b | ✅ Confirmed |
| `$2B25` | Table | IAT Critical Spark | 9×9 × 8b | ✅ Confirmed |
| `$38FD` | Table | Idle Timing Corr | 3×2 × 8b | ✅ Confirmed |
| `$39E0` | Table | Idle Speed Adj Forward Correction (Drive) | 5×2 × 8b | ✅ Confirmed |
| `$39F3` | Table | Idle Speed Adj Reverse Correction (Drive) | 5×2 × 8b | ✅ Confirmed |
| `$405D` | Table | Spark Retard Factor Fuel On | 4×2 × 8b | ✅ Confirmed |
| `$4070` | Table | Spark Retard Factor Fuel Off | 4×2 × 8b | ✅ Confirmed |

### Cranking / Startup  (10 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$3212` | Table | MAP Accel Enrich Mult | 9×9 × 8b | ✅ Confirmed |
| `$3266` | Table | Throttle Based Enrichment Mult | 9×9 × 8b | ✅ Confirmed |
| `$32B8` | Table | AE Decay Time ECT | 9×2 × 8b | ✅ Confirmed |
| `$32CB` | Table | AE Threshold ECT | 7×2 × 8b | ✅ Confirmed |
| `$3306` | Table | AE Duration ECT | 7×2 × 8b | ✅ Confirmed |
| `$33DF` | Table | AE Warmup Factor ECT | 9×2 × 8b | 🔶 Code-linked, name unverified |
| `$3D85` | Table | AE ECT Correction | 5×2 × 8b | 🔶 Code-linked, name unverified |
| `$4083` | Table | Accel Enrich MAP | 5×2 × 8b | ✅ Confirmed |
| `$4096` | Table | Accel Enrich RPM Mod | 8×2 × 8b | ✅ Confirmed |
| `$40A9` | Table | AE Threshold Scalar | 2pt × 8b | ✅ Confirmed |

### Idle / AIS  (10 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$2683` | Table | Cranking Enrichment ECT | 9×2 × 8b | ✅ Confirmed |
| `$2696` | Table | Cranking PW Mult ECT | 8×2 × 8b | ✅ Confirmed |
| `$26BC` | Table | Cranking Duration ECT | 7×2 × 8b | ✅ Confirmed |
| `$26CF` | Table | Cranking Threshold ECT | 4×2 × 8b | ✅ Confirmed |
| `$26E2` | Table | Cranking Correction ECT | 7×2 × 8b | ✅ Confirmed |
| `$2F38` | Table | Prime Shot Pulsewidth | 9×2 × 8b | ✅ Confirmed |
| `$2F4B` | Table | Crank Injection PW | 9×2 × 8b | ✅ Confirmed |
| `$3405` | Table | Startup Fuel Corr ECT | 9×2 × 8b | 🔶 Code-linked, name unverified |
| `$3CA8` | Table | MAP Normalizer $3CA8 (9pt, idle 9x9) [READ-ONLY] | 9×2 × 8b | 📎 Axis ref (read-only) |
| `$3CBB` | Table | RPM Normalizer $3CBB (9pt, idle 9x9) [READ-ONLY] | 9×2 × 8b | 📎 Axis ref (read-only) |

### MAP / BARO  (22 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$26F5` | Table | Idle Speed Adj Delay (Not Moving) | 2×2 × 8b | ✅ Confirmed |
| `$31BE` | Table | Medium-MAP Normalizer $31BE (9pt) [READ-ONLY] | 9×2 × 8b | 📎 Axis ref (read-only) |
| `$3805` | Table | Fan AC Idle Adder | 6×2 × 8b | ✅ Confirmed |
| `$38AC` | Table | Idle Speed Limit RPM | 9×2 × 8b | ✅ Confirmed |
| `$39A8` | Table | Target Idle Drive | 8×2 × 8b | ✅ Confirmed |
| `$39BB` | Table | Target Idle P/N | 8×2 × 8b | ✅ Confirmed |
| `$39CE` | Table | Idle Speed Runtime Adder | 5×2 × 8b | ✅ Confirmed |
| `$3A19` | Table | AIS Warmup Steps ECT | 9×2 × 8b | 🔶 Code-linked, name unverified |
| `$3A2C` | Table | AIS Fine Adjust ECT | 9×2 × 8b | 🔶 Code-linked, name unverified |
| `$3A40` | Table | AIS Startup Position | 9×2 × 8b | ✅ Confirmed |
| `$3A66` | Table | AIS Cold Position | 6×2 × 8b | ✅ Confirmed |
| `$3A8C` | Table | Idle Speed Adj Cold Pos Comp | 3×2 × 8b | ✅ Confirmed |
| `$3A9F` | Table | Throttle Follower Decay vs RPM | 3×2 × 8b | ✅ Confirmed |
| `$3AB2` | Table | Throttle Follower Decay vs Delta TPS | 7×2 × 8b | ✅ Confirmed |
| `$3AC5` | Table | AIS RPM Corr | 5×2 × 8b | 🔶 Code-linked, name unverified |
| `$3B01` | Table | AIS Fine Trim | 5×2 × 8b | 🔶 Code-linked, name unverified |
| `$3B14` | Table | AIS Scalar 1 | 2pt × 8b | 🔶 Code-linked, name unverified |
| `$3B27` | Table | AIS Scalar 2 | 2pt × 8b | 🔶 Code-linked, name unverified |
| `$3B60` | Table | AIS Scalar 3 | 2pt × 8b | 🔶 Code-linked, name unverified |
| `$3B73` | Table | AIS Scalar 4 | 2pt × 8b | 🔶 Code-linked, name unverified |
| `$3C02` | Table | Idle MAP Modifier | 9×9 × 8b | ✅ Confirmed |
| `$A28B` | Table | Idle Spark Proportional Gain vs RPM | 6×2 × 8b | ✅ Confirmed |

### Cat10  (7 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$261F` | Table | Min Throttle Update MAP | 3pt × 16b | ✅ Confirmed |
| `$2637` | Table | Intake Depression WOT | 5×2 × 8b | ✅ Confirmed |
| `$2755` | Table | Altitude Fuel Comp 17pt | 17pt × 8b | ❌ No code link |
| `$2E16` | Table | Altitude Fuel Comp 6pt | 6×2 × 8b | ✅ Confirmed |
| `$373F` | Table | Altitude Load Corr | 9×2 × 8b | ✅ Confirmed |
| `$37F2` | Table | Load Mult ECT | 9×2 × 8b | 🔶 Code-linked, name unverified |
| `$3D72` | Table | A/C Load MAP Adder | 9×2 × 8b | ✅ Confirmed |

### Cat11  (2 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$342B` | Table | Knock Threshold ECT | 9×2 × 8b | 🔶 Code-linked, name unverified |
| `$34DC` | Table | Knock Retard Apply Rate | 9×9 × 8b | 🔶 Code-linked, name unverified |

### Cat12  (3 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$378B` | Table | Speed Corr 2 | 7×2 × 8b | 🔶 Code-linked, name unverified |
| `$3C56` | Table | DUPLICATE Cold Engine MAP Adder OR After-Start Decay | 9×9 × 8b | ✅ Confirmed |
| `$3C56` | Table | DUPLICATE Cold Engine MAP Adder OR After-Start Decay | 9×9 × 8b | ✅ Confirmed |

### Cat13  (3 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$3CE1` | Table | DFSO MAP Threshold | 5×2 × 8b | ✅ Confirmed |
| `$3CF4` | Table | DFSO Re-Entry Corr | 4×2 × 8b | ✅ Confirmed |
| `$3D09` | Table | DFSO Fuel Multiplier | 9×9 × 8b | ✅ Confirmed |

### Cat14  (3 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$3706` | Table | Fan On Timer | 8×2 × 8b | ✅ Confirmed |
| `$3719` | Table | Fan Off Timer | 8×2 × 8b | ✅ Confirmed |
| `$372C` | Table | Fan Hysteresis | 2×2 × 8b | ✅ Confirmed |

### Cat15  (1 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$3E34` | Table | Diag Thresh 2 | 4×2 × 8b | 🔶 Code-linked, name unverified |

### CatNone  (12 tables)

| Address | Type | Possible Name | Dimensions | Status |
|:---|:---:|:---|:---|:---|
| `$2816` | Table | RPM Normalizer $2816 (17pt) [READ-ONLY] | 17×2 × 8b | 📎 Axis ref (read-only) |
| `$284C` | Table | MAP Normalizer $284C (9pt) [READ-ONLY] | 9×2 × 8b | 📎 Axis ref (read-only) |
| `$30B8` | Table | ECT × Load Corr 9×9 | 9×9 × 8b | 🔶 Code-linked, name unverified |
| `$3184` | Table | MAP-indexed Scalar 2pt | 2×2 × 8b | 🔶 Code-linked, name unverified |
| `$31D1` | Table | Identity Normalizer $31D1 (9pt) [READ-ONLY] | 9×2 × 8b | 📎 Axis ref (read-only) |
| `$31FD` | Table | Low-RPM Normalizer $31FD (9pt) [READ-ONLY] | 9×2 × 8b | 📎 Axis ref (read-only) |
| `$3393` | Table | RPM Curve 3pt | 3×2 × 8b | 🔶 Code-linked, name unverified |
| `$33A6` | Table | IAT Curve 5pt | 5×2 × 8b | 🔶 Code-linked, name unverified |
| `$3440` | Table | RPM Limit | 13×9 × 8b | 🔶 Code-linked, name unverified |
| `$3910` | Table | PE Enable RPM vs ECT | 3×3 × 8b | 🔶 Code-linked, name unverified |
| `$3BAE` | Table | Warmup Fuel Multiplier [READ-ONLY] | 9×9 × 8b | 🔶 Code-linked, name unverified |
| `$40BE` | Table | ECT Diag Model &#151; BARO × Load Correction [READ-ONLY] | 9×9 × 8b | ✅ Confirmed |

---


## Part 2 — Scalars

| Address | Type | Possible Name | Size | Status |
|:---|:---:|:---|:---|:---|
| `$266B` | Scalar | MAP Offset | 2B | ✅ Confirmed |
| `$266D` | Scalar | MAP Scaling | 2B | ✅ Confirmed |
| `$2718` | Scalar | Fan 1 Lo Speed Off | 1B | ✅ Confirmed |
| `$271C` | Scalar | Fan 2 Lo Speed Off | 1B | ✅ Confirmed |
| `$271D` | Scalar | Fan 2 Lo Speed On | 1B | ✅ Confirmed |
| `$271E` | Scalar | Fan 2 Hi Speed Off | 1B | ✅ Confirmed |
| `$271F` | Scalar | Fan 2 Hi Speed On | 1B | ✅ Confirmed |
| `$2720` | Scalar | Overheat Threshold 1 | 1B | ✅ Confirmed |
| `$2721` | Scalar | Overheat Threshold 2 | 1B | ✅ Confirmed |
| `$2B78` | Scalar | Min Pulsewidth | 2B | ✅ Confirmed |
| `$2B7A` | Scalar | Min Pulse CL | 2B | ✅ Confirmed |
| `$3355` | Scalar | CL High RPM Hi | 1B | ✅ Confirmed |
| `$3356` | Scalar | CL High RPM Lo | 1B | ✅ Confirmed |
| `$344A` | Scalar | RPM Limit | 2B | ✅ Confirmed |
| `$3947` | Scalar | PE Min TPS | 1B | ✅ Confirmed |
| `$3948` | Scalar | CL Enable ECT | 1B | ✅ Confirmed |
| `$3949` | Scalar | PE Min MAP | 1B | ✅ Confirmed |
| `$394A` | Scalar | PE Min ECT | 1B | ✅ Confirmed |
| `$394B` | Scalar | PE Min BARO | 1B | ✅ Confirmed |

---


## Part 3 — Scaling Factors & Encoding Reference

_This reference applies **by table purpose**, not per-address. Cross-reference against category + known formula patterns. Do not duplicate this information into individual table rows._

### Axis (Input / Breakpoint) Encodings

| Quantity | Raw-to-Real Formula | Notes |
|:---|:---|:---|
| **RPM** (normalized axis, byte × 32) | `X × 32` | Used by 9-pt and 17-pt RPM axes in most 2D lookups |
| **RPM** (period-high-byte, for thresholds) | `20971520 / (X × 256)` | Compared in DFSO/rev-limit gates where raw period byte is the comparand |
| **RPM Limit** (full 16-bit period, `$344A`) | `20971520 / X` | Direct period-to-RPM for the word stored there |
| **MAP** (raw ADC → kPa, 2-bar sensor) | `X × 0.4134` | v130 tune uses a 2-bar MAP sensor |
| **BARO** | `X / 128` | Used in altitude compensation |
| **ECT / IAT** (raw byte → °C) | `X − 64` | Byte offset by 64; covers −64 °C to +191 °C |
| **TPS** (raw → %) | context-dependent | See individual axis labels |

### Z-Axis (Table Value / Output) Formulas

| Table Purpose | Formula | Units |
|:---|:---|:---|
| **Injector Pulse Width** (Base PW, cranking PW, min PW, min PW CL) | `X × 4` | microseconds (μs) |
| **Spark Timing** (Main Spark, WOT Spark, Warm Spark, Idle Spark, ECT/IAT Critical Spark) | `X × 0.5` | degrees BTDC |
| **Dwell** (`$40BE`) | `X × 0.1` | milliseconds (ms) |
| **Battery Voltage Deadtime** (`$2DF1`) | `X × 16` | μs |
| **Fuel Multipliers** (DFSO Fuel Mult `$3D09`, Warmup Fuel Mult `$3BB7`, AE Mult, Throttle-Based Enrich `$3266`) | `X / 64` | dimensionless (1.00 = nominal) |
| **Warmup MAP Adder** | `X × (100 / 256)` | kPa-equivalent offset |
| **Warmup Time Factor** | `X × (100 / 128)` | normalized ratio |
| **Altitude Fuel Comp 17-pt** (`$2755`) | `X / 128` | dimensionless multiplier |
| **Air Enrichment Factor** (`$2E03`) | `1 + X/256` | multiplier (1.0 = no adjust) |
| **Altitude Fuel Comp 6-pt** (`$2E16`) | `1 + X/256` | multiplier |
| **Part Throttle Enrichment** (`$2E53`) | `1 + X/256` | multiplier |
| **PE Vacuum Threshold** (`$2F00`) | `1 + X/256` | multiplier |
| **CL High RPM scalars** (`$3355`, `$3356`) | `X × 32` | RPM |
| **ECT Gate scalars** (CL Enable `$3948`, PE Min ECT `$394A`, etc.) | `X − 64` | °C |
| **All other** (AIS step counts, timer values, flag bytes, counters, correction bytes) | raw | per-context units |

### Storage Header Formats (binary layout conventions)

Every code-accessed table in this ECU uses one of the following five header formats, set up before a JSR to the corresponding interp routine:

| Interp Routine | Header Size | Layout | Identifier |
|:---|:---:|:---|:---|
| `$10030` (1D byte→byte) | 1 byte | `[count]` then `count × (BP_byte, VAL_byte)` | `1Dbb` |
| `$10034` (1D byte→word) | 1 byte | `[count]` then `count × (BP_byte, VAL_hi, VAL_lo)` | `1Dbw` |
| `$10038` (2D byte bilinear) | 3 bytes | `[rows, cols, pad]` then `rows × cols` bytes | `2Db` |
| `$1003C` (2D word bilinear) | 4 bytes | `[rows, cols, pad, pad]` then `rows × cols × 2` bytes | `2Dw` |
| `$10050` (1D word→byte) | 1 byte | `[count]` then `count × (BP_hi, BP_lo, VAL_byte)` | `1Dwb` |

**Important:** TunerPro `Address (Hex)` points to the **data start**, not the header. For 1D count-pair tables the header byte sits at `Address − 1`; for 2D byte tables it's `Address − 3`; for 2D word tables it's `Address − 4`.

### Axis Normalizer Tables (read-only — do not edit)

These translate raw sensor bytes into the normalized 0–255 range that indexes into 2D tables. **Editing these misaligns every lookup that depends on them.**

| Normalizer | Feeds | Axis Decoded |
|:---|:---|:---|
| `$2816` (17-pt) | `$2B87` / `$2CBD` Base Fuel PW 17×9 | RPM (raw × 32): 512 … 4992 |
| `$284C` (9-pt) | `$2B87` / `$2CBD` Base Fuel PW 17×9 | MAP kPa (raw × 0.4134): 14.9 … 105.4 |
| `$3CBB` (9-pt) | 9×9 idle-region tables | RPM: 704 … 4000 |
| `$3CA8` (9-pt) | 9×9 idle-region tables | MAP kPa: 62 … 105 |
| `$3CCE` (9-pt) | 9×9 ECT-indexed tables | ECT °C: −20 … +115 |
| `$31FD` (9-pt) | low-range fuel sub-paths | Low RPM: 512 … 3584 |
| `$2724` / `$33F3` (9-pt) | ECT normalizers (duplicated contexts) | ECT: −40 … +112 °C |
| `$31BE` (9-pt) | medium-MAP range | 12 … 81 kPa |
| `$31D1` (9-pt) | identity pass-through | 0 … 255 linear |
| `$283A` (9-pt) | low-range (purpose TBD) | — |
