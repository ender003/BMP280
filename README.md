Python BMP280
===================

This was forked from https://github.com/TomFoerster/BMP280

I made updates to get rid of warnings about incompatibility when running under python3 in the Thonny environment
on Raspberry Pi. I'm a beginner and the warnings were confusing at first. Hopefully this helps other beginners, too.
-ender003

===================

Python library for accessing temperature and pressure measurments of BMP280 chip

All modes of oversampling for temperature and pressure as well as filter settings are available via this library.

Tested with Adafruit BMP280 temperature pressure sensors: https://www.adafruit.com/products/2651

Code I used as a reference developing this:

https://github.com/vitally/BMP280

https://github.com/gradymorgan/node-BMP280

https://github.com/adafruit/Adafruit_Python_BMP

Installation
------------
To install run the setup.py file.

(e.g. sudo python setup.py install)

You need to have python and python-dev installed!

e.g. usage:
-----------
  
import BMP280.BMP280 as BMP280  
sensor=BMP280.BMP280()  
sensor.read_temperature_pressure()  
  
Make sure you have chosen the right i2c-address  
  
If you dont use the default i2c-bus 1 you can change this by the Argument busnum=x  

**See example file placed in ./examples/ for more guidance**

Options for Usage
-----------------
(e.g. sensor=BMP280.BMP280(modep=BMP280_LOWPOWER)  
  
####BMP280 default address  
BMP280_I2CADDR           0x77  
BMP280_I2CADDR2          0x76  
  
  
####SETTINGS FOR TEMPERATURE OVERSAMPLING  
(OVER x2 SAMPLE NO USE FOR PRESSURE ACCURANCY)  
modet=  
BMP280_T_O1            x1  Sample  
BMP280_T_O2            x2  Sample  
BMP280_T_O4            x4  Sample  
BMP280_T_O8            x8  Sample  
BMP280_T_O16           x16 Sample  
  
  
####PRESSURE OVERSAMPLING MODES  
modep=  
BMP280_ULTRALOWPOWER   x1  Sample  
BMP280_LOWPOWER        x2  Sample  
BMP280_STANDARD        x4  Sample  
BMP280_HIGHRES         x8  Sample  
BMP280_ULTRAHIGHRES    x16 Sample  
  
  
####FILTER SETTINGS        >=75% STEP_RESPONCE AFTER SAMPLE  
BMP280_FILTER_OFF      1  
BMP280_FILTER_2        2  
BMP280_FILTER_4        5  
BMP280_FILTER_8        11  
BMP280_FILTER_16       22  
  
  
Functions:  
----------  
_load_calibration(self)  
_set_filter(self)  
_load_datasheet_calibration(self)  
read_raw_temp_pressure(self)  
read_temperature_pressure(self)  
read_altitude(self, sealevel_pa=101325.0)  
read_sealevel_pressure(self, altitude_m=0.0)  
  
  
#HAVE FUN USING THIS LIBRARY  



