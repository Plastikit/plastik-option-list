plastik-option-list
============

`plastik-option-list` is a listbox that represents a list of selectable options that can be used in place
of a group of radio buttons or check buttons for filtering on a search form or similar use cases. It was
inspired by the [filter controls](http://i.imgur.com/kWMxW0X.png) in the new Google Maps Android app.

Demos and documentation are available on the [component page](https://www.plastikit.org/0.9/components/plastik-option-list/).

Pull requests are always welcome. If you encounter any bugs, please feel free to [submit an issue](https://github.com/Plastikit/plastik-option-list/issues/new/).

## Installation

```sh
bower install Plastikit/plastik-option-list --save
```
## Basic usage

 > _See [component page](https://www.plastikit.org/0.9/components/plastik-option-list/) for more details._
 
 ```html
<plastik-option-list multi attr-for-reset="reset" attr-for-selected="value">
  <div value="" reset>Any</div>
  <div value="0">Free</div>
  <div value="1-100">$1 - $100</div>
  <div value="101-500">$101 - $500</div>
  <div value="501+">$501+</div>
</plastik-option-list>
 ```
