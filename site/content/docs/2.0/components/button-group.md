---
layout: docs
title: Button group
description: Group a series of buttons together on a single line with the button group, and super-power them with JavaScript.
group: components
toc: true
---

## Basic Example

Wrap a series of buttons with `.btn` in `.btn-group`. Add on optional JavaScript radio and checkbox style behavior with [our buttons plugin]({{< docsref "/components/buttons#button-plugin" >}}).

{{< example >}}
<div class="btn-group" role="group" aria-label="Basic example">
  <button type="button" class="btn btn-blue">Left</button>
  <button type="button" class="btn btn-blue">Middle</button>
  <button type="button" class="btn btn-blue">Right</button>
</div>
{{< /example >}}

{{< callout warning >}}
##### Ensure Correct `role` and Provide a Label

In order for assistive technologies (such as screen readers) to convey that a series of buttons is grouped, an appropriate `role` attribute needs to be provided. For button groups, this would be `role="group"`, while toolbars should have a `role="toolbar"`.

In addition, groups and toolbars should be given an explicit label, as most assistive technologies will otherwise not announce them, despite the presence of the correct role attribute. In the examples provided here, we use `aria-label`, but alternatives such as `aria-labelledby` can also be used.
{{< /callout >}}

## Button Toolbar

Combine sets of button groups into button toolbars for more complex components. Use utility classes as needed to space out groups, buttons, and more.

{{< example >}}
<div class="btn-toolbar" role="toolbar" aria-label="Toolbar with button groups">
  <div class="btn-group mr-2" role="group" aria-label="First group">
    <button type="button" class="btn btn-blue">1</button>
    <button type="button" class="btn btn-blue">2</button>
    <button type="button" class="btn btn-blue">3</button>
    <button type="button" class="btn btn-blue">4</button>
  </div>
  <div class="btn-group mr-2" role="group" aria-label="Second group">
    <button type="button" class="btn btn-blue">5</button>
    <button type="button" class="btn btn-blue">6</button>
    <button type="button" class="btn btn-blue">7</button>
  </div>
  <div class="btn-group" role="group" aria-label="Third group">
    <button type="button" class="btn btn-blue">8</button>
  </div>
</div>
{{< /example >}}

Feel free to mix input groups with button groups in your toolbars. Similar to the example above, you'll likely need some utilities though to space things properly.

{{< example >}}
<div class="btn-toolbar mb-3" role="toolbar" aria-label="Toolbar with button groups">
  <div class="btn-group mr-2" role="group" aria-label="First group">
    <button type="button" class="btn btn-blue">1</button>
    <button type="button" class="btn btn-blue">2</button>
    <button type="button" class="btn btn-blue">3</button>
    <button type="button" class="btn btn-blue">4</button>
  </div>
  <div class="input-group">
    <div class="input-group-prepend">
      <div class="input-group-text" id="btnGroupAddon">@</div>
    </div>
    <input type="text" class="form-control" placeholder="Input group example" aria-label="Input group example" aria-describedby="btnGroupAddon">
  </div>
</div>

<div class="btn-toolbar justify-content-between" role="toolbar" aria-label="Toolbar with button groups">
  <div class="btn-group" role="group" aria-label="First group">
    <button type="button" class="btn btn-blue">1</button>
    <button type="button" class="btn btn-blue">2</button>
    <button type="button" class="btn btn-blue">3</button>
    <button type="button" class="btn btn-blue">4</button>
  </div>
  <div class="input-group">
    <div class="input-group-prepend">
      <div class="input-group-text" id="btnGroupAddon2">@</div>
    </div>
    <input type="text" class="form-control" placeholder="Input group example" aria-label="Input group example" aria-describedby="btnGroupAddon2">
  </div>
</div>
{{< /example >}}

## Sizing

Instead of applying button sizing classes to every button in a group, just add `.btn-group-*` to each `.btn-group`, including each one when nesting multiple groups.

<div class="bd-example">
  <div class="btn-group btn-group-lg" role="group" aria-label="Large button group">
    <button type="button" class="btn btn-blue">Left</button>
    <button type="button" class="btn btn-blue">Middle</button>
    <button type="button" class="btn btn-blue">Right</button>
  </div>
  <br>
  <div class="btn-group" role="group" aria-label="Default button group">
    <button type="button" class="btn btn-blue">Left</button>
    <button type="button" class="btn btn-blue">Middle</button>
    <button type="button" class="btn btn-blue">Right</button>
  </div>
  <br>
  <div class="btn-group btn-group-sm" role="group" aria-label="Small button group">
    <button type="button" class="btn btn-blue">Left</button>
    <button type="button" class="btn btn-blue">Middle</button>
    <button type="button" class="btn btn-blue">Right</button>
  </div>
</div>

## Justified

Add the `.btn-group-justified` class to your `.btn-group` to make each button in the group the same size and span the full-width of its containing `div`. The buttons will remain the same size, regardless of the amount of text in each button.

