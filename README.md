HMC8553L Magnetometer (I2C digital compass) for MicroPython
===========================================

MicroPython driver class for HMC5883L magnetometer, using @rm-hull 's Python code and ported to use pyb.I2C

Usage example:
```python
>>>import hmc5883l
>>>compass = hmc5883l.HMC5883L(port = 2, gauss = "4.7", declination = (-2, 5))
>>>compass.heading()
34.45
```

* Uses continuous measurement mode. Single measurement mode can be easily implemented, though.
* You might want to tinker with 'gauss' value in constructor if you see that the output values do not correspond to the way sensor is moved. 
* Beware of magnets - this driver does not do calibration =(

References
----------
* http://magnetic-declination.com/Great%20Britain%20(UK) (dead link?)
