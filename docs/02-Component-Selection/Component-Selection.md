---
title: Component Selection
---

*Table 1: Potentiometer*

**External Clock Module**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](image1.png)<br>Option 1.<br> Bourns PTV09A-4020F-B103<br>$0.89/each<br>[link to product](https://www.digikey.com/en/products/detail/bourns-inc/PTV09A-4020F-B103/3534181)                 | \* Inexpensive<br>\* Compact, PCB-friendly<br>\* Widely stocked                                               | \* Needs panel hole clearance<br>\* not sealed. |
| ![](image3.png)<br>\* Option 2. <br>\* Alpha RV16AF-10-15R1-B10K <br>\* $1.61/each <br>\* [Link to product](https://www.mouser.com/ProductDetail/Alpha-Taiwan/RV16AF-10-15R1-B10K-3LA?qs=MLItCLRbWsxJ6oCJ2%252BBnKw%3D%3D&srsltid=AfmBOoozW9MBl4MJSFmP1FooUcpK-M39N7zomQ4_D5To7BlC04olpZne) | \* Robust shaft <br>\* Easy user control with knob <br> \* Smooth rotation | * Larger <br>\* needs nut/washer hardware <br>\* Off-board wiring if not panel-mounted                                                      |
| ![](image3.png)<br>\* Option 3. <br>\* Bourns 3386P-1-103 <br>\* $2.18/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/bourns-inc/3386P-1-103/86787) | \* Precise adjustment <br>\* tiny footprint <br> \* Smooth rotation | * Not user-friendly <br>\* screwdriver adjust only   |

**Choice:** Option 2: CTX936TR-ND surface mount oscillator

**Rationale:** A clock oscillator is easier to work with because it requires no external circuitry in order to interface with the PSoC. This is particularly important because we are not sure of the electrical characteristics of the PCB, which could affect the oscillation of a crystal. While the shipping speed is slow, according to the website if we order this week it will arrive within 3 weeks.

### Style 2

> Also acceptable, more markdown friendly

**External Clock Module**

1. XC1259TR-ND surface mount crystal

    ![](image1.png)

    * $1/each
    * [link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Inexpensive                               | Requires external components and support circuitry for interface |
    | Compatible with PSoC                      | Needs special PCB layout.                                        |
    | Meets surface mount constraint of project |

1. CTX936TR-ND surface mount oscillator

    ![](image3.png)

    * $1/each
    * [Link to product](http://www.digikey.com/product-detail/en/636L3I001M84320/CTX936TR-ND/2292940)

    | Pros                                                              | Cons                |
    | ----------------------------------------------------------------- | ------------------- |
    | Outputs a square wave                                             | More expensive      |
    | Stable over operating temperature                                 | Slow shipping speed |
    | Direct interface with PSoC (no external circuitry required) range |

**Choice:** Option 2: CTX936TR-ND surface mount oscillator

**Rationale:** A clock oscillator is easier to work with because it requires no external circuitry in order to interface with the PSoC. This is particularly important because we are not sure of the electrical characteristics of the PCB, which could affect the oscillation of a crystal. While the shipping speed is slow, according to the website if we order this week it will arrive within 3 weeks.
