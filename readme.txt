is video my ham kuch project bnany lgy hy us k liye 

1. run "npm init -y"
-> aik file bny gi jis my sara data/info hoti hy aap k project ki

2. run "npm i express"
-> the basic boiler plate of express is given below

======================================================
const express= require('express');
const app = express();

app.get("/", function(req,res){
    res.send("welcome")
})

app.listen(3000)
======================================================

express ka boiler plate code likhna hy sab sy pehly, 

3. Now setup engine for ejs
======================================================
app.set("view engine", "ejs");
======================================================

4. Now add these 2 lines for handling data from backend
======================================================
app.use(express.json());
app.use(express.urlencoded({extended:true}))
======================================================

5. Now write a line for linking HTML,CSS,JS files from public folder, you have to make that folder manually
this is actually a middleware
======================================================
app.use(express.static(path.join(__dirname, "public")))
======================================================

6. Now make a folder named "public", and make three folders in it, "images, javascripts, stylesheets"

7. Make nother folder named "views" having file named "index.ejs"

8. Now install nodemon
-> Run this command "npm i -g nodemon"
-> now run this command "npx nodemon index.js"
-> Aik error aaye ga, aap ny path use kiya hy but require nhi kiya
-> Add this line at the top "const path= require('path');"

9. Then change this line 
res.send("welcome"); 
to this
res.render("index"); 


10. Agr server nhi chal rha to run thses commands again
->npm i ejs
->npm i express


====================================================================

Yha sy ham proper kam shuru kry gy aaj ka
-> we're making a notes makign web app


1. Add tailwind css to index.ejs

2. const fs = require('fs')
write this

fs.readdir();
include this and this will help you ot read file system

aap input ka data sirf tab hi dekh skty ho ja busy name dety ho