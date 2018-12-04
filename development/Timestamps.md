Timestamps are used by signatures and embedded into URLs when sending requests, they have to be formatted properly to ensure the request completes without error. Here's some examples to get you started.

## JavaScript
### Using MomentJS library
```javascript
function timestamp()
{
  return moment().utc().format("YYYYMMDDHHmmss");
}
```

## PHP
### Using Carbon library
```php
private function getTimestamp()
{
  return Carbon::now()->format('Ymdhis');
}
```
