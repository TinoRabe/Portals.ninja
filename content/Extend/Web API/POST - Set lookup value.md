---
title: "POST: Set lookup value "
date: 2021-11-09T20:48:46+01:00
draft: false
---
Inject value from ***Liquid*** variable:
```js
webapi.safeAjax({
		type: "POST",
		url: "/_api/accounts",
		contentType: "application/json",
		data: JSON.stringify({
			"abc_CustomField@odata.bind: "/abc_entity({{id}})"
		}),
		success: function (res, status, xhr) {
			console.log("entityID: "+ xhr.getResponseHeader("entityid"))
		}
	});
```

Inject value from ***JavaScript*** variable:
```js
webapi.safeAjax({
		type: "POST",
		url: "/_api/accounts",
		contentType: "application/json",
		data: JSON.stringify({
			"abc_CustomField@odata.bind: "/abc_entity(+ variable +)"
		}),
		success: function (res, status, xhr) {
			console.log("entityID: "+ xhr.getResponseHeader("entityid"))
		}
	});
```
 
Hint:  
The part of 
```js
"abc_CustomField@odata.bind: "/abc_entity({{id}})"
```
 is case sensitive and perhaps doesn't the schema name of the lookup field. Also, the backend might append custom entity references at will. Therefore, check the metadata record for the technical name of the lookup name. 

 Access metadata:
```html
https://yourorg.crm.dynamics.com/api/data/v9.1/$metadata#EntityDefinitions
```