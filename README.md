# pine64

## Pine64 - PCA9685 PWM Servo driver
        Derived from the ADAFRUIT raspberry pi driver located at
        https://learn.adafruit.com/micropython-hardware-pca9685-pwm-and-servo-driver/software?view=all
        Free to use according to their license
        
@Hlynur Hansen - hlynur@tolvur.net

### i2cServoPCA0685.py
The first driver I create for pine64, derived from the ADAFRUIT driver itself

### EnableI2CPullup.zip
This is from the pine64 POT wiki, not my own work but crucial for the i2cServo to work

### Instructions:
sudo apt-get install python-smbus i2c-tools
sudo adduser username i2c
  *not sure if you need the group but i noticed no sudo needed to run i2c after added to group

### NOTE:
    To be able to use the I2C on the pine you need to download
    Enable Pullup from pine64 and download i2ctools, python-smbus
    EnablePullup ->
    http://wiki.pine64.org/images/d/d8/EnableI2cPullup.tar.gz
  
### USAGE:
     from i2cServoPCA9685 import PWN_DRIVER as PWN
     def run():
         a = PWN()
         a.test_servo()
