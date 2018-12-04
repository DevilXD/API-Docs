> *To begin using the API, you will first need to establish a valid Session. To do so you will start a session (via the createsession method) and receive a SessionId. Sessions are used for authentication, security, monitoring, and throttling. Once you obtain a SessionId, you will pass it to other methods for authentication. Each session only lasts for 15 minutes and must be recreated afterward.*
>
> *More details regarding Session creation are provided later in this document.*

I'll go ahead and explain session creation. It's pretty simple, here's a template URL for you to use:
```
http://api.paladins.com/paladinsapi.svc/createsessionJson/{devId}/{signature}/{timestamp}
```

The signature and timestamp will be documented in the development folder of the documentation. The current URL is for PC Paladins API, if you're looking for PS4 or Xbox you will have to change the endpoint although the rest is the same.

The response will
look something like this: 
```json
{ 
  "ret_msg": "Approved",
  "session_id": "69B765CF776E4436096FFD05F877CDA0F4",
  "timestamp": "12/4/2018 10:54:27 AM"
}

```

The `session_id` variable is the one you need the most, the other is just extra information that you could use if needed.

As previously stated in the documenation earlier, if you rather use XML then you could switch `createsessionJson` for `createsessionXML` and the response will be in XML format and look something like this:
```xml
<Session xmlns="http://schemas.datacontract.org/2004/07/PaladinsApi" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
  <ret_msg>Approved</ret_msg>
  <session_id>90C5CB0B953E4F299783F2E620BC60A1</session_id>
  <timestamp>12/4/2018 10:56:44 AM</timestamp>
</Session>

```
