  # Snake96

### Easy to use, reliable Windows96 library.

**Warning: Requires access to <a href="https://windows96.net">Windows96</a> and access to a developer console.**

How to get started:
1. Go to [https://windows96.net](https://windows96.net)
2. Wait for page to load
3. Paste the entirety of [main.js](https://raw.githubusercontent.com/telephone-line/Snake96/main/good%20stuff/main.js) into your developer console (`CTRL + Shift + I`)
And boom! You now have access to the rest of programs people have made.

---

# For Developers

How to use

### Alerts
```js
Snake96.ShowAlert("Your Text");
```
Of course you want to replace "Your Text", with, well, *your text*.

![](https://raw.githubusercontent.com/telephone-line/Snake96/main/alert.png)

### Play Audio
```js
var url = "<Your Audio URL>";
Snake96.PlayAudio(url);
```

### Set Wallpaper to a Custom Image URL
```js
var url = "https://snake.krab-cake.repl.co/snake96-disrupt.png"; // This is a placeholder URL, you can replace it with something else if you like.
Snake96.SetWallpaper(url);
```

### Open Link in IE (Expirmental)
```js
/* Warning: This is a non-use feature. Meaning: This is expiremental and will cause bugs! */
Snake96.OpenLinkInIE("https://telephone-line.verxcyhost.xyz"); // Replace with your URL
```

### Reboot OS
```js
/* Warning: This is a non-use feature. Meaning: This is expiremental and will cause bugs! */
Snake96.Reboot();
```

## GDI
### Rotate Screen 90 Degress
```js
Snake96.GDI.Rotate90Deg();
```
This one does basically what it sounds like, you can toy with it.

### Invert Colors (PatBLT)
```js
Snake96.GDI.InvertColors();
```
![](https://raw.githubusercontent.com/telephone-line/Snake96/main/Snake96InvertedColors.png)

Wondering how you can use these two things?
This snippet here showcases a cool GDI use for them:
- Warning, Flashing colors.
```js
var length = 1000; // In this case, modify length to be a integer.
for (i = 0; i < length; i++){
    setTimeout(function(){
        Snake96.GDI.InvertColors();
        Snake96.GDI.Rotate90Deg();
    }, 600 + (i * 2));
}
```
