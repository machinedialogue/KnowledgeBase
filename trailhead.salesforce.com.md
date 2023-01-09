

Hands-On Orgs
  - https://trailhead.salesforce.com/users/profiles/orgs

Q:
  - https://focusonforce.com/catalog/ 
  - https://jestjs.io/docs/mock-functions
  - SF community in Dhaka
  - post: LWC Arch
  - post: relationship
  - post: apex history
  - flow
  - case team
  - LWC data binding (2 way)
  - https://developer.salesforce.com/tools/vscode
  - Apex unit testing 
  - Custom Related List by Extentia
    - https://appexchange.salesforce.com/appxListingDetail?listingId=a0N3u00000MBg07EAD

Commands:

  - sfdx force:source:push --json --loglevel fatal
  - sfdx force:source:push --json --loglevel fatal --forceoverwrite
  - sfdx force:config:set defaultusername={ALIAS}
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
  
   -  https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql_relationships.htm
  
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
  
  - Salesforce Field Reference Guide  
      - https://developer.salesforce.com/docs/atlas.en-us.sfFieldRef.meta/sfFieldRef/salesforce_field_reference_Contact.htm
  
    combine date and time field with formula
    DATETIMEVALUE( TEXT(Start_Date__c)&' '& LEFT(TEXT( Start_Time__c ), 8) )
  
  - <b>Lightning Web Components Dev Guide</b>
     - https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.get_started_introduction
  
  - <b> # Dev Guide </b>
      - https://lwc.dev/guide/introduction
  
  - <b> Lightning Web Components Recipes </b>
    -  https://recipes.lwc.dev/#hello
    - https://github.com/trailheadapps/lwc-recipes
  
  - Get picklist values based on Record Types in LWC
    - https://blog.salesforcecasts.com/get-picklist-values-based-on-record-types-in-lwc/
    - get recordtypeid in LWC using
     - https://medium.com/@varma6228/getobjectinfo-in-lwc-1ffe490ea396
    - https://craftware.com/salesforce-lightning-web-components-chain-wire-methods/
  
  - <b>How to Choose Lightning Web Components or Aura </b>
    - https://developer.salesforce.com/docs/component-library/documentation/en/lwc/lwc.get_started_lwc_or_aura

  - https://salesforcescool.blogspot.com/2021/11/row-actions-in-lightning-datatable-in.html
  
  - VS Code - localhost 1717 error while Authorizing an Org
    - https://developer.salesforce.com/forums/?id=9062I000000IDtcQAG 

