Hands-On Orgs
  - https://trailhead.salesforce.com/users/profiles/orgs

Q:
  - https://developer.salesforce.com/tools/vscode
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

<b>Apex</b>
  How can I turn my returned List<SObject> into a Set<Id>? Is the best option just a for loop?
    List<SObject> results = Database.query(someSOQL);
    Set<Id> resultIds = (new Map<Id,SObject>(results)).keySet();
    [https://salesforce.stackexchange.com/questions/8910/how-can-i-efficiently-generate-a-setid-from-a-listsobject-structure]

 <b>SOQL</b>
   - https://salesforce.stackexchange.com/questions/231708/soql-to-join-3-objects
  
  <b>Apex:</b>
    - get picklist
      ```
      Schema.DescribeFieldResult fieldResult = Case.Status.getDescribe();
      List<Schema.PicklistEntry> ple = fieldResult.getPicklistValues();
      for(Schema.PicklistEntry s:ple){
        System.debug('{label: "' + s.getLabel() + '", value: "' + s.getValue() + '"},');
      }
      ```
  
<b>Ref:</b>
  - <b>Lightning Web Components Dev Guide</b>
     - https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.get_started_introduction
  
  - <b> # Dev Guide </b>
      - https://lwc.dev/guide/introduction
  
  - <b> Lightning Web Components Recipes </b>
    -  https://recipes.lwc.dev/#hello
  
  - <b>How to Choose Lightning Web Components or Aura </b>
    - https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.get_started_lwc_or_aura

  - https://salesforcescool.blogspot.com/2021/11/row-actions-in-lightning-datatable-in.html
  
  - VS Code - localhost 1717 error while Authorizing an Org
    - https://developer.salesforce.com/forums/?id=9062I000000IDtcQAG 

