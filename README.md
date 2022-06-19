# stockticker-esp8266-ws2812b
Combination ESP8266 and WS2812B LED Matrix to create an scrolling LED stock ticker

Because I’m always trying to learn new things, I recently had the idea of building an Arduino powered stock ticker. If you’ve ever watched a live financial news program, you’ll often see scrolling text at the top or bottom of the screen. That text contains a stock symbols, it’s current price and the percent trend difference since it’s last display. The original project was listed here on GitHub. https://github.com/DKARDU/stock

What you need for this project

Hardware: 
+ ESP8266 (NodeMCU CP2102 ESP-12E) HiLetgo from Amazon. $7.99
+ WS2812B (RGB 8X32 256 Pixels LED Matrix) BTF-Lighting from Amazon. $20.99
+ Mini Solderless Breadboard Universal 400 Contacts (optional) from Amazon ~$2.50

Software:    
+ Arduino 2.0.0-rc6 IDE (not rc7 or newer)

Libraries: 
+ esp8266 by ESP8266 Community v2.4.2
+ Adafruit NeoPixel by Adafruit v1.5.0
  + Adafruit NeoMatrix by Adafruit v1.1.6
  + Adafruit GFX by Adafruit v1.11.1

Data: 
+ You’ll pull data from ThingSpeak ThingHTTP app
+ ThingHTTP app will pull financial data from Marketwatch 

Things to note:
+ The original project had a few bugs. (trending up = red; trending down = green)
+ The data you are parsing from Marketwatch is from after the markets close. You'd be surprised how sloppy a website formatting can be. This current version of the project works but if you want it "live" live, you need to parse data from a different location on the website. Once I solve for that, I'll update it here.
