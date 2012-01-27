JS-Jigsaw
===
JS-Jigsaw is a MooTools based class which facilitates the filtering of items
based on their class, in an animated, &#039;fun&#039; way.

### Sample Instantiation &amp; Filtering

``` javascript

// instantiation
var jigsaw = (new Jigsaw(
    $$('ul#parent').shift(),
    $$('ul#parent').shift().getElements('li')
));

// events
$$('nav').shift().getElements('a').addEvent(
    'click',
    function(event) {
        event.stop();
        jigsaw.filter(this.get('rel'));
    }
);
```

This example showcases the following case:

 - Markup exists with a ul#parent tag
 - This list contains a series of list items (li tags)
 - The page contains a nav tag with a a series of anchor tags
 - Each anchor tag contains a *rel* attribute
 - Each anchor&#039;s *rel* value corresponds to a class that may be assigned to a
list item
 - Upon clicking on an anchor, the jigsaw begins, filtering out all list items
which do not contain the class specific by the *rel* attribute value

### Inspiration
[razorjack](https://github.com/razorjack/) has a wicked plugin called
[quicksand](https://github.com/razorjack/quicksand/). While not a direct port of
it, it was showed to me by a friend, and acts as the source of the inspiration
(albeit, a [MooTools](http://mootools.net/) version).
