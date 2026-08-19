Question 18 - Ransomware Investigation and Incident Report :

For this project, I am looking at a realistic network security crisis where a PC on a local network get hit with a ransomware. This threat is a very huge problem because it attack data availability by using strong encryption for locking up all your files, and then the hackers ask for untraceable cryptocurrency like bitcoin. The main point for this report is to show a step by step workflow on how to handle an incident, like how to isolate the threat, save the digital evidence, and safely restoring everything back to normal.

Tools I Used for the Analysis :

To check the network and doing the forensic steps, I used a few basic security tools that we learn about in the class:Wireshark: I use this for looking at data packets and network traffic to see how the infected PC was talking with outside networks.FTK Imager: I used this to do a live memory capture, which let you save a copy of the volatile RAM data before it disappear.Windows Event Viewer: This is just for checking system logs to see the timeline of when the virus actually start running.

My Steps for Handling the Attack :

1. Finding the ThreatThe incident was first found when a user say their computer became super slow and a weird ransom note pop up on the screen. The PC was almost completely freeze because the bad program was using up 100% of the CPU to encrypt all the files in the background. To check what was happening, I open the processes and see weird files running that shouldn't be there.
2. Stopping it from SpreadingBecause ransomware tries to spread more faster across the network to infect shared folders and another PCs, I had to contain it immediately. I did this by pulling out the LAN network cable and turned off the Wi-Fi on that computer. A big mistake people make is turning off the power completely, but you shouldn't do that because it destroy the volatile data in the RAM memory which we need for proof.
3. Saving the EvidenceBefore deleting anything or cleaning the PC, we need forensic proof to see how the hackers got inside. I ran FTK Imager from a safe USB drive to dump the RAM, because the temporary memory can sometimes hold the decryption keys or show the exact virus files. I also copied the ransom text note and a few locked files to a safe place for analyzing them.
4. Cleaning the ComputerJust running a basic antivirus scan is usually not enough for bad ransomware because it can hide secret files in the system registry that turn back on later. So to be completely safe, I decided to do a total storage wipe. I formatted the hard drive completely to erase all the bad stuff, install a fresh clean version of Windows, and then immediately installed the newest security patches and antivirus updates.
5. Getting Back to WorkWe never pay the ransom because it go against security rules and the hackers might just steal your money and give you nothing. Instead, I used our offline backup strategy. Since our backup drives were completely unplugged from the network when the attack happen, the virus couldn't touch them. I restored all the files from the last clean backup. Before letting the user back on the network.

Personal Reflection:

Handling this scenario showed me how important it is to follow a proper plan when a network gets hacked. It showed me that panicking and doing things like pulling the power plug can actually ruin an investigation because you lose the volatile RAM data. The project also prove that having a good offline backup is basically the only real defense against losing your files forever. Next time, I want to learn more about how to set up automated firewall rules to block these threats before they even get inside the local network.
