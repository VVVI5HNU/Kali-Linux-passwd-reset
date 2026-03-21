Step 1: Boot into Recovery Mode
Begin by rebooting your system. As Kali Linux starts, interrupt the boot process by pressing the “e” key when the GRUB menu appears. Locate the line starting with “linux” and add the following commands at the end
```
rw /initrd=/install/initrd.gz init=bin/bash
```
This ensures that Kali Linux starts in read-write mode with the bash shell.

Step 2: Apply Changes and Access Bash
Press “Ctrl + X” or “F10” to boot with the modified parameters. This will bring you to a bash shell prompt.

Step 3: Change the Password
To change the password, use the following command
```
passwd (username of kali)
```
You will be prompted to enter and confirm the new password. Once completed, you’ll receive a confirmation message.

Step 4: Restart the System
Execute the following command to restart the system
```
exec /sbin/init
```
This will bring your system back to its normal startup state.

Step 5: Login with the New Password
As the system reboots, you’ll be presented with the login screen. Enter the username “kali” and the new password you just set.
