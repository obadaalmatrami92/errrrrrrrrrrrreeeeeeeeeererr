## EJS tutorial 
### about : 
-  evaluate an injected var.
-  loop 
-  if statment 
-  layout 
-  partials
#### 
### gitteng startted ..
use this as a reference 
[link](https://scotch.io/tutorials/use-ejs-to-template-your-node-application)
- in server.js -> strat with init , express , body-parser , cors , ejs install. then app.use .. 
> app.use(path) its a build in no need to install which will join two paths the current and the chosen .

-  app.use body-parser and cors, then app.listen.

```js
var express = require('express');
var app = express();

// set the view engine to ejs
app.set('view engine', 'ejs');

// use res.render to load up an ejs view file

// index page 
app.get('/', function(req, res) {
    res.render('pages/index');
});

// about page 
app.get('/about', function(req, res) {
    res.render('pages/about');
});

app.listen(8080);
console.log('8080 is the magic port');
``` 
###### 
### how to inject variale ..
## 
the responce.render() takes 3 variables the first is the file name the second is the variables **in an obj** the third is the callback function(we will use 1&2).
- you can use the variable by its key as `<%= key %>` in the index.ejs file.
> note : `/<%= key% >/destroy` will deleat the roat.
### to loop ->
```
 <% for(var element of array) {%>
  <h1><%= element %></h1>
  <% }%>
```
-  everytime you make a change type nodemon
in ubuntu
### using if statement ->
```
<% for (var element of array ){%>
   <% if (statment){%>
   <h1><%=element%></h1>
   <%}%>
<%}%>
```
> it can be tricky to organize .. 

## 
