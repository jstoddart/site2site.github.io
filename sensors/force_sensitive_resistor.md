---
layout: base
style: sensor
title: Force Sensitive Resistor
sensor: Force Sensitive Resistor
---
##	Force Sensitive Resistor

![Force Sensistive Resistor](https://dlnmh9ip6v2uc.cloudfront.net//images/products/9/3/7/6/09376-1.jpg)

A force-sensing resistor is a material whose resistance changes when a force or pressure is applied. They are also known as "force-sensitive resistor" and are sometimes referred to by the initialism "FSR".

Force-sensing resistors consist of a conductive polymer, which changes resistance in a predictable manner following application of force to its surface. They are normally supplied as a polymer sheet or ink that can be applied by screen printing. The sensing film consists of both electrically conducting and non-conducting particles suspended in matrix. The particles are sub-micrometre sizes, and are formulated to reduce the temperature dependence, improve mechanical properties and increase surface durability. Applying a force to the surface of a the sensing film causes particles to touch the conducting electrodes, changing the resistance of the film. As with all resistive based sensors, force-sensing resistors require a relatively simple interface and can operate satisfactorily in moderately hostile environments. Compared to other force sensors, the advantages of FSRs are their size (thickness typically less than 0.5 mm), low cost and good shock resistance. However, FSRs will be damaged if pressure is applied for a longer time period (hours).



Source: [Wikipedia](http://en.wikipedia.org/wiki/Force-sensing_resistor)



##### Specs

*	$7.95/unit from [Sparkfun](https://www.sparkfun.com/products/9376)
*	Interlink [Guide](https://www.sparkfun.com/datasheets/Sensors/Pressure/fsrguide.pdf)
*	Buildr [Tutorial](http://bildr.org/2012/11/force-sensitive-resistor-arduino/)



##### Code

Source: [Johnny-Five - FSR Sensor](https://github.com/rwaldron/johnny-five/blob/master/docs/sensor-fsr.md)

Commented out code to control LED and added a console.log() to print out the sensor's readings.

```javascript
var five = require("johnny-five"),
    fsr;
    //led;

(new five.Board()).on("ready", function() {

  // Create a new `fsr` hardware instance.
  fsr = new five.Sensor({
    pin: "A0",
    freq: 25
  });

  //led = new five.Led(9);

  // Scale the sensor's value to the LED's brightness range
  fsr.scale([ 0, 100 ]).on("data", function() {

    // set the led's brightness based on force
    // applied to force sensitive resistor

    //led.brightness( this.value );
    console.log( this.value );
  });
});
```

![Arduino - FSR diagram](https://raw.github.com/site2site/object-oriented-office/master/docs/images/fsr_sensor_diagram.png)

##### Phone-home to Louis Identifier

_Ignore for now._

##### Examples in Use

_Optional._
