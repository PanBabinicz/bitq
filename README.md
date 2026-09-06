# Bitq

## SAP-1 Architecture

![SAP1-ARCH](https://github.com/PanBabinicz/bitq/blob/master/doc/screenshots/sap1-architecture.png)

### Clock

#### Functional Diagram

![ICM7555-FUNC-DIAGRAM](https://github.com/PanBabinicz/bitq/blob/master/doc/screenshots/clock_icm7555_func_diagram.png)

#### Astable

![ICM7555-ASTABLE](https://github.com/PanBabinicz/bitq/blob/master/doc/screenshots/astable.png)

*In the astable configuration, the 555 timer puts out a continuous stream of rectangular pulses
having a specific period. The astable configuration is implemented using two resistors,
R1 and R2, and one capacitor C. The threshold and trigger pins are both connected to the
capacitor; thus they have the same voltage.*

*Its repeated operating cycle (starting with the capacitor uncharged) is:*

*1. Since the capacitor's voltage will be below 1⁄3 VCC, the trigger pin causes the 555's
internal latch to change state, causing OUT to go high and the internal discharge
transistor to cut-off.*

*2. Since the discharge pin is no longer short-circuited to ground, the capacitor starts charging via current
from Vcc through the resistors R1 and R2*

*3. Once the capacitor charge reaches 2⁄3 Vcc, the threshold pin causes the 555's internal latch to change state,
causing OUT to go low and the internal discharge transistor to go into saturation (maximal-conductivity) mode.*

*4. This discharge transistor provides a discharge path, so the capacitor starts discharging through R2.*

*5. Once the capacitor's voltage drops below 1⁄3 VCC, the cycle repeats from step 1.*

#### Monotstable

>

#### Bistable

>

#### Resources

> Ben Eater
>
> https://www.youtube.com/watch?v=kRlSFm519Bo&list=PLowKtXNTBypGqImE405J2565dvjafglHU&index=2
> https://www.youtube.com/watch?v=81BgFhm2vz8&list=PLowKtXNTBypGqImE405J2565dvjafglHU&index=3
> https://www.youtube.com/watch?v=WCwJNnx36Rk&list=PLowKtXNTBypGqImE405J2565dvjafglHU&index=4
> https://www.youtube.com/watch?v=SmQ5K7UQPMM&list=PLowKtXNTBypGqImE405J2565dvjafglHU&index=5

> James Sharman
>
> https://www.youtube.com/watch?v=KEwL2P8IGaA&list=PLFhc0MFC8MiCDOh3cGFji3qQfXziB9yOw

## References

> Albert P. Malvino, Jerald A. Brown - Digital Computer Electronics
