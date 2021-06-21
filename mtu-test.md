
#### MTU Test Instructions

1. Search for "command prompt" in the Windows search bar.

2. Select **Run as administrator**



3. At the prompt "Do you want to allow this app..." click  **Yes**

4. In the command prompt enter (copy and paste this command):

`netsh interface ipv4 show subinterfaces`

5. You should see a network interface called "Ethernet" and an MTU value in the range 1400 - 1500. Please **make a note** of this value in the spreadsheet.

6. At the command prompt enter:

`netsh interface ipv4 set subinterface "Ethernet" mtu=1448 store=persistent`
