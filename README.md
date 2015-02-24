# Zanox API written in Javascript

This is an Api to access Zanox with nodejs. Installation:



```cmd
npm install zanox_api
```
See /examples for usage
This example gives you the sales as of 2013-05-20

This GitHub](https://github.com/jbt/markdown-editor) so let me know if I've b0rked it somewhere.

```javascript
var zanox_req, params, zanox;

zanox_req = require('zanox_api');

zanox = zanox_req(API_KEY, SHARED_SECRET);

params = { datetype: 'modifiedDate', state: 'approved' };

zanox.getAllSalesOfDate('2013-05-20', params, function(err, data)
{
  if (err != null)
  {
      return console.log('error', err);
  }
  return console.log('%j', data);
});

```
