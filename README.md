Wireless channel measurements
=============================

This repository contains [VNA](https://en.wikipedia.org/wiki/Network_analyzer_(electrical)) measurements of a wireless channel around the 5.8 GHz band in an indoor environment. These measurements can be used for simulation purposes, e.g. to determine the performance of various modulation schemes in this type of environment.

Measurements were done with a Rohde & Schwarz ZVA40 VNA. In order to improve the sensitivity, the signal from the receiving antenna was first amplified with a wideband amplifier before being sent to the VNA. We tried to calibrate out the response of the cables, however we had to move the cables around a lot so there may be some artifacts in the data as a result of this.

All measurements used [Pagoda antennas](https://www.maartenbaert.be/quadcopters/antennas/pagoda-antenna/) for both the transmitting and receiving side, with the exception of the last data set, which used [Triple Feed Patch antennas](https://www.maartenbaert.be/quadcopters/antennas/triple-feed-patch-antenna/) instead.

The transmitting antenna was placed in a fixed location while the receiving antenna was moved around in the lab. Since part of the goal of these measurements was to determine how the channel characteristics would change when the antenna is moved around, the receiving antenna was placed on a linear rail with a 20cm range of movement, which could be moved in 1mm increments. The measurements were fully automated and no one was present in the lab during these measurements, to avoid interference.

We measured the channel response with the receiving antenna placed at multiple positions along the linear rail, without changing anything in the lab. All changes to the channel are purely the result of the movement of the receiving antenna, nothing else was moved. These measurements may be useful to simulate wireless communication with a moving device.

Measurement details
-------------------

The first set of measurements used a wide frequency range of 4 .. 8 GHz. Measurements were supposed to be done in 0.1 MHz increments, but I accidentally set the number of frequency points to 40000 instead of 40001, so the frequency steps are slightly off. This shouldn't affect the measurement accuracy though. All measurements used Pagoda antennas.

| Dataset | Description                   |
| ------- | ----------------------------- |
| data01  | Direct path, ~9m, 10cm steps  |
| data02  | Direct path, ~8m, 10cm steps  |
| data03  | Direct path, ~7m, 10cm steps  |
| data04  | Blocked path, ~6m, 10cm steps |
| data05  | Blocked path, ~6m, 10cm steps |
| data06  | Direct path, ~7m, 10cm steps  |
| data07  | Direct path, ~7m, 1cm steps   |

The second set of measurements used a narrower frequency range of 5.3 .. 6.3 GHz, but uses much finer increments for the position along the linear rail. For these measurements we used 2 transmitting antennas and 2 receiving antennas, and measured the channel response for each antenna pairing, to simulate a MIMO channel. All measurements used Pagoda antennas.

| Dataset | Description                             |
| ------- | --------------------------------------- |
| data08  | Direct path, ~7m, 1mm steps, TX1 -> RX1 |
| data09  | Direct path, ~7m, 1mm steps, TX1 -> RX2 |
| data10  | Direct path, ~7m, 1mm steps, TX2 -> RX2 |
| data11  | Direct path, ~7m, 1mm steps, TX2 -> RX1 |

The third set of measurements used Triple Feed Patch antennas instead.

| Dataset | Description                 |
| ------- | --------------------------- |
| data12  | Direct path, ~7m, 1mm steps |
