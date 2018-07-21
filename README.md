# S9-Volt-Rocket-Ship
Letting the S9 go to the MOON!

S9 Volt Rocket Ship



This is made for the 13.5th and 14th S9.

9v

The following is good to run at 800mhz and gets 17th/s and is STABLE and will almost max out the bitmain 1600w psu. This one is running at 8.8v and there are a few other small modifications that seemed to work better for the s9i. If you have an s9i use this one below for a stable 17th. I need some people to test this on 13.5 and 14th S9 non i models.

880


Upgrade instructions: 


Flash Fixed Frequency firmware.
ssh into your piner. For example, download and run Putty and connect to the ip of your miner.
Log into the miner in Putty root:admin
Type /etc/init.d/bmminer.sh stop
Run WinSCP and connect to your miners ip.
Go to remote directory /usr/bin and rename bmminer to bmminer.old (so we can always put it back)
Browse on your local side to wherever you downloaded the copy of bmminer and change their permissions of the file to executable.
Copy the now executable copy of bmminer onto your miner.
Now you should see bmminer and bmminer.old which is new and old.
In putty type: /etc/init.d/bmminer.sh restart
Got back to your miners web console and you should see in the kernal log it is running at 9v.
Go to minersip./cgi-bin/minerAdvanced.cgi and change the frequency of the miner. I would start at around 675mhz and run it for a few minutes and check for hardware errors.
Keep increasing the mhz until you find the spot where there are to many hardware errors happening in the miner status then roll it back some mhz until it is stable.


Now you can benefit from running your s9 like a Rocket Ship.. Get it 9Volt Rocket Ship... It is running at 9 volts muahahaha

• You can now increase your voltage up to whichever works best for you.
• If one of your fans is not working or is not reporting it to speed it will not complain and flood your kernal log.
• I believe I have it so no fans can be plugged in and it will hash perfect for immersive cooling.
• If you flashed to the fix frequency prior you have full fan control.
• If you are looking to hash at a lower speed at lower voltage I changed the following 650mhz to 631 8.8v 631 to 631mhz to 606mhz 8.7v 581mhz or less 8.6v. I might be changing this completely based on feedback.




Please post below any issues you have so I can tweak the file a bit more. Also please post what frequency you are able to run stable at and please let us know if it is a 13.5th or 14th unit. The goal of this mod is to make it so you can squeeze as much power as you can out of the bitmain psu so if you have cheap or free electricity you can benefit from the increased speed. If any of your miner turn off and don't immediately turn back on it is because the psu when into protective mode because it was drawing to much power. Please let me know if that happens to you and list which bitmain psu you have as some are capable of 1600w and some 1800w but we have noticed the ones rated at 1600w go much higher than that.

Please also post what temps you are running at and at which frequency.



Known Issues:


• Hashboard do not report temps but will still mine. Possible good and bad. If you have a hashboard with no temp reading it may work just fine with this mod. The miner will still stop mining if it overheats.


If you have any issues stop bmminer from putty and in WinSCP delete bmminer and then rename bmminer.old to bminner which will be your stock settings.



To compile from source

sudo dpkg --add-architecture i386
sudo apt-get update
sudo apt-get install git build-essential libz1:i386 libc6:i386 libstdc++6:i386


make clean
./setminertype S9
make