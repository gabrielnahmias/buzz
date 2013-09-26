# Buzz, a Javascript HTML5 Audio library

Buzz is a small but powerful Javascript library that allows you to easily take advantage of the new HTML5 audio element. It tries to degrade properly on non-modern browsers.

```js
(function() {

	var mySound = new buzz.sound( "/sounds/myfile", {
            formats: [ "ogg", "mp3", "aac" ]
        }),
    	update = function() {
            var timer = buzz.toTimer( this.getTime() );
            document.getElementById( "timer" ).innerHTML = timer;
        };
    
    mySound.play().fadeIn()
                  .loop()
                  .bind("timeupdate", update);
                  
})();
```

#### Official website
http://buzz.jaysalvat.com/

#### Real life demo
http://buzz.jaysalvat.com/demo/

#### Documentation
http://buzz.jaysalvat.com/documentation/

## Contributing

Please don't edit files in the `dist` subdirectory as they are generated via Grunt. You'll find source code in the `src` subdirectory!
Regarding code style like indentation and whitespace, **follow the conventions you see used in the source already.**
