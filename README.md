<div align="center">
	<img src="https://lolisafe.moe/88r6gPQS.png" />
</div>

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://raw.githubusercontent.com/kanadeko/Kuro/master/LICENSE)
[![Chat / Support](https://img.shields.io/badge/Chat%20%2F%20Support-discord-7289DA.svg?style=flat-square)](https://discord.gg/5g6vgwn)

### What does this do?
You know how LINE and Telegram have this beautiful sticker system where you can send different reactions with just one click? This is a new approach at doing exactly that but on Discord!

[It looks like this](https://lolisafe.moe/OXI6AEeH.mp4)

### How even?
By injecting the script into Discord it will automatically pull a curated list of sticker packs from [lolisafe](https://lolisafe.moe) and add them to your Discord client. After that a heart button will appear in your message bar where you'll be able to see all the stickers!

### Do I have to inject this on each restart?
Unless you use something like [mydiscord](https://github.com/justinoboyle/mydiscord) then yeah, everytime you start Discord you need to paste the script. I highly recommend using mydiscord and adding the minified script to the plugins array!

### So how exactly do I use it after adding the script?
It's very easy.
After opening the sticker popup click on the little tool icon and you'll see a list of available sticker packs. Clicking on a sticker pack will subscribe you to it, making every sticker on that pack available on the main window. You can also right click any sticker in the list and add them to your favorites for easy access! To remove one, right click on it again.

### Give me the code, I want to run this right now!
Press `Ctrl + Shift + i` or `CMD + Option + i` to open DevTools, and paste the following code inside:
```js
document.head.appendChild(document.createElement('script')).setAttribute("src", "https://cdn.rawgit.com/Pitu/Magane/cd777e32/dist/stickers.min.js")
```
If you are using mydiscord, make sure to add the following script to the plugins array:
```
https://raw.githubusercontent.com/Pitu/Magane/master/dist/stickers.min.js
```
If you are using BetterDiscord, make sure to add the following script to your plugins folder:
[script url](http://venipa.net/uploads/2017-11-12/6Y7VbESziChssX.js)

> Injecting random code into your Discord client could be harmful, that's why I provide the full source code so you can check out exactly what the script does. This plugin makes use of your personal token to make a request to the Discord api each time you click a sticker and never leaves nor does it do anything else with it. The script found in `/dist` is generated, webpacked and babeled from the source by running `npm run webpack`.
