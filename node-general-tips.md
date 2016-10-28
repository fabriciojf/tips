# General Tips

### Http request

  - [Http.request](https://nodejs.org/docs/v0.4.11/api/http.html#http.request)

```javascript
var http = require('http');

var options = {
  host: 'fabriciojf.com',
  port: 80,
  path: '/site'
};

http.get(options, getOptionsReturn)
.on("error", function(e){
  console.log('Got error: ' + e.message);
});

function getOptionsReturn(resp) {
  resp.on('data', function(chunk){
    console.log('My Code Here');
  });
}
```
