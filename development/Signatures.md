# What are they?
Signatures are used heavily through the API. Why? I guess it's just how they like to do it. Instead of using something like access tokens where we embed it in an authorization header upon request, everything is embeded in the URL. Knowing this, they make it hashed as to not reveal the auth key they give us to anyone sniffing on the network. 

Signatures use 4 items to be created:
- Developer ID
- Auth key
- Method (without response format, eg Json)
- Current timestamp (covered in the Timestamp documenation)

Here's some example functions, feel free to add more.

## JavaScript
```javascript
function signature(method)
{
    return md5(`${devId}${method}${authKey}${timestamp()}`)
}
```

## PHP
```php
private function getSignature($method)
{
    return md5($this->devId . $method . $this->authKey . $this->getTimestamp());
}
```
