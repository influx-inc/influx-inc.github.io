## MTU Configuration Instructions

1. Search for "command prompt" in the Windows search bar.

2. Click **Run as administrator**

<img width="400" alt="commandprompt" src="https://user-images.githubusercontent.com/481602/122732046-38e43b00-d2bf-11eb-8ae7-c2ca9b7d4a2a.png">

3. When asked "Do you want to allow this app to make changes to your device?" click  **Yes**.

4. In the command prompt window, enter:

```
netsh interface ipv4 show subinterfaces
```
☝️ You can copy and paste this command

5. This will output some information similar to the image below. You should see a network interface called "Ethernet" with an MTU value (generally in the range 1400 - 1500). Please **make a note** of this value in the spreadsheet in the column "Previous MTU"

##![netsh](https://user-images.githubusercontent.com/481602/122732255-721cab00-d2bf-11eb-871c-7f3ab02cc5c1.png)

6. At the command prompt enter:

`netsh interface ipv4 set subinterface "Ethernet" mtu=1450 store=persistent`

7. All done! Please put a "Y" in the "Done" column in the spreadsheet next to your name.
