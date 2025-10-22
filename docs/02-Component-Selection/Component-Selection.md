---
title: Component Selection
---


**Op-amp**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](MCP6004_IP.png)<br>Option 1.<br> MCP6004-I/P<br>$0.59/each<br>[link to product](https://www.digikey.com/en/products/detail/microchip-technology/MCP6004-I-P/523060)                                                                                                                                                                   | \* Rail-to-rail I/O<br>\* 1.8–5.5 V supply<br>\* Low quiescent current<br>\* Good for sensors, buffers, or filters                                                                                                                                                                                                         | * 1 MHz GBW (not for high-speed) <br>\* Limited output drive 
| ![](TLV9004IDR.png)<br>\* Option 2. <br>\* TLV9004IDR <br>\* $.69/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/texas-instruments/TLV9004IDR/9674911)                                                                                                                                                         | \* Rail-to-rail <br>\* 1.8–5.5 V <br> \* Many footprints | * Often SMD only <br>\* Similar 1 MHz GBW <br>\* Availability varies                                                                                                                       |
| ![](LM324N.png)<br>\* Option 3. <br>\* LM324N <br>\* $.24/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/onsemi/LM324N/458682)                                                                                                                                                                              | \* Inexpensive <br>\* Dual In-line Package <br> \* Present everywhere | * Not rail-to-rail <br>\* Input common-mode limits can bite at 3.3 V <br>\* Vout can’t hit 3.3 V rails   |

**Choice:** Option 1: MCP6004-I/P

**Rationale:** Runs happily at 3.3 V, rail-to-rail I/O, low Iq, DIP package for quick breadboard/proto. It hits the sensor-signal conditioning needs without SMD headaches or excess cost.




**Linear Regulator**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](LM7805T.png)<br>Option 1.<br> LM7805T<br>$0.33/each<br>[link to product](https://www.digikey.com/en/products/detail/taejin/LM7805T/22237260)                                                                                                                                                                                       | \* 5 V fixed <br>\* Up to ~1 A with heatsinking<br>\* easy to design with | * Big dropout (~2 V): needs ≥7 V in <br>\* Poor efficiency vs switchers<br>\* Watch thermals
| ![](MC7805CTG.png)<br>\* Option 2. <br>\* MC7805CTG <br>\* $.52/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/onsemi/MC7805CTG/919333)                                                                                                                                                                       | \* Same behavior <br>\* Widely available <br>  | * Same dropout/thermal limits                    |
| ![](AMS1117-5.0.png)<br>\* Option 3. <br>\* AMS1117-5.0 <br>\* $.12/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/evvo/AMS1117-5-0/24370130)                                                                                                                                                                   | \* Compact <br>\* Inexpensive | * High dropout (~1.1–1.3 V <br>\* Only ~800 mA <br>\* Thermal headroom limited   |

**Choice:** Option 1: LM7805T

**Rationale:** 5 V rail for lab bricks ≥7–9 V input. The design time is near zero, and sourcing is painless. If the input headroom is tight, it can be replaced with an LM2940-5.0.





**Photoresistor**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](Adafruit.png)<br>Option 1.<br>Adafruit Photo Cell<br>$0.95/each<br>[link to product](https://www.digikey.com/en/products/detail/adafruit-industries-llc/161/7244927)                                                                                                 | \* Well-documented <br>\* Simple to integrate in a 3.3 V divider<br>\* Small and inexpensive                                                                                                                                                             | * Not super high precision<br>\*Typical resistance ranges<br>\* May need calibration
| ![](NSL-5162.png)<br>\* Option 2. <br>\*Photonix NSL‑5162 CDS Photoresistor<br>\* $1.06/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/advanced-photonix/NSL-5162/5039797)                                                                     | \*Good industrial pedigree<br>\*Known performance specs<br> \*Radial through-hole | *Slightly higher cost<br>\*More specs than needed<br>\*Adjustment to the ambient light threshold more than originally intended                    |
| ![](PDV-P5001.png)<br>\* Option 3. <br>\* Photonix PDV‑P5001 CDS Photoresistor<br>\* $1.54/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/advanced-photonix/PDV-P5001/480599)                                                                  | \* Larger sensor area (11 mm)<br>\*Could give stronger signal for low-light situations                                                                                                                                                                                                                              | * Bigger package<br>\* Might require different mounting / sensor housing    |

**Choice:** Option 2: Photonix NSL‑5162 CDS Photoresistor

**Rationale:** The NSL-5162 CdS photoresistor was chosen because it offers precise, repeatable light-to-resistance characteristics backed by a detailed datasheet and stable manufacturing. Its wide dynamic range and reliable performance at 3.3 V make it a better long-term, spec-driven choice for consistent ambient-light sensing than hobby-grade LDRs.
