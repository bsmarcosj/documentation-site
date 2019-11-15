{
  "title": "Advise Messages",
  "hideGithubLink": true,
  "pagetitle": "AlertsX - Advise Messages",
  "description": "AlertsX - Advise Message",
  "weight": 6,
  "icon": "fa-comments",
  "isDirectory": false
}

[website-API]: https://api.travelgatex.com/
[customer-care]: https://xmltravelgate.atlassian.net/servicedesk/customer/portal/7


Here can be found posible advise message you would receive from travelgate [API][website-API] of AlertsX. 

# Advise message from create
   
| Type  | Code | Level | Description | Posible Causes | Solutions |
|:-:|:-:|---|---|---|---|
| STATUS INTERNAL SERVER ERROR | 500 | ERROR   | Error  | Somthing goes wrong while checking groups permissions  | Can check with your organization owner if you have all permissions. If the error persist contact us [here][customer-care]  |
| STATUS BAD REQUEST           | 400 | ERROR   | Error while quering to PostgreSQL  |   |   |
| STATUS INTERNAL SERVER ERROR | 500 | ERROR   | Error during the alert create: Error while retrieving results from maximum alerts  |   |   |
| STATUS INTERNAL SERVER ERROR | 500 | ERROR   | Error during the alert create: The maximum number of active alerts has been reached in  |   |   |
| STATUS INTERNAL SERVER ERROR | 500 | ERROR   | Error during the alert create: Failed to check maximum number of alerts active  |   |   |
| STATUS INTERNAL SERVER ERROR | 500 | ERROR   | Checking groups error  |   |   |
| STATUS INTERNAL SERVER ERROR | 500 | ERROR   | Error while creating the PostgresQL client:  |   |   |
| STATUS INTERNAL SERVER ERROR | 500 | ERROR   | "Error during the alert create:  |   |   |
| STATUS INTERNAL SERVER ERROR | 500 | ERROR   | "Error during the alert create:  |   |   |



# Advise message from update
   
| Type  | Code | Level | Description |
|:-:|:-:|---|---|
| NOT FOUND                    | 204 | WARNING | No alerts found                    |  
| STATUS INTERNAL SERVER ERROR | 500 | ERROR   | Error while quering to PostgresQL  |  
| STATUS BAD REQUEST           | 400 | ERROR   | Error while quering to PostgreSQL  |  


# Advise message from alerts
   
| Type  | Code | Level | Description |
|:-:|:-:|---|---|
| NOT FOUND                    | 204 | WARNING | No alerts found                    | 
| STATUS INTERNAL SERVER ERROR | 500 | ERROR   | Error while creating the PostgresQL client  |
| STATUS INTERNAL SERVER ERROR | 500 | ERROR   | Error while quering to PostgresQL  | 
| STATUS INTERNAL SERVER ERROR | 500 | ERROR   | Error for Marshal configuration  |  
| STATUS INTERNAL SERVER ERROR | 500 | ERROR   | Error for Unmarshal configuration  |
| STATUS INTERNAL SERVER ERROR | 500 | ERROR   | Configuration error  |  
| MISCELLANEOUS WARNING        | 199 | WARNING | Organization group type is not longer allowed, please update the alert with a product group type  |  
| MISCELLANEOUS WARNING        | 199 | WARNING | Folder group type is not longer allowed, please update the alert with a product group type  |  
| MISCELLANEOUS WARNING        | 199 | WARNING | GroupBy value is not correct |  |  |
| STATUS FORBIDDEN             | 403 | ERROR   | The member/members [***] do/does not have read permissions  |  

