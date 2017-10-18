

```
npm install --save express

npm init
```

Procfile.md
```
web: node app/index.js
```


index.js
```
var express = require('express');
var app = express();
var port = process.env.PORT || 3000;

app.use(express.static(__dirname + '/'));

app.listen(port, function() {
  console.log('I am listening on port 3000!');
});
```

.gitignore
```
.DS_Store
node_modules/*
npm-debug.log
```

### important note
the index.js file has this line ...
<br>
app.use(express.static(__dirname + '/app'));
<br>

that line has to point to whatever directory the index.html is in