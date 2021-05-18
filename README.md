
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title> CALCULATOR</title>
</head>
<body>
    <h1> CALCULATOR</h1>
    <form action="/" method="post">
        <input type="text" name="num1" placeholder="first number">
        <input type="text" name="num2" placeholder="second number">
       <button type="submit" name="submit">CALCULTOR</button>
      <h3><br> sitanshu ranjan <br>email id--------  bit18ec122@bit.ac.in  </h3>
    </form>
</body>
</html>






const bodyParser = require("body-parser");
const express = require("express");

const app = express();
app.listen(3000);
app.use(bodyParser.urlencoded({extended: true}));

app.get("/", function(req, res))
 {
  res.sendFile(__dirname+"/index.html");
  
 }
 app.post("/", function(req, res))
 {
     var n1 = Number(req.body.num1);
     var n2 = Number(req.body.num2);
     var result = n1*n2;
     res.send("final answer:-" + result);
    console.log("req.body");
     res.send("thanx for posting the from");
 }
app.listen(3000, function() {
  console.log(" i am sitanshu ranjan , email id--------  bit18ec@bit.ac.in   ");
}
