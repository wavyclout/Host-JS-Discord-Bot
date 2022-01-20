# Replit Bot Hosting Tutorial 2022 
In this tutorial I will be explaining how to host your discord bot 24/7 on replit without paying anything, that's right completely free (no hacker plan)

## Requirements:
- [x] Desktop/Laptop/Mobile 
- [x] Internet Connection

## Setup:
- [x] Create a new file named `server.js` and paste the following code 
```javascript
const express = require('express');
const server = express();

server.all('/', (req, res)=>{

  res.setHeader('Content-Type', 'text/html');

  res.write('<link href="https://fonts.googleapis.com/css?family=Roboto Condensed" rel="stylesheet"> <style> body {font-family: "Roboto Condensed";font-size: 22px;} <p>Hosting Active</p>');

  res.end();

})
function keepAlive(){

  server.listen(3000, ()=>{console.log("Server is online!")});

}

module.exports = keepAlive;
```

- [x] Now go to the main file for your bot, for example `index.js` and paste this all the way on top of your file 
```javascript
const keepAlive = require("./server");
```
- [x] Lastly locate your client login, for example `client.login("TOKEN')` or `bot.login("TOKEN")`
- [x] Then paste `keepAlive();` on the top of `client.login` or any name that it's set to
- [x] Now click `▶️ Run` on the top middle and you should see a webpage on the top right corner
- [x] Copy the URL and use a uptimer website like [UptimeRobot](https://uptimerobot.com) or [Freshping](https://www.freshworks.com/website-monitoring/)
- [x] **Congratulations** 🎊 you have successfully made your discord bot online 24/7

## Important note:
If you are using replit to host your discord bot please don't paste your token in ANY file, or else someone can visit your replit profile and since you don't have hacker plan then he/she can view your token and do malicious things like nuke your servers, login your bot, and other things. It is highly recommended to paste your TOKEN in the replit "Secrets (Environment Variables)" because your TOKEN will be private

