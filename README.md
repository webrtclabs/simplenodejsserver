simplenodejsserver
==================
assuming you have node installed

##installation
1.Download node http://nodejs.org/
2.install express
``` command
npm install express
```
3.create server.js
```server.js


 var express = require("express");
 var app = express();
 
 /* serves main page */
 app.get("/", function(req, res) {
    res.sendfile('index.html')
 });
 
  app.post("/user/add", function(req, res) { 
    /* some server side logic */
    res.send("OK");
  });
 
 /* serves all the static files */
 app.get(/^(.+)$/, function(req, res){ 
     console.log('static file request : ' + req.params);
     res.sendfile( __dirname + req.params[0]); 
 });
 
 var port = process.env.PORT || 5000;
 app.listen(port, function() {
   console.log("Listening on " + port);
 });
 
 
```

4.create html page as i used index.html

```html
<html>
<head>
<title>
simple node js server by webrtclabs by quickstreamingmedia
</title>

</head>
<body>
done:P
<body>
</html>

```

5.run the server

```js
node server.js

```
6.done
:P

###running directly

1.install node
2.download master.zip
3.got odirectory where these files placed
4.run server.js

MIT licence 2014 by quickstreamingmedia

follow on twitter https://twitter.com/webrtclabs
