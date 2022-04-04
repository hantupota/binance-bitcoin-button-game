**Sure, it's quite stright forward.**

1. Install node from here, https://nodejs.org/dist/v16.14.2/node-v16.14.2-x64.msi

2. Open powershell on your windows machine(win key and start to write powershell) and verify that your node installation is done, it should look like this:

[![](https://i.imgur.com/8UFFV1f.png)

Node version number can differ.

3. Download .zip folder with bot:

![](https://i.imgur.com/hBaSdrj.png)

4. place it somehwere on your PC, I would extract it under C:\binance or whatever

5. Go to binance button website and sign in with twitter. Or your binance. With ctrl+shift+J open console and refresh page.

6. Now you need to acquire headers to authorize your bot. Open index.js with Sublime Text 3 or any other text editor.

These are the variables you will need to fill.
![](https://i.imgur.com/E0PODor.png)

Its a bit risky, you need to do a click on that big button in binance page, there is a chance you will succeed and burn account. Probably this could be avoided by looking up other requests your browser makes but I'm too lazy. So either click on button or investigate if you can find headers in any other requests.

It seems that other requests will contain those headers as we can see here(it's network tab in chrome dev tools):
![](https://i.imgur.com/sUwmp2V.png)

So use those. I like to be authentic as much as possible and I did risked to make a click to obtain real ones.

If you have questions about this step let me know, it can be confusing for beginner.

5. When its done, now cd from powershell into this directory by calling command "cd :\binance"

6. Run those commands in following order:
6.1. npm install
6.2. node index.js

That's it. Bot will connect to binance websockets and listen for timer to end and when the last miliseconds will come close, it will try to submit a click.

I posted this thread for shit n giggles and a bit for edu purposes as well because this shows how easy botting can bring you some serious opportunities.

When I was younger, I constantly won new mobile phones or gift cards by doing exactly this shit in social network games by hacking results, so it's possible to win.

No guarentees tho, there will be a lot of people going after that 1 BTC.

But by some luck it could be you.

# Installation instructions: 

- Install node.js
- Copy files to any directory
- Run following commands:
```
npm install -g pm2
npm install
npm index.js
```

When tested you can start a new process by:
```pm2 start index.js```

And then check logs:
```pm2 logs index.js```

> No guarentees or support whatsoever

