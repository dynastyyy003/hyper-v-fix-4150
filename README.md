# Hyper-V Bridge Network Connection (External Network)
 A fix for those who want to use WSL 2 on bridge networking.

> Note: This is my first time creating a GitHub repository, and I'm still learning. I hope this guide helps others facing similar issues.

## The Issue
As a student in digital cybersecurity, I often encountered problems where my virtual machine (WSL) needed an external network connection to run certain programs or scripts. Most tutorials I found on YouTube either had too many steps, caused me to lose my virtual machine's IP, or required formatting the machine.

While the internal network  allows for basic tasks, it's not suitable for practicing penetration testing or network testing, which require an external network connection.

After researching various manuals and forums, I found a simple solution to this problem.

# The Solution (Fix)
## Step 1: Enable Hyper-V
1. Press the Windows key and type: "Turn Windows features on or off."
2. Press ENTER to open the Windows Features window.
3. Ensure that the Hyper-V option is enabled. If it's not, check the box next to it.
4. Click OK and reboot your computer.

## Step 2: Create a Virtual Switch in Hyper-V Manager
1. After your computer restarts, press the Windows key and type: "Hyper-V Manager."
2. Press ENTER to open Hyper-V Manager.
3. In the left pane, click on your computer (probably should be the only thing to appear)
4. In the right pane, click on Virtual Switch Manager
5. In the Virtual Switch Manager window, click on "New virtual network switch" and click Create Virtual Switch
6. In the Virtual Switch Type section, select External Network.
7. Under Connection type, select the physical network adapter you want to use for the external network.
8. Under Name, give your virtual switch the name "Bridge" (exactly like that)
9. Ensure that Allow management operating system to share this network adapter is checked.
10. Click Apply and then OK to create the virtual switch.


## Step 3: Restart  WSL to Use the Virtual Switch
1. Open PowerShell as an administrator.
2. Run the following command to restart WSL and apply changes:

```
wsl --shutdown
``` 

3. Start WSL again by opening a new terminal or running:

```
wsl
```

## Step 4: Create .wslconfig file
1. Start your machine terminal 
2. Now you have to find your Windows User inside your terminal, the directory should be:
```
$ /mnt/c/Users/(Your User)
```
3. Once inside the folder, create a file called .wslconfig and copy the text bellow
![wslconfig](https://github.com/dynastyyy003/hyper-v-fix-4150/blob/main/wlsconfig.png?raw=true)




# Conclusion
This documentation was written late at night so if you encounter any issues or have questions, feel free to open an issue in this repository.
And also feel free to ask me any questions, I will answer them all as soon as possible.

> Observations:
> I still intend to create a video explaining step by step, but it depends on motivations that I don't have yet. If this mini step-by-step gets some views I will probably record the video immediately.
