---
layout: docs
title: Buttons
meta_description: Material design Buttons for Bootstrap 4 using some extra CSS classes for a perfect imitation.
description: Buttons allow users to take actions, and make choices, with a single tap.
group: material
redirect_from: "/docs/4.4/material/"
toc: true
---

Flat, outlined and raised buttons are the most commonly used types.

<div class="list-group mt-2 mt-lg-5">
    <a href="{{ site.baseurl }}/docs/{{ site.docs_version }}/components/buttons/" target="_blank" class="list-group-item list-group-item-action lgi-icon-bs">Bootstrap documentation: Buttons
      <span class="d-block font-weight-normal text-black-secondary"> Most of the details have been covered here</span>
    </a>
    <a href="https://material.io/components/buttons/" target="_blank" class="list-group-item list-group-item-action lgi-icon-md">Material Design guidelines: Buttons</a>
    <a href="https://material.io/components/buttons-floating-action-button" target="_blank" class="list-group-item list-group-item-action lgi-icon-md">Material Design guidelines: Buttons: floating action button</a>
    <a href="https://material.io/design/layout/applying-density.html" target="_blank" class="list-group-item list-group-item-action lgi-icon-md">Material Design guidelines: Applying density</a>
    <a href="https://material-components.github.io/material-components-web-catalog/#/component/button" target="_blank" class="list-group-item list-group-item-action lgi-icon-mdc">Material Components for the web: Buttons</a>
    <a href="https://material-components.github.io/material-components-web-catalog/#/component/fab" target="_blank" class="list-group-item list-group-item-action lgi-icon-mdc">Material Components for the web: Floating Action Button</a>
</div>

## Buttons

### Flat buttons

Flat buttons are text-only buttons (now called Text Buttons in MD). They may be used in dialogs, toolbars, or inline. They do not lift, but fill with color on press. Material adds `.btn-flat-*` buttons in order to own these elements.

Bootstrap's `.btn-link` is styled as a primary flat/text button.

{% capture example %}

<button class="btn btn-link" type="button">Btn-link</button>

<button class="btn btn-flat" type="button">Flat</button>
{% for color in site.data.theme-colors %}
<button class="btn btn-flat-{{ color.name }}" type="button">{{ color.name | capitalize }}</button>
{% endfor %}
{% endcapture %}
{% include example.html content=example %}

### Raised buttons

Raised buttons are rectangular-shaped buttons. They may be used inline. They lift and display ink reactions on press.

