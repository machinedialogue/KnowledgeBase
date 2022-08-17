https://playful-badger-pujdmc-dev-ed.lightning.force.com/lightning/n/Property_Explorer


Q:

  - Apex unit testing 



Ref:

  - VS Code - localhost 1717 error while Authorizing an Org
    - https://developer.salesforce.com/forums/?id=9062I000000IDtcQAG 

Speaking to windows here, the root cause of this issue is port exclusion by the WINNAT service (winnat randomly reserves some ports and disallows use by other processes). If WINNAT is not configured to leave port 1717 alone, it will randomly hold it (held ports can change with each reboot of your PC, causing the issue to appear random, or to fix after a reboot).

Run this command from a cmd prompt to see if port 1717 is being held by WINNAT:
netsh interface ipv4 show excludedportrange protocol=tcp

The command above will give output like this, in this case 1717 is between 1684 and 1783, so I am affected by the issue:
Start Port    End Port
----------    --------
        80          80
      1025        1124
      1545        1644
      1683        1683
      1684        1783
      1784        1883
      1884        1983
      1984        2083

If  it is, you have to stop the winnat service, exclude port 1717, and restart it using these commands (admin command prompt):
1)
net stop winnat
2)
netsh int ipv4 add excludedportrange protocol=tcp startport=1717 numberofports=1
3)
net start winnat

After running those commands, try your "SFDX: Authorize an Org" again.
