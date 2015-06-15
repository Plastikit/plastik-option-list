plastik-option-list
============

`plastik-option-list` is a listbox that represents a list of selectable options that can be used in place
of a group of radio buttons or check buttons for filtering on a search form or similar use cases. It was
inspired by the [filter controls](http://i.imgur.com/kWMxW0X.png) in the new Google Maps Android app.

`plastik-option-list` provides the same behavior as `plastik-selector`, and thus, any attributes and
functionality supported by `plastik-selector` are likewise supported by `plastik-option-list`.

Demos and documentation are available on the [component page](http://www.plastikit.org/1.x/#!/components/plastik-option-list).

Pull requests are always welcome. If you encounter any bugs, please feel free to [submit an issue](https://github.com/Plastikit/plastik-option-list/issues/new/).

## Installation

```sh
bower install Plastikit/plastik-option-list --save
```
## Basic usage

 > _See [component page](http://www.plastikit.org/1.x/#!/components/plastik-option-list) for more details._

```html
    <plastik-option-list multi attr-for-reset="reset" attr-for-selected="value">
        <div value="" reset>Any</div>
        <div value="tier1">Free</div>
        <div value="tier2">$1 - $100</div>
        <div value="tier3">$101 - $500</div>
        <div value="tier4">$501+</div>
    </plastik-option-list>
```

## Compact mode

In compact mode, items in `plastik-option-list` cumulatively take up the entire
width of the element and are wrapped. This is useful for situations where there
is limited screen space, such as on a mobile phone. A recommended best practice
is to enable compact mode when the screen's width is under a certain threshhold.

Compact mode is enabled simply by applying the `compact` class to the element.

### Example

```html
    <plastik-option-list attr-for-selected="value" class="compact">
        <div value="5">Up to 5 miles</div>
        <div value="10">Up to 10 miles/div>
        <div value="20">Up to 20 miles/div>
        <div value="&gt;20">Over 20 miles/div>
    </plastik-option-list>
```
 
## Styling

`plastik-option-list` uses three CSS mixins to allow for customization.
 
 - `--item-theme` is applied to all items.
 - `--compact-item-theme` is applied to all items when the element is in
   compact mode.
 - `--selected-item-theme` is applied to all selected items.
 - `--wrapper-theme` is applied to the wrapper node which contains all
   of the items.
 - `--compact-wrapper-theme` is applied to the wrapper node when the element
   is in compact mode.

### Example

```html
    <dom-module id="my-custom-element">
      <style>
        :host {
          --selected-element-theme: {
            background-color: #B3E5FC;
            color: #000;
          };
        }
      </style>
      
      <template>
        <div>Search for:</div>
        <plastik-option-list multi attr-for-reset="reset">
          <paper-item>Any rating</paper-item>
          <paper-item>1 star</paper-item>
          <paper-item>2 stars</paper-item>
          <paper-item>3 stars</paper-item>
          <paper-item>4 stars</paper-item>
          <paper-item>5 stars</paper-item>
        </plastik-option-list>
      ...
```
