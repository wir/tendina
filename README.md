Tendina
=======

A super easy-to-use jQuery plugin to rapidly build dropdown side menus.

![Tendina reveals!](/demo/tendina.gif "Tendina reveals")

[Demo CodePen](http://codepen.io/iprignano/full/tjoua)

Usage
===

To use Tendina, you just need to have some basic markup for your menu. That means you'll have some nested unordered lists, like this:

```html
<ul class="dropdown">
  <li>
    <a href="#">Menu 1</a>
    <ul>
      <li><a href="#">Submenu 1</a></li>
    </ul>
  </li>
  <li>
    <a href="#">Menu 2</a>
    <ul>
      <li><a href="#">Submenu 2</a></li>
      <li><a href="#">Submenu 2</a></li>
      <li><a href="#">Submenu 2</a>
        <ul>
          <li>Subsubmenu 2</li>
          <li>Subsubmenu 2</li>
        </ul>
      </li>
    </ul>
  </li>
  <li>
    <a href="#">Menu 3</a>
    <ul>
      <li><a href="#">Submenu 3</a></li>
      <li><a href="#">Submenu 3</a></li>
    </ul>
  </li>
</ul>
```

Next step is to have **jQuery** and **Tendina** in your page:

```html
<script src="http://code.jquery.com/jquery-1.11.0.min.js"></script>
<script src="tendina.js"></script>
```

Finally, you can simply call the function on your list to transform it in a snappy side menu:

```javascript
$('.dropdown').tendina()
```

The plugin supports three-level-deep nesting (`ul > li > ul > li > ul > li`). Bring on dem categories!

Tendina will hide your nested submenus and manage all interactions with a nice slideUp/Down effect. You can even call Tendina on dinamically added elements (nice to have when building a menu from a JSON tree)!

I made this plugin just to handle menu interactions in a flexible way. As a result, Tendina comes with **no styles at all**. This means you don't need to override useless CSS classes, and you have total control on the styling of your menu. Additionally, Tendina will add a "selected" class to the currently open menu, so you can customize its looks without adding other Javascript code!

Contributing
===

Contributions are welcome! In order to contribute, you can use the [Fork & Pull Model](https://help.github.com/articles/using-pull-requests#fork--pull).

Bonus sugar: Tendina comes with a easy-to-use Grunt configuration.

Given you have `npm` and `grunt-cli` installed, you just need to run `npm install` in the project folder once to install all the dev dependencies. 
Then, just execute `grunt watch`: this way Grunt will spawn a watcher that will compile the Coffee and minify the resulting Javascript everytime you edit `tendina.coffee`.

License
===

Tendina is released under the MIT License.

The MIT License (MIT)

Copyright (c) 2014 Ivan Prignano

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.