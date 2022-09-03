Hands-On Orgs
  - https://trailhead.salesforce.com/users/profiles/orgs

Q:

  - Apex unit testing 

Commands:
  - sfdx update
  - sfdx auth:web:login -d -a DevHub
  - git clone https://github.com/trailheadapps/dreamhouse-lwc.git
  - sfdx force:org:create -s -f config/project-scratch-def.json -a dreamhouse-org
  - sfdx force:user:permset:assign -n Dreamhouse
  - sfdx force:data:tree:import --plan data/sample-data-plan.json
  - sfdx force:org:list
  - sfdx force:org:open

  - sfdx force:project:create -n geolocation
  - sfdx force:org:create -s -f config/project-scratch-def.json -a GeoAppScratch
  - sfdx force:data:record:create -s Account -v "Name='Marriott Marquis' BillingStreet='780 Mission St' BillingCity='San Francisco' BillingState='CA' BillingPostalCode='94103' Phone='(415) 896-1600' Website='www.marriott.com'"
  - sfdx force:data:tree:export -q "SELECT Name, BillingStreet, BillingCity, BillingState, BillingPostalCode, Phone, Website FROM Account WHERE BillingStreet != NULL AND BillingCity != NULL and BillingState != NULL" -d ./data


  - geolocation>sfdx force:apex:class:create -n AccountSearchController -d force-app/main/default/classes

Apex:
  How can I turn my returned List<SObject> into a Set<Id>? Is the best option just a for loop?
    List<SObject> results = Database.query(someSOQL);
    Set<Id> resultIds = (new Map<Id,SObject>(results)).keySet();
    [https://salesforce.stackexchange.com/questions/8910/how-can-i-efficiently-generate-a-setid-from-a-listsobject-structure]

Ref:
  - <b>How to Choose Lightning Web Components or Aura </b>
    - https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.get_started_lwc_or_aura

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

