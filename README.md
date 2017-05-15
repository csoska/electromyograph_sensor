# electromyograph_sensor
Uses an electromygraph sensor to process electrical signals and send them to other locations

This project uses a Myoware SEN-13723 ROHS muslce sensor. It can be purchased here: https://www.sparkfun.com/products/13723

The sensor has six solderable input pins; 3 are on each side. Each side has a power, ground, and signal pin. One side is raw EMG data in an analogue format and the oter side has a processed signal. The device has its own pot to ajust current (use a ceramic tool and multimeter while sensor is on).

The body of this project is a prebuilt leg brace with channels cut into it with a dremmel. 

I velcroed a Particle Photon to the body and ran the wires throught he channel. The particle code reads the processed signal data and sends it to the particle cloud. For info on setting up your photon, please see this site from Daragh Byren: http://diotlabs.daraghbyrne.me/

Once the particle is sending to the cloud, you can apply a webhook and set it to send a POST request to any server that can handle Restful operations. I used thingspeak. With the webhook already functioning, it is easy to also forward this data to another service. I sent mine to Twitter API for demo puroses. 

Feel free to change or modify this however you would like as per the license and let me know if you build something cool!