{{< example >}}
<div class="btn-group btn-group-justified" role="group" aria-label="Justified button group">
  <button type="button" class="btn btn-red">Left Button with More Text</button>
  <button type="button" class="btn btn-blue">Middle</button>
  <button type="button" class="btn btn-info">Right Button</button>
</div>
{{< /example >}}

```html
<div class="btn-group btn-group-lg" role="group" aria-label="...">...</div>
<div class="btn-group" role="group" aria-label="...">...</div>
<div class="btn-group btn-group-sm" role="group" aria-label="...">...</div>
```

## Nesting

Place a `.btn-group` within another `.btn-group` when you want dropdown menus mixed with a series of buttons.

{{< example >}}
<div class="btn-group" role="group" aria-label="Button group with nested dropdown">
  <button type="button" class="btn btn-blue">1</button>
  <button type="button" class="btn btn-blue">2</button>

  <div class="btn-group" role="group">
    <button id="btnGroupDrop1" type="button" class="btn btn-blue dropdown-toggle" data-toggle="dropdown" aria-expanded="false">
      Dropdown
    </button>
    <div class="dropdown-menu" aria-labelledby="btnGroupDrop1">
      <a class="dropdown-item" href="#">Dropdown link</a>
      <a class="dropdown-item" href="#">Dropdown link</a>
    </div>
  </div>
</div>
{{< /example >}}

## Vertical Variation

Make a set of buttons appear vertically stacked rather than horizontally. **Split button dropdowns are not supported here.**

<div class="bd-example">
  <div class="btn-group-vertical" role="group" aria-label="Vertical button group">
    <button type="button" class="btn btn-blue">Button</button>
    <button type="button" class="btn btn-blue">Button</button>
    <button type="button" class="btn btn-blue">Button</button>
    <button type="button" class="btn btn-blue">Button</button>
    <button type="button" class="btn btn-blue">Button</button>
    <button type="button" class="btn btn-blue">Button</button>
  </div>
</div>


<div class="bd-example">
  <div class="btn-group-vertical" role="group" aria-label="Vertical button group">
    <button type="button" class="btn btn-blue">Button</button>
    <button type="button" class="btn btn-blue">Button</button>
    <div class="btn-group" role="group">
      <button id="btnGroupVerticalDrop1" type="button" class="btn btn-blue dropdown-toggle" data-toggle="dropdown" aria-expanded="false">
        Dropdown
      </button>
      <div class="dropdown-menu" aria-labelledby="btnGroupVerticalDrop1">
        <a class="dropdown-item" href="#">Dropdown link</a>
        <a class="dropdown-item" href="#">Dropdown link</a>
      </div>
    </div>
    <button type="button" class="btn btn-blue">Button</button>
    <button type="button" class="btn btn-blue">Button</button>
    <div class="btn-group" role="group">
      <button id="btnGroupVerticalDrop2" type="button" class="btn btn-blue dropdown-toggle" data-toggle="dropdown" aria-expanded="false">
        Dropdown
      </button>
      <div class="dropdown-menu" aria-labelledby="btnGroupVerticalDrop2">
        <a class="dropdown-item" href="#">Dropdown link</a>
        <a class="dropdown-item" href="#">Dropdown link</a>
      </div>
    </div>
    <div class="btn-group" role="group">
      <button id="btnGroupVerticalDrop3" type="button" class="btn btn-blue dropdown-toggle" data-toggle="dropdown" aria-expanded="false">
        Dropdown
      </button>
      <div class="dropdown-menu" aria-labelledby="btnGroupVerticalDrop3">
        <a class="dropdown-item" href="#">Dropdown link</a>
        <a class="dropdown-item" href="#">Dropdown link</a>
      </div>
    </div>
    <div class="btn-group" role="group">
      <button id="btnGroupVerticalDrop4" type="button" class="btn btn-blue dropdown-toggle" data-toggle="dropdown" aria-expanded="false">
        Dropdown
      </button>
      <div class="dropdown-menu" aria-labelledby="btnGroupVerticalDrop4">
        <a class="dropdown-item" href="#">Dropdown link</a>
        <a class="dropdown-item" href="#">Dropdown link</a>
      </div>
    </div>
  </div>
</div>

```html
<div class="btn-group-vertical">
  ...
</div>
```

### Block

Add the `.btn-group-block` class to your `.btn-group-vertical` to make all buttons and dropdowns inside inherit the `.btn-block` style, and span the full width of the containing `div`.

{{< example >}}
<div class="btn-group-vertical btn-group-block" role="group" aria-label="Block button group" style="max-width: 500px;">
  <button type="button" class="btn btn-red">Button</button>
  <div class="btn-group" role="group">
    <button id="btnGroupVerticalDropBlock" type="button" class="btn btn-blue dropdown-toggle" data-toggle="dropdown" aria-expanded="false">Dropdown
    </button>
    <div class="dropdown-menu" aria-labelledby="btnGroupVerticalDropBlock">
      <a class="dropdown-item" href="#">Dropdown link</a>
      <a class="dropdown-item" href="#">Dropdown link</a>
    </div>
  </div>
</div>
{{< /example >}}
