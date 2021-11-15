---
title: "Pass Liquid Variable to JavaScript Function as Parameter"
date: 2021-11-10T19:57:31+01:00
draft: true
---
```html
{% for results in query %}
    <button onclick="MyCustomFunction('{{results.attribute1}}', {{results.attribute2}}', {{results.attribute3}}', )> </button>
{% endfor %}
```

```js
Check:
function MyCustomFunction (a, b , c) {
    console.log (arguments[0]);   // expects attribute1
    console.log (arguments[1]);   // expects attribute2
    console.log (arguments[2]);   // expects attribute3
};
```