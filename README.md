# Interrupt_and_SoftwareSerial_combined
A project that aims to use both Interrupt and Software Serial together.

Recently I was working on the Arduino Uno Board, where I wanted to do these three things simulatneously:
  1. Take the readings from a Pulsioximeter which was connected to a fixed Interrupt Pin(Pin - 6 on the Physical ).
  2. Encrypt the data.
  3. Send the commands and data along a Software Serial Channel to the ESP8266.
  4. Be able to debug the whole process.

# Alternative Approaches thought :
  1. I could have used the ESP8266WiFi library but eHealth library does not support changing the board.
  2. Using both the PinChangeInterrupt and SoftwareSerial together throws up the error of clashing of vectors, which is actually desirable for better individual performance.
  3. I could have connected the ESP266WiFi to the hardware ports, but that does not give the option of debugging.
# So the Saviour was NeoSWSerial that combines the two together.
  --Find further description in the simple code attached.