**Default buttons, i.e. `.btn`, are the equivalent of Material raised buttons. For more details, please refer to [Components/Buttons documentation]({{ site.baseurl }}/docs/{{ site.docs_version }}/components/buttons/#examples).**

{% capture example %}

<button class="btn" type="button">Raised</button>
{% for color in site.data.theme-colors %}
<button class="btn btn-{{ color.name }}" type="button">{{ color.name | capitalize }}</button>
{% endfor %}
{% endcapture %}
{% include example.html content=example %}

### Unelevated buttons

Unelevated buttons are easy to obtain : just add `shadow-none` class to your button.

{% capture example %}

<button class="btn shadow-none" type="button">Raised</button>
{% for color in site.data.theme-colors %}
<button class="btn btn-{{ color.name }} shadow-none" type="button">{{ color.name | capitalize }}</button>
{% endfor %}
{% endcapture %}
{% include example.html content=example %}

### Outlined buttons

**Outlined buttons have already been covered in the documentation. For more details, please refer to [Components/Buttons documentation]({{ site.baseurl }}/docs/{{ site.docs_version }}/components/buttons/#examples).**

{% capture example %}

{% for color in site.data.theme-colors %}
<button class="btn btn-outline-{{ color.name }}" type="button">{{ color.name | capitalize }}</button>
{% endfor %}
{% endcapture %}
{% include example.html content=example %}

### Shaped buttons

For rounded buttons, add `btn-shaped` class to your button. it also works for small and large buttons.

{% capture example %}

<button class="btn btn-primary btn-shaped" type="button">Normal</button>
<button class="btn btn-primary btn-sm btn-shaped" type="button">Small</button>
<button class="btn btn-primary btn-xs btn-shaped" type="button">XSmall</button>
<button class="btn btn-primary btn-lg btn-shaped" type="button">Large</button>
{% endcapture %}
{% include example.html content=example %}

### Density and icons

Recently, Google introduced **Density guidelines**, see the references at the top of page.

To reflect these changes with lowest impact on Bootstrap, here are our choices :

* btn is equivalent to **Default** button size
* btn-sm is equivalent to **Comfortable** button size
* `btn-xs` is introduced to represent **Compact** button size

At the same time, for easier icon integration within buttons (*Material icons*, *Fontawesome* or any other), `btn-icon-prepend` class has been created. Just add this class to your `.btn` for a proper icon's sizing and positioning.

<p class="typography-overline">Default</p>
{% capture example %}

<button class="btn btn-primary btn-icon-prepend" type="button"><i class="material-icons">add</i>button</button>
<button class="btn btn-flat-primary btn-icon-prepend" type="button"><i class="material-icons">add</i>button</button>
<button class="btn btn-outline-primary btn-icon-prepend" type="button"><i class="material-icons">add</i>button</button>
{% endcapture %}
{% include example.html content=example %}

<p class="typography-overline">Default shaped</p>
{% capture example %}

<button class="btn btn-primary btn-icon-prepend btn-shaped" type="button"><i class="material-icons">add</i>button</button>
<button class="btn btn-flat-primary btn-icon-prepend btn-shaped" type="button"><i class="material-icons">add</i>button</button>
<button class="btn btn-outline-primary btn-icon-prepend btn-shaped" type="button"><i class="material-icons">add</i>button</button>
{% endcapture %}
{% include example.html content=example %}

<p class="typography-overline">Comfortable standard</p>
{% capture example %}

<button class="btn btn-primary btn-sm btn-icon-prepend" type="button"><i class="material-icons">add</i>button</button>
<button class="btn btn-flat-primary btn-sm btn-icon-prepend" type="button"><i class="material-icons">add</i>button</button>
<button class="btn btn-outline-primary btn-sm btn-icon-prepend" type="button"><i class="material-icons">add</i>button</button>
{% endcapture %}
{% include example.html content=example %}

<p class="typography-overline">Comfortable shaped</p>
{% capture example %}

<button class="btn btn-primary btn-sm btn-icon-prepend btn-shaped" type="button"><i class="material-icons">add</i>button</button>
<button class="btn btn-flat-primary btn-sm btn-icon-prepend btn-shaped" type="button"><i class="material-icons">add</i>button</button>
<button class="btn btn-outline-primary btn-sm btn-icon-prepend btn-shaped" type="button"><i class="material-icons">add</i>button</button>
{% endcapture %}
{% include example.html content=example %}

<p class="typography-overline">Compact standard</p>
{% capture example %}

<button class="btn btn-primary btn-xs btn-icon-prepend" type="button"><i class="material-icons">add</i>button</button>
<button class="btn btn-flat-primary btn-xs btn-icon-prepend" type="button"><i class="material-icons">add</i>button</button>
<button class="btn btn-outline-primary btn-xs btn-icon-prepend" type="button"><i class="material-icons">add</i>button</button>
{% endcapture %}
{% include example.html content=example %}

<p class="typography-overline">Compact shaped</p>
{% capture example %}

<button class="btn btn-primary btn-xs btn-icon-prepend btn-shaped" type="button"><i class="material-icons">add</i>button</button>
<button class="btn btn-flat-primary btn-xs btn-icon-prepend btn-shaped" type="button"><i class="material-icons">add</i>button</button>
<button class="btn btn-outline-primary btn-xs btn-icon-prepend btn-shaped" type="button"><i class="material-icons">add</i>button</button>
{% endcapture %}
{% include example.html content=example %}

## Icon buttons

Daemonite Material brings brand new `btn-icon` class for buttons. Markup is simple : set a simple button with usual `btn` class, add `btn-icon` class and just place an icon in the button. See the examples below.

They also exist in Comfortable (`.btn-sm`) and Compact (`.btn-xs`) versions with smaller sizing.

<p class="typography-overline">Default</p>
{% capture example %}

<button class="btn btn-icon" type="button"><i class="material-icons">format_underline</i></button>
<a class="btn btn-icon" href="#"><i class="material-icons">attach_file</i></a>
<button class="btn btn-icon" type="button"><i class="material-icons">link</i></button>
<a class="btn btn-icon" href="#"><i class="material-icons">tag_faces</i></a>
{% endcapture %}
{% include example.html content=example %}

<p class="typography-overline">Comfortable</p>
{% capture example %}

<button class="btn btn-icon btn-sm" type="button"><i class="material-icons">format_underline</i></button>
<a class="btn btn-icon btn-sm" href="#"><i class="material-icons">attach_file</i></a>
<button class="btn btn-icon btn-sm" type="button"><i class="material-icons">link</i></button>
<a class="btn btn-icon btn-sm" href="#"><i class="material-icons">tag_faces</i></a>
{% endcapture %}
{% include example.html content=example %}

<p class="typography-overline">Compact</p>
{% capture example %}

<button class="btn btn-icon btn-xs" type="button"><i class="material-icons">format_underline</i></button>
<a class="btn btn-icon btn-xs" href="#"><i class="material-icons">attach_file</i></a>
<button class="btn btn-icon btn-xs" type="button"><i class="material-icons">link</i></button>
<a class="btn btn-icon btn-xs" href="#"><i class="material-icons">tag_faces</i></a>
{% endcapture %}
{% include example.html content=example %}

## Floating action buttons

A floating action button represents the primary action in an application, it is used for a promoted action.

{% capture example %}

<button class="btn btn-secondary btn-float" type="button"><i class="material-icons">favorite_border</i></button>
{% endcapture %}
{% include example.html content=example %}

### Colors

{% capture example %}

<button class="btn btn-float my-1" type="button"><i class="material-icons">favorite_border</i></button>
{% for color in site.data.theme-colors %}
<button class="btn btn-float btn-{{ color.name }} my-1" type="button"><i class="material-icons">favorite_border</i></button>
{% endfor %}
{% endcapture %}
{% include example.html content=example %}

### Dropdown

Floating action buttons can also work with dropdown menus to fling out related actions:

{% capture example %}

<div class="btn-float-dropdown dropdown">
  <button aria-expanded="false" aria-haspopup="true" class="btn btn-float btn-primary" data-toggle="dropdown" type="button"><i class="material-icons">add</i></button>
  <div class="dropdown-menu">
    <button class="btn btn-float btn-light btn-sm" type="button"><i class="material-icons">link</i></button>
    <button class="btn btn-float btn-light btn-sm" type="button"><i class="material-icons">link</i></button>
    <button class="btn btn-float btn-light btn-sm" type="button"><i class="material-icons">link</i></button>
  </div>
</div>
{% endcapture %}
{% include example.html content=example %}

Or flinging them upwards:

{% capture example %}

<div class="btn-float-dropdown dropup">
  <button aria-expanded="false" aria-haspopup="true" class="btn btn-float btn-primary" data-toggle="dropdown" type="button"><i class="material-icons">add</i></button>
  <div class="dropdown-menu">
    <button class="btn btn-float btn-light btn-sm" type="button"><i class="material-icons">link</i></button>
    <button class="btn btn-float btn-light btn-sm" type="button"><i class="material-icons">link</i></button>
    <button class="btn btn-float btn-light btn-sm" type="button"><i class="material-icons">link</i></button>
  </div>
</div>
{% endcapture %}
{% include example.html content=example %}

### Sizes

A smaller sized, i.e. mini floating action button, is also available.

{% capture example %}

<button class="btn btn-secondary btn-float btn-sm" type="button"><i class="material-icons">favorite_border</i></button>
{% endcapture %}
{% include example.html content=example %}

### Extended FAB

A larger FAB button has been introduced in recent Material guidelines. Add `btn-float-extended` class to your actual FAB.

To place icon after the label, use Bootstrap's flex utily `order-2`.

{% capture example %}

<button class="btn btn-secondary btn-float btn-float-extended" type="button"><i class="material-icons">add</i>Create</button>
<button class="btn btn-secondary btn-float btn-float-extended" type="button"><i class="material-icons order-2">add</i>Create</button>
{% endcapture %}
{% include example.html content=example %}

Extended FAB (without Icon)
{% capture example %}

<button class="btn btn-secondary btn-float btn-float-extended" type="button">Create</button>
{% endcapture %}
{% include example.html content=example %}

## Toggle buttons

Toggle buttons may be used to group related options, similar to [Components/Button group]({{ site.baseurl }}/docs/{{ site.docs_version }}/components/button-group/). Use flat buttons (i.e. `.btn-outline`s or `.btn-outline-*`s) instead of raised buttons to achieve a look that is more in line with the specifications laid out in Material Design Guidelines.

{% capture example %}

<div class="btn-group" data-toggle="buttons" role="group">
  <label class="btn btn-outline btn-sm active">
    <input autocomplete="off" checked name="options1" type="radio">
    <i class="material-icons">format_align_left</i>
  </label>
  <label class="btn btn-outline btn-sm">
    <input autocomplete="off" name="options1" type="radio">
    <i class="material-icons">format_align_center</i>
  </label>
  <label class="btn btn-outline btn-sm">
    <input autocomplete="off" name="options1" type="radio">
    <i class="material-icons">format_align_right</i>
  </label>
  <label class="btn btn-outline btn-sm">
    <input autocomplete="off" name="options1" type="radio">
    <i class="material-icons">format_align_justify</i>
  </label>
</div>
{% endcapture %}
{% include example.html content=example %}

Logically-grouped options, like Bold, Italic, and Underline, allow multiple options to be selected.

{% capture example %}

<div class="btn-group" data-toggle="buttons" role="group">
  <button class="btn btn-outline btn-sm" disabled><i class="material-icons">attach_file</i></button>
  <label class="btn btn-outline btn-sm active">
    <input autocomplete="off" checked name="options2" type="checkbox">
    <i class="material-icons">format_bold</i>
  </label>
  <label class="btn btn-outline btn-sm active">
    <input autocomplete="off" checked name="options2" type="checkbox">
    <i class="material-icons">format_italic</i>
  </label>
  <label class="btn btn-outline btn-sm active">
    <input autocomplete="off" checked name="options2" type="checkbox">
    <i class="material-icons">format_underlined</i>
  </label>
  <div class="btn-group" role="group">
    <button aria-expanded="false" aria-haspopup="true" class="btn btn-outline btn-sm dropdown-toggle" data-toggle="dropdown" id="toggleBtnDrop1" type="button"><i class="material-icons">format_color_text</i></button>
    <div aria-labelledby="toggleBtnDrop1" class="dropdown-menu dropdown-menu-sm">
      <a class="dropdown-item" href="#">color 1</a>
      <a class="dropdown-item" href="#">color 2</a>
      <a class="dropdown-item" href="#">color 3</a>
    </div>
  </div>
  <div class="btn-group" role="group">
    <button aria-expanded="false" aria-haspopup="true" class="btn btn-outline btn-sm dropdown-toggle" data-toggle="dropdown" id="toggleBtnDrop2" type="button"><i class="material-icons">format_color_fill</i></button>
    <div aria-labelledby="toggleBtnDrop2" class="dropdown-menu dropdown-menu-sm">
      <a class="dropdown-item" href="#">color 1</a>
      <a class="dropdown-item" href="#">color 2</a>
      <a class="dropdown-item" href="#">color 3</a>
    </div>
  </div>
</div>
{% endcapture %}
{% include example.html content=example %}

Purely flat toggle buttons can be achieved by adding `.btn-group-fluid` class.

{% capture example %}

<div class="btn-group btn-group-fluid" data-toggle="buttons" role="group">
  <label class="btn btn-outline btn-sm active">
    <input autocomplete="off" checked name="options3" type="radio">
    <i class="material-icons">format_align_left</i>
  </label>
  <label class="btn btn-outline btn-sm">
    <input autocomplete="off" name="options3" type="radio">
    <i class="material-icons">format_align_center</i>
  </label>
  <label class="btn btn-outline btn-sm">
    <input autocomplete="off" name="options3" type="radio">
    <i class="material-icons">format_align_right</i>
  </label>
  <label class="btn btn-outline btn-sm">
    <input autocomplete="off" name="options3" type="radio">
    <i class="material-icons">format_align_justify</i>
  </label>
</div>
{% endcapture %}
{% include example.html content=example %}

Vertical variation is also supported

{% capture example %}

<div class="btn-group-vertical" data-toggle="buttons" role="group">
  <button class="btn btn-outline btn-sm" disabled><i class="material-icons">attach_file</i></button>
  <label class="btn btn-outline btn-sm active">
    <input autocomplete="off" checked name="options4" type="checkbox">
    <i class="material-icons">format_bold</i>
  </label>
  <label class="btn btn-outline btn-sm active">
    <input autocomplete="off" checked name="options4" type="checkbox">
    <i class="material-icons">format_italic</i>
  </label>
  <label class="btn btn-outline btn-sm active">
    <input autocomplete="off" checked name="options4" type="checkbox">
    <i class="material-icons">format_underlined</i>
  </label>
  <div class="btn-group" role="group">
    <button aria-expanded="false" aria-haspopup="true" class="btn btn-outline btn-sm dropdown-toggle" data-toggle="dropdown" id="toggleBtnDrop3" type="button"><i class="material-icons">format_color_text</i></button>
    <div aria-labelledby="toggleBtnDrop3" class="dropdown-menu dropdown-menu-sm">
      <a class="dropdown-item" href="#">color 1</a>
      <a class="dropdown-item" href="#">color 2</a>
      <a class="dropdown-item" href="#">color 3</a>
    </div>
  </div>
  <div class="btn-group" role="group">
    <button aria-expanded="false" aria-haspopup="true" class="btn btn-outline btn-sm dropdown-toggle" data-toggle="dropdown" id="toggleBtnDrop4" type="button"><i class="material-icons">format_color_fill</i></button>
    <div aria-labelledby="toggleBtnDrop4" class="dropdown-menu dropdown-menu-sm">
      <a class="dropdown-item" href="#">color 1</a>
      <a class="dropdown-item" href="#">color 2</a>
      <a class="dropdown-item" href="#">color 3</a>
    </div>
  </div>
</div>
{% endcapture %}
{% include example.html content=example %}

## Usage

The type of button used should be suited to the context in which it appears.

<div class="table-responsive mb-3">
  <table class="table table-bordered table-striped mb-0">
    <thead>
      <tr>
        <th>Context</th>
        <th>Button type</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th>Always available</th>
        <td>If your app requires actions to be persistent and readily available, you can use the floating action button.</td>
      </tr>
      <tr>
        <th>Dialogs</th>
        <td>Use flat buttons in dialogs.</td>
      </tr>
      <tr>
        <th>Inline</th>
        <td>Flat buttons or raised buttons can be used for inline buttons.</td>
      </tr>
    </tbody>
  </table>
</div>

### Recommended button placement

#### Cards

Buttons are best placed on the left side of a card to increase their visibility. However, as cards have flexible layouts, buttons may be placed in a location suited to the content and context, while maintaining consistency within the product.

#### Forms

Button alignment on screen: Left.

Place the affirmative button on the left, the dismissive button on the right.

#### Standard dialogs

Button alignment on screen: right.

Place the affirmative button on the right, the dismissive button on the left.
