This is my own modified version of the jquery-ui themeswitcher widget.
Ever since jquery changed its hotlinking policies, the widget began to break.
So users started downloading it locally.
This gave me the opportunity to look at the code more closely.
Changes I decided to make:

* instead of creating the ul list with the jquery-ui themes with a single string, 
  I decided to construct an object that is then iterated to create the string with the ul list. 
  This way it is much easier to add / subtract themes from the list.
* I didn't like the loadTheme option triggering a click on the ul list and subsequently calling the onselect callback. 
  So I made a couple simple modifications to the cookie read / loadTheme option behaviour, 
  eliminating the click trigger and the onselect callback. 
  This way the onselect callback is only triggered when an actual user instantiated selection is made on the widget.

When [js-cookie](https://github.com/js-cookie/js-cookie/blob/latest/src/js.cookie.js "Javascript Cookie") is available the plugin utilizes it to save and load the most recently chosen theme.

Any other ideas for bettering this very useful plugin are welcome! And I hope it does make its way to jquery-ui core, 
or at least have some sort of presence on their repository...

[See it live here](https://johnrdorazio.github.io/Themeswitcher/ "JohnRDOrazio Themeswitcher")
