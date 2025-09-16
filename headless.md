# Mac Studio headless notes

Disable FileVault: This is non-negotiable for a truly headless server. If enabled, the Mac will wait for a password at the login screen before it can decrypt the drive, which you won't be able to enter without a physical keyboard.

Enable Automatic Login: This prevents the Mac from stopping at the user selection screen and waiting for a mouse click, ensuring it proceeds directly to the desktop.

Enable Screen Sharing (or Remote Management): This must be done before you unplug the physical monitor. You need to enable this service in the Sharing settings so you have a way to remotely connect to the Mac Studio once it's running.

Configure Power Settings: In System Settings > Energy Saver, enable the option to "Start up automatically after a power failure." This ensures your Mac Studio will restart and be accessible again if the power goes out.

Use a Headless Display Emulator: As mentioned above, this is the final piece of the puzzle to ensure your remote connection is smooth and not choppy.