# Weather station Arduino MKR and Adafruit IO
This is an example of using Adafruit IO with Arduino  MKR1000 as weather station 
# Update 20/05/2016
you need to add these code lines in the file Adafruit_MQTT.cpp

#ifdef ARDUINO_SAMD_MKR1000
static char *dtostrf (double val, signed char width, unsigned char prec, char *sout) {
  char fmt[20];
  sprintf(fmt, "%%%d.%df", width, prec);
  sprintf(sout, fmt, val);
  return sout;
}
#endif
