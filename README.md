##A python Socket Server

#It exposes 3 APIs:
1. GET request as `"/api/request?connId=<connection_id>&timeout=<timeout>"` . returns  `{"status" : "OK"}`  if successful else error with error code.
2. GET request as `"/api/serverStatus"` . Returns all running requests and time remaining to complete as JSON.
3.GET request as `"/api/kill?connId=<connection_id>"` . Kills the running request with given connId and returns `{"status" : "KILLED"}`  to killed request and `{"status" : "OK"}` to current request. If req not found returns `{"status" : "invalid connection id:<connection_id>"}` .
