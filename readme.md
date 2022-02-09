# Replit Bot Hosting Tutorial 2022 
In this tutorial I will be explaining how to host your discord bot 24/7 on replit without paying anything, that's right completely free (no hacker plan)

## Requirements:
- [x] Desktop/Laptop/Mobile 
- [x] Internet Access

## Setup:
- [x] Go to your `index.js` or main startup file and paste the following code on top
```javascript
var http = require('http');
http.createServer(function (req, res) { res.write("Server Online ✅"); res.end(); }).listen(8080);
```
- [x] Now click `▶️ Run` on the top middle and you should see a webpage on the top right corner
- [x] Copy the URL and use a uptimer website like [UptimeRobot](https://uptimerobot.com) or [Freshping](https://www.freshworks.com/website-monitoring/)
- [x] **Congratulations** 🎊 you have successfully made your discord bot online 24/7

## Important note:
If you are using replit to host your discord bot please don't paste your token in ANY file, or else someone can visit your replit profile and since you don't have hacker plan then he/she can view your token and do malicious things like nuke your servers, login your bot, and other things. It is highly recommended to paste your TOKEN in the replit "Secrets (Environment Variables)" because your TOKEN will be private
