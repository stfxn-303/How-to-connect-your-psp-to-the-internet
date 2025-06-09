
# WPA2PSP Plugin for PSP
The wpa2psp.prx plugin adds WPA2-PSK (AES) support to PlayStation Portable (PSP) systems running custom firmware (CFW). This allows older PSP models to connect to modern Wi-Fi networks that require WPA2 encryption.

# ⚠️ Requirements
A PSP with Custom Firmware (CFW) installed (e.g., PRO CFW, ME/LME)

Memory Stick with free space

```wpa2psp.prx``` plugin file

A PC or phone that can create a custom wireless hotspot

# 📝 Incase you haven't modded your psp or you don't know how to,

Check out my tutorial on how to mod your PSP [here](https://github.com/stfxn-303/Beginners-Guide-to-Modding-PSP3000) , come back here after you've done it :)

# 📦 Files Included
```wpa2psp.prx``` — main plugin file


# 📥 Installation Steps
Connect your PSP to your PC using USB mode.

Go to the root of your Memory Stick.

Place ```wpa2psp.prx``` in the seplugins folder:

Create ```seplugins``` if it doesn’t exist.

Example path: ```ms0:/seplugins/wpa2psp.prx```

Edit or create ```vsh.txt``` and game.txt in ```seplugins/```:

```ms0:/seplugins/wpa2psp.prx 1```

Exit USB mode and reboot your PSP.

Enter Recovery Menu by holding R during boot, or just press ```START``` or ```SELECT``` and go to the recovery menu via the mod menu.

Go to Plugins and enable ```wpa2psp.prx``` for ```VSH``` and ```GAME```.

# 📶 Creating an Insecure WPA2-Compatible Hotspot
Due to hardware limitations, even with WPA2 support, the PSP often struggles to connect to most modern routers. The solution: create a custom insecure hotspot with compatible settings.

# 📱 Option 1: Using an Android Device
Go to Settings > Network & Internet > Hotspot & tethering > Wi-Fi hotspot

Tap on Hotspot settings and change:

Security: Set to WPA2-Personal or None (depending on plugin success)

Band: Set to 2.4 GHz

Password: Use a simple one (e.g., psp12345)

SSID: Something short (e.g., PSPNet)

Save and activate the hotspot.

# ⚠️ If WPA2 still doesn’t work, temporarily set Security to "None" (open network) and try connecting without the plugin. This is for testing purposes.

💻 Option 2: Using a PC
Use software like Connectify, Virtual Router, or command prompt to set up a hotspot:


```netsh wlan set hostednetwork mode=allow ssid=PSPNet key=psp12345```
```netsh wlan start hostednetwork```
Be sure to allow Internet Connection Sharing (ICS) on the network adapter.

# 🌐 Connecting Your PSP
On your PSP, go to:

Settings → Network Settings → Infrastructure Mode
Create a new connection and select your custom hotspot.

Under Security Settings, choose:

WPA2-PSK (AES) (if using WPA2)

Or None (if testing with open network)

Complete the setup and test the connection.

# ❓ Troubleshooting
Still can't connect?

Try using an open network without encryption temporarily.

Ensure hotspot uses 2.4 GHz, not 5 GHz.

Double-check plugin is enabled in Recovery Menu.

Plugin not showing WPA2?

Reboot PSP after enabling the plugin.

Ensure correct paths in vsh.txt/game.txt.

# 🙏 Credits
Huge thanks to the developers who made WPA2 support possible on the PSP through this plugin.

