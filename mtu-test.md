## MTU Configuration Instructions

Please review this spreadsheet before you start: 

https://docs.google.com/spreadsheets/d/10xtY3daQ6R3eTvyp_w56OFJM7ifQs73CnjWJLijhsl0/edit#gid=0

### 1. Open the command prompt

- Search for "command prompt" in the Windows search bar.
- Click **Run as administrator**
- When asked "Do you want to allow this app to make changes to your device?" click  **Yes**.

<img width="400" alt="commandprompt" src="https://user-images.githubusercontent.com/481602/122732046-38e43b00-d2bf-11eb-8ae7-c2ca9b7d4a2a.png">


### 2. Record your current MTU value

In the command prompt window, enter:

```
netsh interface ipv4 show subinterfaces
```
☝️ You can copy and paste this command

- This will print some information similar to the image below. 
- You should see a network interface called "Ethernet" with an MTU value (a number in the range 1400 - 1500). 
- Please **enter this value** in the spreadsheet in the column "Current MTU"

![netsh](https://user-images.githubusercontent.com/481602/122732255-721cab00-d2bf-11eb-871c-7f3ab02cc5c1.png)

### 3. Update your MTU value

If you are in **Test Group 1** enter:

`netsh interface ipv4 set subinterface "Ethernet" mtu=1450 store=persistent`

If you are in **Test Group 2** enter:

`netsh interface ipv4 set subinterface "Ethernet" mtu=1400 store=persistent`

This should respond with:

`Ok`

All done! Please enter a "Y" in the "Done" column in the spreadsheet next to your name.
