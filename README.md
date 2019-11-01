# validator

To execute the travis build you may curl it with: 

 ```
 body='{
   "request": {
   "message": "Override the commit message: this is an api request",
   "branch":"master",
   "config": {
     "script": "sbt \"testOnly *Suite -- -z Suppliers\""
    }
  }}'
  
  
  
  curl -s -X POST \
   -H "Content-Type: application/json" \
   -H "Accept: application/json" \
   -H "Travis-API-Version: 3" \
   -H "Authorization: token xxxxx" \
   -d "$body" \
   https://api.travis-ci.com/repo/franciscolopezsancho%2Fvalidator/requests```