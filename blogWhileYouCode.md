## A blog style log while seting up the sensor board in the style of Mark Zuckerberg in the film the social network

It looks like the new imager settings where you can set wifi, username etc don't work on a custom imager

The 2019 version or raspian is getting pretty old now in 2024 and is no longer fully supported, I'll try a newer version at some point but last time I was building this project 2019 stretch was the newest version that would work, I guess google developed the board on pi around that time. We can no longer run `aprt-get update` or `apt-get dist-upgrade` continuing with the steps

I'm building this out with a screed this time, but as its all command line stuff it could be done with SSH enabled, though you would need to add the supliment file in the old school way

Failed, I think the age of the raspbian distro is causing issues here, I'm going to try with bullseye which has a 2024 update, fun fact, debian distro's are named after toy story chatachters
If this doesn't work, buster is my next best bet
Whilst thats flashing, lunch time

Avocado and tomato bagle gone, lets try bullseye

Demo works, kind of, the Temp is readint 21.77c, and the Pressure 100.33 but the light is NaN, and the RH (relative humidity) is NaN too, lets look in the setup here and dust off my python

I've done another `sudo apt upgrade` and spotted that there were errors with the `coral-enviro-drivers-skms` and `python3-coral-enviro`
