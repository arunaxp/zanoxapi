# Zanox API written in Javascript

This is an Api to access Zanox with nodejs. Installation:



```cmd
npm install zanox_api
```
```javascript
var zanox_req, params, zanox;

zanox_req = require('zanox_api');

zanox = zanox_req(API_KEY, SHARED_SECRET);

```

See /examples for usage.</br>
This example gives you the sales as of 2013-05-20
</br>Example 1

```javascript
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
Example 2
```javascript
params = {
    purpose: 'startpage',
    adspace: adspace,
    admediumtype: 'text',
    partnership: 'direct'
  };

  zanox.getAllAdmedia(params, function(err, data) {
    if (err != null) {
      return console.log('error', err);
    }
    return console.log('%j', data);
  });
 ```
 Example 3
```javascript
  params = {
    adspace: adspace,
    status: 'confirmed'
  };

  zanox.getAllProgramApplications(params, function(err, data) {
    if (err != null) {
      return console.log('error', err);
    }
    return console.log('%j', data);
  });
 ```
  Example 4
  ```javascript
    params = {
    datetype: 'modifiedDate',
    state: 'approved',
    zpar1: usrid.toString(),
    fromdate:'2014-1-1',
    todate:'2015-1-1',
    groupby:'MONTH'
  };

  z.getSalesOfDateRange(params, function(err, data) {
    if (err != null) {
      return console.log('error', err);
    }
    return console.log('%j', data);
  });
 ```
