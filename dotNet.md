
https://stackoverflow.com/questions/270531/how-can-i-determine-if-a-net-assembly-was-built-for-x86-or-x64

  - [reflection.assemblyname]::GetAssemblyName("${pwd}\Microsoft.GLEE.dll") | fl


https://stackoverflow.com/questions/56863631/is-it-possible-to-install-net-4-7-version-on-my-machine-when-net-4-8-is-alread


How to Check the .NET Framework Version with PowerShell?
 - http://woshub.com/how-to-check-net-framework-version/
    - Get-ChildItem ‘HKLM:\SOFTWARE\Microsoft\NET Framework Setup\NDP’ -Recurse | Get-ItemProperty -Name version -EA 0 | Where { $_.PSChildName -Match ‘^(?!S)\p{L}’} | Select PSChildName, version


<b>ASP.NET MVC 5</b>
https://docs.microsoft.com/en-us/aspnet/mvc/overview/getting-started/introduction/getting-started
