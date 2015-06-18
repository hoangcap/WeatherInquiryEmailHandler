# WeatherInquiryEmailHandler

##Problem:
You are the founder and CTO of your own company, WeatherForce.com and you have, for reasons known only to yourself, concluded that there is a market for a weather service which people interact with via email.

##Email Handling

    A customerwill email a weather enquiry to your Developer Edition Organisation and receive a short while later a reply ocntaining the details of the weather for the location they specified in the subject line.
    You will need to develop several components to handle this.
    You will need to write an ‘inbound email handler’ which:
        Receives the incoming email, saving its subject and body to a custom object that you will create.
        Get the email ‘From Address’ and check whether that particular sender is a Contact in the organisation, if it isn’t, create a contact.
    You will need to write a trigger on your Custom Object
        When the subject and body are saved, an insert trigger (experiment with before and after) will run which conducts a search of this weather service (http://www.webservicex.com/ws/WSDetails.aspx?CATID=12&WSID=56)  using the SOAP API described at the following WSDL (http://www.webservicex.net/globalweather.asmx?WSDL)
        You must conduct the web service call from the Trigger.
        You will store the response into a master detail record of the search by checking whether there exist a search query similar to that in the org, if there exist then the results in the response should be merged to the existing detail record of the search.
    Using Batch Apex and Scheduling you will then compose response emails using a Visualforce template which emails the search results back to the originating user. Also attach a PDF of the results to the email you send.
    
    
    Installation Url:https://login.salesforce.com/packaging/installPackage.apexp?p0=04t1000000035b5
    Password: whynotme123
    
    Contact me: ge.hoangct@gmail.com
