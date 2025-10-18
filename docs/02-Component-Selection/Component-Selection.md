---
title: Component Selection
---

*Table 1: Potentiometer*

**External Clock Module**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](<img width="240" height="215" alt="PTV09A-4020F-B103" src="https://github.com/user-attachments/assets/9f41d368-792b-4897-8668-1025522d5386" />
)<br>Option 1.<br> Bourns PTV09A-4020F-B103<br>$0.89/each<br>[link to product](https://www.digikey.com/en/products/detail/bourns-inc/PTV09A-4020F-B103/3534181)                 | \* Inexpensive<br>\* Compact, PCB-friendly<br>\* Widely stocked                                               | \* Needs panel hole clearance<br>\* not sealed. |
| ![](image3.png)<br>\* Option 2. <br>\* Alpha RV16AF-10-15R1-B10K <br>\* $1.61/each <br>\* [Link to product](https://www.mouser.com/ProductDetail/Alpha-Taiwan/RV16AF-10-15R1-B10K-3LA?qs=MLItCLRbWsxJ6oCJ2%252BBnKw%3D%3D&srsltid=AfmBOoozW9MBl4MJSFmP1FooUcpK-M39N7zomQ4_D5To7BlC04olpZne) | \* Robust shaft <br>\* Easy user control with knob <br> \* Smooth rotation | * Larger <br>\* needs nut/washer hardware <br>\* Off-board wiring if not panel-mounted                          ![Uploading PTV09A-4020F-B103.png…]()
                            |
| ![](image3.png)<br>\* Option 3. <br>\* Bourns 3386P-1-103 <br>\* $2.18/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/bourns-inc/3386P-1-103/86787) | \* Precise adjustment <br>\* tiny footprint <br> \* Smooth rotation | * Not user-friendly <br>\* screwdriver adjust only <br>\* Most expensive out of three   |

**Choice:** Option 1: Bourns PTV09A-4020F-B103 (10 kΩ, linear)

**Rationale:** Small, PCB-mountable, and reliable for clean 0–3.3 V ADC readings without panel hardware overhead. It hits the “simple, inexpensive, available” trifecta while fitting the 3.3 V analog input plan. Trimmers are a pain for user interaction; the big Alpha is overkill for this board.

