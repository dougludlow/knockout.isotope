knockout.isotope
================

A KnockoutJS binding for Isotope


## Requirements

* [jQuery](http://jquery.com/)
* [Knockout](http://knockoutjs.com/)
* [Isotope](http://isotope.metafizzy.co/)
* knockout.isotope.js plugin

```html
<script src="http://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.js"></script>
<script src="http://cdnjs.cloudflare.com/ajax/libs/knockout/3.0.0/knockout-debug.js"></script>
<script src="http://cdnjs.cloudflare.com/ajax/libs/jquery.isotope/1.5.25/jquery.isotope.js"></script>
<script src="src/knockout.isotope.js"></script>
```
    
## Usage

### Example Markup

```html
<div id="container" data-bind="isotope: { data: items, options: options }">
    <div class="item"></div>
</div>
```
  
### Example View Model

```javascript
$(function () {

  var vm = new ExampleViewModel(),
      items = [1, 2, 3, 4, 5, 6, 7, 8, 9];

  ko.applyBindings(vm);
  vm.items(items);
});

function ExampleViewModel() {
  var self = this;

  self.items = ko.observableArray([]);
  self.options = {
      itemSelector: '.item',
      masonry: {
          columnWidth: 500,
          gutterWidth: 25,
      }
  };
}
```
    
## Options

A javascript object containing the key/value pair [Isotope options](http://isotope.metafizzy.co/docs/options.html).
