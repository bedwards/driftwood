# Mac Studio headless notes

## Settings

Disable FileVault: This is non-negotiable for a truly headless server. If enabled, the Mac will wait for a password at the login screen before it can decrypt the drive, which you won't be able to enter without a physical keyboard.

Enable Automatic Login: This prevents the Mac from stopping at the user selection screen and waiting for a mouse click, ensuring it proceeds directly to the desktop.

Enable Screen Sharing (or Remote Management): This must be done before you unplug the physical monitor. You need to enable this service in the Sharing settings so you have a way to remotely connect to the Mac Studio once it's running.

Configure Power Settings: In System Settings > Energy Saver, enable the option to "Start up automatically after a power failure." This ensures your Mac Studio will restart and be accessible again if the power goes out.

Use a Headless Display Emulator: As mentioned above, this is the final piece of the puzzle to ensure your remote connection is smooth and not choppy.

## USB-C connection

This is an excellent solution for a fast and reliable connection between your two Macs. This is made possible by a built-in macOS feature called **Thunderbolt Bridge**. When you connect your Mac Studio and your MacBook Pro with a single USB-C to USB-C cable (which must be a Thunderbolt 3 or Thunderbolt 4 cable), the two computers automatically create a direct, high-speed peer-to-peer network connection. This is a much faster and more dependable link than using Wi-Fi, which is perfect for remote desktop sessions.

Here's how to set it up:

1.  **Connect the Cable:** Use a Thunderbolt 3 or 4 cable to connect a USB-C port on your Mac Studio to one on your MacBook Pro.
2.  **Open Network Settings:** On both Macs, go to **System Settings > Network**.
3.  **Configure Thunderbolt Bridge:** You should see a new network interface called **Thunderbolt Bridge** appear in the left-hand menu. Select it and ensure it's set to "Connected." You may need to assign a manual IP address to one of the Macs, or the network will likely self-assign IPs.
4.  **Connect Remotely:** Once the connection is established, you can use Screen Sharing on your MacBook Pro to connect directly to the Thunderbolt Bridge IP address of your Mac Studio.

This direct connection ensures that your remote desktop packets are transferred with minimal latency and maximum speed, creating a much smoother experience for all your tasks, including running your local LLMs.