---
title: Star Skirt
project: bof-star-skirt
published: true
year: 2019
---

## About
This is a skirt inspired by the milky way galaxy. I made a very large petticoat type skirt using 27 layers of different colored tulle, and added LED stars with my own custom LED driver circuit boards. 

### Honors
I used this project as a part of my application for the [Brooke Owens Fellowship](brookowensfellowship.org), and was able to advance to the semifinalist round of this highly competitive fellowship.  

### Design
I developed a custom miniature circuit board system, designed to be modular and easy to wire. I optimized for low cost-to-star ratio compared to existing methods with similar individual control over the brightness of each light.

In order to do this, I designed a tiny 0.60" x 0.40" breakout board for the WS2812 LED driver. This is the same driver used in Adafruit NeoPixels and other common addressable LED strips. These drivers are designed to be chained, and each one has 3 channels, ostensibly for the red, green, and blue channels of an RGB LED. There exist commercially available LED strips that replace the three colored LEDs with white ones, allowing for a pure white color rather than the off-white achieved by RGB color mixing, but they are restricted to the "strip" form factor, which isn't well suited for embedding into fabric. The strip form factor also means the LEDs are uniformly spaced, which inhibits my ability to create a more natural looking random distribution of stars. 

I tripled the number of stars I would get per driver by repurposing the three channels to each control an individual 3mm white LED. I made cables for sets of 3 of these LEDs using scrap Ethernet cable, with varying lengths to allow me to control the locations and distribution of the lights.

I made three chains of 15-20 drivers (45-60 lights), and secured them to ribbons. I could layer these three chains under different amounts of tulle in my skirt, which gave the star field depth - a detail that really distinguishes this skirt. Their power, ground, and data lines wired through hidden slits in the skirt to a pocket on the innermost layer, which housed an Arduino Nano and a rechargable USB power bank. 

On the Nano, I programmed an algorithm that would twinkle each star by first pseudorandomly seeding initial brightness values, and then periodically fading into new random target brightness levels. This is an algorithm I have used on several star type projects. 

The LEDs and SMD board components were soldered by hand. The 0402 resistors and capacitors went on with tweezers and a lot of patience. 

I did a photoshoot with [Fayth Krause](https://www.instagram.com/squirrelbait.photos/) and put together a webpage based multimedia essay that spoke about how this skirt was part of my journey as an aspiring engineer, astronomer, and dreamer. 

## Resources
- ["Starlight" submission]({{site.url}}/starlight/)
- [twinkle Arduino code](https://github.com/gisellegk/twinkle)
- [Eagle files](https://github.com/gisellegk/ws2811_breakout)

## Media
{% include image-gallery.html folder="/assets/img/bof-star-skirt" %}
