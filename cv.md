# Artem Orlov

![Orlov Artem Sergeevich](https://github.com/GuyFox70/images/blob/master/K7ldyUj85UM.jpg)

For connect with me, you can to use following ways:

* *My phone number :* __+79096145081__;
* *My email adress :* __artm.orlov.88@list.ru__;
* *My Facebook page :* __[www.facebook.com](https://www.facebook.com/artem.orlov.566/)__;
* *My VK page :* __[www.VKontacte.com](https://vk.com/id106321171)__.

__*Also you can send me message in \"Whatsapp\" or \"Viber\" on phone number specify above.*__

## *A LITTLE BIT ABOUT MYSELF.*

I have one aim, it's study and develop like front end developer. I am very fastly catching new knowledges, purposeful (try always achieve what I think), responsible and community (I like meeting different people and talk on common themes and just everything). In future I want became full stack developer and I will be hard work for it. Unfortunately, I don't have commercial experience development, but I have several training projects and very big wish and aspiration to study. I always try improve my skills in programming and English.

## *Now about my skills.*

* __Languages:__
  * HTML
  * CSS
  * JavaScrip
  * Node JS
* __Frameworks__
  * Express
  * React
* __Ahother__
  * SCSS
  * Gulp
  * Jade
  * Socket (socket.io)
  * Git
  * PhotoShop
  * Figma
  
__A bit details, all that specified above, I know, but I'm not a guru, obviously everything know impossible, but we should tend to it. And I do it.__

## *My works*

By the way, I want to represent one of mine works and source code, which show you my skills. Rest works you may see in my [GitHub](https://github.com/GuyFox70). Please, don't condemn very strongly :-). There is no limit perfect.

### Snake
This is link for gh-pages [https://guyfox70.github.io/snake-gh-pages/](https://guyfox70.github.io/snake-gh-pages/).\
And this source code:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta http-equiv="X-UA-Compatible" content="ie=edge">
        <link rel="stylesheet" href="css/style.css">
        <title>Snake</title>
    </head>

    <body>
        <section class="field"></section>
    </body>

    <script src="js/snake.js"></script>
</html>
```

This is HTML, where I plugged styles, scripts and into tag 'body' placed tag 'section' with class 'field'. This class define game field. Next code will be javascript.

```javascript
(function () {
    class Game {
        constructor(field) {
            this._step = 10;
            this._delay = 250;
            this._top = 20;
            this._left = 20;
            this._size = ['7px', '7px'];
            this._currentCode;
            this._counter = 0;
            this._acceleration = 20;

            this._field = document.querySelector(field);
            this._snake = new Snake(4, this._field, this._step, this._top, this._left, this._size);
            this._start = new Start('.field');
            this._lose = new Lose(this._field);
            this._blink = new Blink(this._field);

            this._idInterval;
            this._idTimeOut;

            this._elems = this._snake.getSquares();
            this._coordinate = this._snake.getCoordinate(this._elems);

            this.run();
        }

        run() {
            this._start.getButton().addEventListener('click', () => {
                this._start.getWrap().classList.add('hide');

                this._currentCode = 37;

                this._idTimeOut = setTimeout(() => {
                    this._blink.showDIV(this.getNum(this.getWidthCss(this._field)),this.getNum(this.getHeightCss(this._field)), this._step);
                    
                    clearTimeout(this._idTimeOut);
                }, 2000);
  ```
                
In code above, I assign main class and constructor of class. In the constructor, I defined variables and start base method, which begin game. Full code you can find in Github. It was my first time, when I use OOP in javascript.
