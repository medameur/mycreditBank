
 PUT /api/accounts/{accountId}/deposit
 ```
 Payload is as:
 
 ```json
 {
   "amount":2000
  }
 ```
  Response preview:
  ```json
  {
    "balance": 18080000,
    "latestOperations": [
        {
            "id": 967,
            "date": "2018-03-06T13:48:07.776Z",
            "type": "DEPOSIT",
            "amount": 20000
        }
        
        ]
  }
   ```
       
 2. Withdrawal of a given amount of money from an account:
  
 ```json 
 PUT /api/accounts/{accountId}/withdrawal
 ```
 payload is as :
    
 ```json
   {
    "amount":2000
   }
   ```
   Response preview :
    
 ```json
   {
    "balance": 12080000,
    "latestOperations": [
        {
            "id": 970,
            "date": "2018-03-06T13:48:11.754Z",
            "type": "WITHDRAWAL",
            "amount": -2000000
        },
   ]
  ```
  
 3. All operations (debit, credit) listing:
    
   ```json  
   GET /api/accounts/{accountId}/history
   ```
   
   Response preview:
   
   ```json
   [
    {
        "id": 962,
        "date": "2018-03-06T13:46:59.722Z",
        "type": "DEPOSIT",
        "amount": 20000
    },
    {
        "id": 963,
        "date": "2018-03-06T13:47:01.414Z",
        "type": "DEPOSIT",
        "amount": 20000
    }, ....
   ]
   ```
 4. Account balance and last operations (5 most recent ones):
 
   ```json 
    GET /api/accounts/{accountId} 
   ```  
   Response preview:
     
    
    {
                 "balance": 12080000,
                 "latestOperations": [
                    {
                        "id": 970,
                        "date": "2018-03-06T13:48:11.754Z",
                        "type": "WITHDRAWAL",
                        "amount": -2000000
                    },
                   ]
                         
     }
    

