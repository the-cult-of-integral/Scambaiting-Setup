**Milestones:** 
- 10 stars. ✅
- 50 stars. ✅
- 69 stars. ✅([@ArchGryphon9362](https://github.com/ArchGryphon9362)).
- 100 stars. ❌
- 250 stars. ❌
- 420 stars. ❌
- 1000 stars. ❌

---

# Scam-baiting with a Windows 10 Host using Oracle's VirtualBox.

**Contents:**
- [A: What is scam-baiting?](#a-what-is-scam-baiting)
- [B: How do I set up a scam-baiting environment with VirtualBox?](#b-how-do-i-set-up-a-scam-baiting-environment-with-virtualbox)
  - [Installing VirtualBox](#installing-virtualbox)
  - [Creating a new Virtual Machine](#creating-a-new-virtual-machine)
  - [Installing Windows 10](#installing-windows-10)
- [C1: Disguising your Virtual Machine](#c1-disguising-your-virtual-machine)
- [C2: Further Disguising](#c2-further-disguising)
- [D: Further Scam-Baiting tools](#d-further-scam-baiting-tools)
- [E/F: Some Scam-Baiting YouTubers/Suggestions and resources](#e-some-scam-baiting-youtubers)

---
### A: What is scam-baiting?
Scam-baiting is the art of wasting a scammer's time in order to prevent real people from being affected by the scammer. Scam-baiting may also extend to more serious actions such as deleting files, locking scammers out of their computer, gathering information on scammers and more. Whilst these further activities are illegal, the chances of being raided by the police for messing with fraudulent scammers are pretty slim. However, it is still advised to take basic anonymity precautions.

### B: How do I set up a scam-baiting environment with VirtualBox?
Setting up a scam-baiting environment is not as hard as some people may think. Here is a full guide on how to do just that:

##### Installing VirtualBox:
Firstly, you'll need to install VirtualBox. It is recommended to use the latest version. To do this, [download VirtualBox here](https://download.virtualbox.org/virtualbox/6.1.12/VirtualBox-6.1.12-139181-Win.exe).

After the file has downloaded, install the file like how you would normally install software (e.g. Windows uses its installer wizard). After installing VirtualBox, run it. You should come across a screen that looks like this:

![Fresh VirtualBox Screen](https://user-images.githubusercontent.com/66549839/87617329-2eb0d880-c70f-11ea-84d7-2503422b3861.png)

---
##### Creating a new Virtual Machine:
When creating a new Windows 10 Virtual Machine, some users may find it hard to set it up correctly, even after downloading their Windows 10 ISO file - the same thing happened to me. However, now that I have the knowledge, it's actually incredibly easy, it's just that most first-time users wouldn't think of doing it. So, here is how to set up your Windows 10 Virtual Machine!
- Download the [Windows 10 ISO file](https://www.microsoft.com/en-us/software-download/windows10ISO).

- Head to the main screen of the VirtualBox application and click the blue **New** button.
- Name the Virtual Machine whatever you want and select its types as Microsoft Windows and its version as Windows 10 (64-bit).
- Allocate the machine however much RAM you want (Personally, I use 4 GB of RAM for my VMs, but you can use down to 2 GB).
- Keep the selection: "Create a virtual hard disk now", and click "Next".
- Keep the selection: "VDI (VirtualBox Disk Image)", and click "Next".
- Keep the selection: "Dynamically allocated", and click "Next".
- Give the machine a <ins>**reasonable**</ins> amount of space (Enough for the OS files and your own usage).
- After creating the machine, highlight it by clicking it once, then click the orange **Settings** button.
- Head to the **Storage** section via the left panel.
- You should see a disc icon that says: "Empty". Click on it to highlight it.
- After highlighting the disc, on the right panel there should be a label that reads: "Attributes". Underneath this label you should see another label that reads: "Optical Drive:" along with a drop down menu beside it. **Next to the drop down menu, click the small blue disc icon, then select: "Choose Virtual Optical Disk File"**.
- Select the Windows 10 ISO file that you downloaded earlier. After selecting the ISO file, press OK to close the Settings window.
- Highlight the Virtual Machine you just created and click the green **Start** button. From there, the machine will power on and begin installing Windows 10.

---
##### Installing Windows 10:
Before installing Windows 10 for scam-baiting, there are some important considerations you should take note of...
- When Windows 10 asks for an activation key, click the option to activate Windows 10 later (Which, of course, you won't do).

- Install Windows 10 Pro; it will give you access to regedit.
- **Never** use your real information. When Windows 10 asks for your Microsoft account's e-mail, choose the option to make a brand new outlook account. Furthermore, when Windows 10 asks you for its back-up account, you may want to use a random throwaway e-mail as well (For example, my throwaway email is cle************@protonmail.com); my real name does not begin with "cle".
- **Refuse all offers/services.** This includes finding your device, knowing your location, using your voice, etc.
- When setting your account's password, **do not set a password you use for your host machine or any other services.**
---
### C1: Disguising your Virtual Machine. 
##### The following guide is based upon [this video](https://www.youtube.com/watch?v=WCHZj0EXpOk) by UncleUdink.
One of the most important things to do with a Virtual Machine is to hide from scammers the fact that it is a Virtual Machine. Most scammers nowadays will check to see if the machine that they are connected to is a Virtual Machine or not to see if they are being baited and - if they find out it is a Virtual Machine, will usually disconnect and hang up. You can disguise an Oracle Virtual Machine by doing the following:
- [Download the vBoxSysInfoMod tool](https://github.com/JayMontana36/vBoxSysInfoMod/) (Remember to star the page if you have a GitHub account!). Then, run the `vBox System Info Mod.bat` file and follow the instructions in the terminal (For system manufacturer, you can use Dell - for system model, you can use any Dell Model (e.g. Optiplex 745)). **Note that you must stop your Virtual Machine if it is running to avoid corruption.**

- After this process is complete, you can take the following steps **within the Virtual Machine** to further hide it from scammers:
  - Run `regedit` using the run window (Win+R) and navigate to the following path: HKEY_LOCAL_MACHINE ➡️ SOFTWARE ➡️ Microsoft ➡️  Windows ➡️ CurrentVersion ➡️ Uninstall. Within this path, you should see a folder named "Oracle VM VirtualBox Additions". Delete this folder, as it will prevent the scammer from viewing it in `appwiz.csl` (If the folder does not exit, you have no need to worry!).
  
  - Following this, you then want to navigate to the following path: HKEY_LOCAL_MACHINE ➡️ SYSTEM ➡️ ControlSet001. 
  - Within this path, you should see a folder named, "Enum". Right click the folder and click: "Permissions". Then, click the "Add" button and enter your Virtual Machine's username in the text box. After entering the username, click the "Check Names" button, then click OK. Finally, go to the option you've just added and check: "Allow full control" then click: "Apply".
  - From here, click the "Advanced" button. At the top of the pop-up, click the "Change" link and, again, enter your Virtual Machine's username into the text box, then click: "Check Names", then click OK. Then, click: "Apply".
  - Next, re-open the Advanced menu and check the "Replace all child objects..." check box. Then, click "Apply" again and OK (Do not be alarmed at the checkbox becoming unchecked after applying).
  - Here is the tedious part. Right click the "Enum" folder and click find. From there, enter the following hash: `4d36e967-e325-11ce-bfc1-08002be10318` and click, "Find Next". Now, right click the "FriendlyName" option, click "Modify" and change the value to "Samsung 50 GB ATA".
  - Next, right click the "Enum" folder again and click "Find". Enter the following hash: `4d36e968-e325-11ce-bfc1-08002be10318` and modify the "DeviceDesc" to "Nvidia Geforce GTX 1080".
  - Next, right click the "Enum" folder again and click "Find". Enter the following hash: `4d36e965-e325-11ce-bfc1-08002be10318` and modify the "FriendlyName" to "NEC DVD-RW SATA DVD01".
  - Finally, right click the "Enum" folder again and click "Find". Enter the following hash: `4d36e96f-e325-11ce-bfc1-08002be10318` and modify the "DeviceDesc" to "Microsoft Pointing Device". Now click F3 twice and modify the next "DeviceDesc" to "Microsoft USB Pointing Device".

---
### C2: Further disguising:
So, you've changed all the complicated settings, good job! (**WARNING: IF USING VIRTUALBOX GUEST ADDITIONS, CLOSE THE TRAY ICONS USING THE TASK MANAGER. FURTHERMORE, YOU SHOULD DISABLE THE TASK MANAGER AND BLAME IT ON A VIRUS. FURTHERMORE, EJECT THE GUEST ADDITIONS CD FROM THE D: DRIVE.**)

However, a fresh PC is going to look suspicious, so remember to use [Ninite](https://ninite.com) to install some applications in the Virtual Machine (Download the files to your Virtual Machine, not your host).

Furthermore, you will also want to use a custom Desktop Background. **There is an easy way to do this without an activation key**. Simply download a picture from the internet onto your desktop. Then, **move** it to the Windows 10 file in the following path: `C:\Windows\Web\Wallpaper\Windows 10`. After this, simply right click the image and click, "Set as desktop background." Note that you can not adjust its crop, so choose an image that roughly fits the Virtual Machine's resolution.

#### Before saving a snapshot of your Virtual Machine, check you have done the following:
1. You have successfully edited the Virtual Machine using vmSysInfoMod tool.
2. You have successfully removed the Guest Additions folder from Regedit if using Guest Additions.
3. You have successfully edited each of the four hashes' values as shown above.
4. You have successfully installed some applications to make yourself appear innocent.
5. You have successfully changed the desktop background to match the pretend-victims personality.
6. You have successfully removed the guest addition tray icons using the task manager if using Guest Additions.
7. You have successfully disabled the task manager after this if using Guest Additions.

### If all of these requirements are met, save a snapshot of the machine.
This can be done using the top menu of the Virtual Box window: `Machine -> Take Snapshot`. Then, every time you finish a scam bait, when powering off the machine check the, "Restore to <snapshot name>" check box to revert back to this finished set-up state.

---
### D: Further scam-baiting tools.
- Google Hangouts, BobRTC, TextNow and Telegram are all good, free alternatives to FireRTC, which is essentially dead.

- You can use a RAT Creator (At your own risk!) and port forwarding to get access to a scammer's computer without the VM, using the VM as a service for which the scammer should download and run the file.
- You can use [fake name generator](https://www.fakenamegenerator.com) to give you several fake details.

---
### E: Some scam-baiting YouTubers:
- [Jim Browning](https://www.youtube.com/channel/UCBNG0osIBAprVcZZ3ic84vw) (Arguably the greatest Scam-Baiter to exist).
- [ScammerRevolts](https://www.youtube.com/channel/UC0uJKUXiU5T41Fzawy5H6mw)
- [Atomic Shrimp](https://www.youtube.com/user/AtomicShrimp)
- [Kitboga](https://www.youtube.com/channel/UCm22FAXZMw1BaWeFszZxUKw)
- [Trilogy Media](https://www.youtube.com/channel/UCca2961Ton2js_f9IDXK9Wg)
- [ScamBait Central](https://www.youtube.com/user/mbayowambayo)
- [Scammer Payback](https://www.youtube.com/channel/UCC9EjyMN_hx5NdctLBx5X7w)
- [JayBee TV](https://www.youtube.com/c/JayBeeTV/featured)
- [Joe Scambait](https://www.youtube.com/user/joeg1725/featured)

---
### F: Suggestions and resources.
A suggestion can be requested by creating an issue on this repository. Please make the suggestion as descriptive as possible, rather than just three words; it'll make it more likely to be added. Furthermore, a suggestion for you, the reader. You should probably visit the [Scambaiting Reddit](https://www.reddit.com/r/scambait/) as it may contain helpful resources.

---
# If this page helped, you may star it if you wish :)
