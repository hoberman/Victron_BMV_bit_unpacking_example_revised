# Victron_BMV_bit_unpacking_example

Please note: Based on some questions from people attempting to use my sample code I
realize I may have a big-vs-little-endian byte ordering problem. Because of this, I have
created this revised version as a second try at getting this right. I'll point out (again)
that I don't have a BMV so I can't really test this in real life. I hope I'm
not leading anyone down the wrong path!

If it turns out that the revised code leads you to find the right way to decode the BMV Battery
Current field, please let me know so I can decommission my original version of the code.




This is an example of how to unpack the "Aux Input" and "Battery Current" fields
from Victron BMV devices' extra manufacturer data BLE broadcasts. Note that this
is not complete, as it does not include code to actually receive and unencrypt the
Victron-provided BLE extra manufacturer data. You will need to integrate the sample
coding below into a larger, more functional program.

This is related to the code in my Victron BLE decoding example:

https://github.com/hoberman/Victron_BLE_Advertising_example/blob/main/Victron_BLE_Advertising_example.ino

  Information on the "extra manufacturer data" that we're picking up from Victron SmartSolar
  BLE advertising beacons can be found at:
 
    https://community.victronenergy.com/storage/attachments/48745-extra-manufacturer-data-2022-12-14.pdf
 
Thanks, Victron, for providing both the beacon and the documentation on its contents!


Note that I don't have a BMV; this is only meant as an example for how to decode the
value once you have the data bytes from the BMV. Actual integration into your own code
is left as an exercise for the reader.

Also: Since I don't have a BMV, I can't test this to see if it actually works with real data.
If it turns out that I have this all wrong, please provide me some feeback via a Github issue
report. Thanks!
