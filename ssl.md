cmds:
  -  Get-ItemPropertyValue -Path HKLM:\SYSTEM\CurrentControlSet\Control\Cryptography\Configuration\Local\SSL\00010002 -Name Functions

Ref: 
- https://techcommunity.microsoft.com/t5/windows-server-essentials-and/installing-a-self-signed-certificate-as-a-trusted-root-ca-in/ba-p/396105
- https://community.sap.com/t5/technology-blogs-by-members/how-to-troubleshoot-client-certificate-authentication-for-inbound/ba-p/13503601
- https://osqa-ask.wireshark.org/questions/62098/how-to-find-out-which-ssl-cipher-suite-is-being-used/
- https://www.ibm.com/support/pages/why-do-i-keep-getting-ssl-peer-did-not-send-certificate-error-datapower