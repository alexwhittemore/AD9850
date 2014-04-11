# AD9850 Demo Program

The AD9850 is a DDS frequency synthesizer chip capable of up to 40MHz output. It's available on ebay integrated into modules requiring only an external microcontroller for use. There are at least two major versions of this module, both available for substantially lower cost than single quantities of the chip itself in the US.

This arduino sketch allows one to get up and running with one of these boards quickly. Connections are included in the sketch itself, but they are as follows:

Arduino: | Module:
---------|--------
8        | W_CLK
9        | FQ_UD
10       | DATA (or D7)
11       | RST

Additionally:

Arduino: | Potentiometer:
---------|---------------
GND      | Low
2        | High (for lack of an extra 5V pin is all)
5        | Center (analog in pin)

The map_double function will map the potentiometer input to a frequency, currently configured between 100kHz on the low end and 40MHz at the top. This frequency is continuously printed to the serial terminal and updated to the DDS. Changing these parameters should be straightforward in the sketch.


## Credits:

* Original sketch: http://nr8o.dhlpilotcentral.com/?p=83
* map_double function: http://www.dustynrobots.com/news/high-resolution-arduino-map-function/
* Additional info: http://www.ad7c.com/projects/ad9850-dds-vfo/
