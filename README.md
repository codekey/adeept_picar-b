# Adeept 4WD Smart Car Kit for Raspberry Pi PiCar-B

## About This Product

## About Adeept

Adeept is a technical service team of open source software and hardware. Dedicated to applying the Internet and the latest industrial technology in open source area, we strive to provide best hardware support and software service for general makers and electronic enthusiasts around the world. We aim to create infinite possibilities with sharing. No matter what field you are in, we can lead you into the electronic world and bring your ideas into reality.

## Contact Info
 Technical Support:  support@adeept.com<br/>
 Customer Service:   service@adeept.com<br/>
 Website:            www.adeept.com<br/>


10/09/2019 Karl Yamashita
1. client.py: Added Police button to flash the front lights in a red/blue pattern. Added Middle button to return the wheels straight.
2. server.py: Had to comment out some calls to led.py as some gpio's were not setup yet so would crash the script if PC button 'Turn Left' or 'Turn Right' was clicked.
3. led.py: Added bothOnFlag. When calling police function it sets the flag if the front lights are on. So when police function finished the front light would go back to last state.
4. setup.py: Removed block comment around section that would create a car.desktop file that would run the server.py script when the RPi booted to the desktop. Without this car.desktop you could not connect to the car from the PC. The PC would try 5 times and fail.
Also the instructions fail to mention to modifiy the set.txt file in your root directory. You need to adjust the left/right/middle max values for the wheels. You can adjust the camera/ultrasonc min/max values from the client.py but not the wheels. When i get a chance i'll add adjustments to modify the set.txt file from the client.py gui.
