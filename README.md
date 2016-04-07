highlighter.js
==============

A jQuery plugin that allows for enabling tooltips on user selected text

[Demo](http://huffpostlabs.github.com/highlighter.js/ "Demo")

Usage
-----

Include the script on your page (make sure to use the correct path here)

```html
<script type="text/javascript" src="/js/jQuery.highlighter.js"></script>
```

Activate the highlighter on the element of your choice, e.g.

```javascript
$('.article').highlighter();
```

to deactivate it, use

```javascript
$('.article').highlighter('destroy');
```

The styling of the tooltip is completely up to you. This library will simply show and hide it in the correct position when appropriate.
You can use the ```selector``` option (see next section) to specify how highlighter.js can find your tooltip element. We have been using it with something like

```html
<span class='highlighter-container'>
    <div>
     ... my tooltip text ...
    </div>
</span>
```

Where the span has an absolute position, and the div is position relative.

### Options

On init you can pass in a settings object that will recognize two parameters:

```javascript
$('.article').highlighter({
                           'selector': '.highlighter-container',
                           'minWords': 0,
                           'complete': function (data) { }
});
```

Where ```selector``` is the jQuery selector string of the element that you want to show upon text being selected, and ```minWords``` is the minimum number of words that have
to be selected in order for the tooltip to appear. The defaults are ```'.highlighter-container'```, and ```0```, respectively.

And ```complete``` is a callback function that executes after the tooltip shows and ```data``` is a string that is the text selected


Compatibility
------

This plugin has been tested in Chrome, Firefox, Safari and IE 9.


Sightings in the Wild
-----

If you use this project in a production project, please contact the authors or submit a pull request on this list! We like to know other people find our work helpful.

* http://www.newrepublic.com/
* http://www.slate.com/


Authors
-----

- Matthew Conlen, mc@mathisonian.com

Contributors
-----

- GYatesIII, https://github.com/GYatesIII

License
-----
Copyright © 2012 Huffington Post Labs.

This program is free software. It comes without any warranty, to
the extent permitted by applicable law. You can redistribute it
and/or modify it under the terms of the WTFPL, Version 2, as
published by Sam Hocevar. See http://sam.zoy.org/wtfpl/
for more details.
