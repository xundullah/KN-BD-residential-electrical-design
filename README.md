# Electrical Circuit Diagram — Bangladesh Standard Residential Building

> A complete single-line diagram (SLD), consumer-unit (CU) circuit schedules, and floor-plan wiring schematic for a 3018 sq.ft residential floor with **3 apartments + common services**, designed to **Bangladesh standards** (BNBC 2020, BSTI, DPDC/DESCO service rules).

![Standard](https://img.shields.io/badge/Standard-BNBC%202020-blue)
![Supply](https://img.shields.io/badge/Supply-1--Phase%20230V-yellow)
![Meters](https://img.shields.io/badge/Meters-4%20(3%20Apt%20%2B%20Common)-green)
![Total Load](https://img.shields.io/badge/Sanctioned%20Load-21%20kVA-orange)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📐 Overview

This repository contains a print-ready, A3-landscape electrical design document for a typical multi-unit residential floor in Bangladesh. The design follows the standard practice of **separate single-phase meters per apartment** with an additional common meter for shared services (staircase lighting and water pump).

The deliverable is a single self-contained HTML file with **4 sheets**:

| Sheet | Content |
|-------|---------|
| **1** | Single Line Diagram (SLD) — 4 independent single-phase services, meters, main breakers, earthing |
| **2** | Consumer Unit (CU) circuit schedules — every MCB, cable size, load, and outlet list per apartment |
| **3** | Floor plan wiring schematic — feeder routing + point layout per room |
| **4** | Standards, metering application, voltage-drop check, safety mandates, designer credit |

---

## 🏠 Building Layout

| Unit | Position | Rooms | Connected Load | Main Breaker | Sanctioned |
|------|----------|-------|----------------|--------------|------------|
| **Unit 1** | Top-Left | M.Bed + Bed-2 + Drawing/Dining + Kitchen + 2 Toilets + Verandah | 5.5 kW | 32 A 2P RCCB | 5 kVA |
| **Unit 2** | Bottom-Left | M.Bed + Bed-2 (with AC) + Drawing/Dining + Kitchen + 2 Toilets + 2 Verandahs | 6.5 kW | 32 A 2P RCCB | 6 kVA |
| **Unit 3** | L-shape (Top-Right + Bottom-Right) | 2 × M.Bed + Small Room + Drawing/Dining + Kitchen + 2 Toilets + Verandah + Open Terrace | 7.2 kW | 40 A 2P RCCB | 7 kVA |
| **Common** | Central staircase | Stair + Lobby + 1 HP Pump + Roof lights | 2.5 kW | 20 A 2P RCCB | 3 kVA |
| | | | | **Total** | **21 kVA** |

> **Note:** Unit 3 is an L-shaped duplex spanning both the Top-Right and Bottom-Right zones, served by a single meter and sharing one kitchen between zones.

---

## ⚡ Per-Room Point Counts

### Master Bedroom
- 3 lights (2 ceiling + 1 bedside reading)
- 3 × 13 A sockets (bedside high / floor low / TV-height)
- 1 × Split AC point (1.5 Ton, 20 A industrial socket)
- 1 × Ceiling fan

### Bed-2 / Small Room
- 2 lights
- 2 × 13 A sockets (1 high 1100 mm + 1 low 300 mm)
- 1 × Ceiling fan
- *(Unit 2 Bed-2: additional 1 Ton AC)*

### Drawing / Dining
- 4 lights
- 4 × 13 A sockets (Fridge dedicated + TV low + 2 others)
- 2 × Ceiling fans
- 1 × Split AC point (1.5 Ton)
- 1 × Fridge dedicated feed (always-on)

### Kitchen
- 1 ceiling light + 1 counter light
- **4 × 13 A counter sockets** (exhaust fan / microwave / rice cooker or air fryer / electric oven)
- 1 × Kitchen fan point

### Toilets
- **No geysers** (by design — owner's preference)
- M.Toilet: 1 light + 1 × 13 A IP44 socket (for trimmer/hairdryer)
- 2nd Toilet: 1 light only

### Verandah / Balcony
- 1 light per verandah (weatherproof)

### Open Terrace (Unit 3 only)
- 4 weatherproof lights
- 4 × 13 A IP54 sockets

---

## 🛡️ Protection Strategy

| Level | Device | Purpose |
|-------|--------|---------|
| Meter | DPDC service fuse | Utility protection |
| Apartment incomer | **30 mA RCCB** (25/32/40 A 2P) | Life-safety (shock protection) — *mandatory per BNBC* |
| Lighting circuits | 6 A SP MCB | Overcurrent on 1.5 mm² cable |
| Socket circuits | 16 A SP MCB | Overcurrent on 2.5 mm² cable |
| Kitchen / Drawing | 20 A SP MCB | Overcurrent on 4 mm² cable |
| AC / large loads | 20 A DP MCB | Double-pole isolation |
| Pump motor | 16 A DP MCB + DOL Starter | Inrush current management |

**Earthing:** TT system with **4 separate earth pits** (one per meter), 25×3 mm GI strip 2.5 m deep with charcoal + salt layer, target resistance < 1 Ω.

---

## 🔌 Cable Schedule

| Application | Cable (PVC Cu) | Rated Current |
|-------------|----------------|---------------|
| Service drop (per meter) | 2C × 10 mm² | 50 A |
| Meter → CU (apartment incomer) | 3C × 6 mm² to 10 mm² | 36–50 A |
| Lighting + fans | 2 × 1.5 mm² + 1.5 mm² Earth | 14 A |
| General sockets | 2 × 2.5 mm² + 2.5 mm² Earth | 21 A |
| AC / Kitchen / Drawing | 2 × 4 mm² + 2.5 mm² Earth | 28 A |

All conduits: **20 mm rigid PVC, concealed**, per IEE wiring practice adopted in Bangladesh.

---

## 📏 Standard Socket Heights (AFFL)

| Type | Height |
|------|--------|
| Low socket (L) — floor appliances, TV, fridge | 300 mm |
| High socket (H) — wall items, chargers | 1100 mm |
| Kitchen counter sockets | 1100 mm |
| Toilet socket (IP44) | 1200 mm |
| Light switch | 1200 mm |
| AC socket (20 A) | 1800 mm |

---

## 📜 Standards Applied

- **BNBC 2020, Part 8** — Bangladesh National Building Code, Building Services / Electrical
- **DPDC / DESCO / REB Service Rules** — Metering, service cable, sanctioned load application
- **BSTI / BDS IEC 60898** — MCB certification in Bangladesh
- **BDS IEC 61008** — RCCB / RCBO certification
- **IEE Wiring Regulations** (adopted) — Installation method, derating, voltage drop ≤ 4%
- **IEC 60364** — Low-voltage electrical installations

---

## 🚀 How to Use

### View the design
1. Clone or download this repository
2. Open `electrical_circuit_diagram_BD_FINAL.html` in any modern browser (Chrome, Firefox, Edge)
3. Use browser **Print → Save as PDF** with A3-landscape paper size for a hard copy

### For contractors
- Sheet 2 has the full MCB schedule — every circuit is numbered (1.1, 1.2 … 3.13) and includes breaker rating, cable size, and exact outlet description
- Sheet 3 shows where each device sits in each room
- Sheet 4 has the voltage-drop check and the safety mandates that must be followed before energisation

### For DPDC / DESCO meter application
- Sheet 4 lists the sanctioned load per meter (5 kVA + 6 kVA + 7 kVA + 3 kVA = 21 kVA)
- Apply for **4 separate single-phase connections** (3 apartment + 1 common)
- Maximum per single-phase meter is ~7.5 kVA — all 4 meters are within limits

---

## ⚠️ Important Notes

> **This design is schematic.** Final routing, exact point counts, and load list must be verified by a **licensed electrical engineer** (Government Electrical Inspectorate — CEI, GoB) before execution. All installation work must be carried out by a CEI-licensed electrician.

### Pre-energisation tests (mandatory)
- Insulation resistance > 1 MΩ
- Earth continuity < 0.5 Ω
- RCCB trip-time test (must trip within 40 ms at I∆n)

### Specific advisories
- **Unit 3 (L-shape duplex):** 3 ACs + electric oven running simultaneously can briefly exceed 7 kVA — post advisory inside CU-3 door
- **Voltage drop check:** For meter-to-CU runs over 25 m, upgrade Unit 3's feeder from 10 mm² to 16 mm² Cu
- **Lightning arrester** recommended if total building height > 15 m

---

## 📁 Repository Contents

```
.
├── electrical_circuit_diagram_BD_FINAL.html   # Main 4-sheet design (open in browser)
├── README.md                                   # This file
└── floor_plan.jpeg                             # Original architectural floor plan (reference)
```

---

## 👤 Designed by

**Raihan Bin Mofidul**
PhD Student & Teaching Assistant | Electrical and Data Engineering, FEIT
Research Assistant | Connectivity Innovation Network (CIN), NSW, Australia
University of Technology Sydney (UTS), Sydney, Australia

---

## 📄 License

This design is shared under the **MIT License** — free to use, modify, and distribute with attribution. See `LICENSE` for details.

---

## 🤝 Contributing

This is a reference design for educational and contractor-handover purposes. If you adapt it for your own project:

1. **Verify cable lengths on site** — voltage drop is the main variable
2. **Confirm sanctioned load** with DPDC/DESCO before final breaker selection
3. **Use only BSTI-certified** MCBs, RCCBs, and cables (BRB, BBS, Paradise, or equivalent)
4. **Earth resistance must be tested** with a megger before energisation — < 1 Ω is non-negotiable

Pull requests for improvements, additional load scenarios (with geysers, with 3-phase upgrade, with solar PV integration, etc.) are welcome.

---

## 🔖 Citation

If you use this design as a reference in a publication or report, please cite:

```
Mofidul, R. B. (2026). Electrical Circuit Diagram for a Bangladesh-Standard
Residential Building (3 Apartments + Common, Single-Phase Service).
University of Technology Sydney. [GitHub Repository]
```

---

*Drawing No. EL-04 | Final Revision | Bangladesh Standard (BNBC 2020 / BSTI / DPDC)*
