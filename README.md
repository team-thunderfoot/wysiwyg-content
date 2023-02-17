# wysiwyg-content

## Stylized blocks

- block-btn
- block-footnote
- block-highlighted (highlighted paragraph)
- block-image
- block-quote
- block-separator
- block-table
- headings
- links
- lists
- paragraphs
- utilities


## Use

Install package
```sh
npm i @teamthunderfoot/wysiwyg-content
```

Import content mixins at the beginning of the c--content stylesheet
```sh
@import "@teamthunderfoot/wysiwyg-content/src/scss/_mixins.scss";
```

Your HTML structure should look like this

```sh
<div id="c--content-a">
  <?= apply_filters('the_content',get_the_content()) ?>
</div>
```

Copy c--content styles and change parameters with the ones we want
```sh
.c--content-a {
    @include block-btn(
        $btn-class: g--btn-01
    );
    // @include block-btn-modifier(
    //     $btn-class-modifier: g--btn-01--second
    // );

    @include block-footnote(
        $text-font: e,
        // $text-font-weight: default,
    );
    @include block-footnote-modifier(
        $text-color: map-get($color-options, a)
    );

    @include block-highlighted(
        $text-font: c,
        // $text-font-weight: default,
    );
    @include block-highlighted-modifier(
        $text-color: map-get($color-options, a)
    );

    @include block-image(
        $caption-font: g,
        // $caption-font-weight: default,
        // $img-border-radius: default
    );
    @include block-image-modifier(
        $caption-color: map-get($color-options, a)
    );

    @include block-quote(
        $quote-font: d,
        $quote-font-style: italic,
        $cite-font: e,
        $cite-font-style: normal,
        // $quote-font-weight: default,
        // $cite-font-weight: default,
    );
    @include block-quote-modifier(
        $quote-color: map-get($color-options, a),
        $cite-color: map-get($color-options, a),
        $border-color: map-get($color-options, e),
        $border-width: 1px,
    );

    @include block-separator();
    @include block-separator-modifier(
        $separator-width: 1px,
        $separator-color: map-get($color-options, e),
    );

    @include block-table(
        $first-row-font: d,
        $other-rows-font: d,
        $caption-font: f,
        // $first-row-font-weight: default,
        // $other-rows-font-weight: default,
        // $caption-font-weight: default,
    );
    @include block-table-modifier(
        $first-row-border-width: 1px,
        $first-row-border-color: map-get($color-options, a),
        $other-rows-border-width: 1px,
        $other-rows-border-color: transparent,
        $first-row-background: map-get($color-options, a),
        $even-rows-background: map-get($color-options, d),
        $odd-rows-background: map-get($color-options, b),
        $first-row-text-color: map-get($color-options, d),
        $other-rows-text-color: map-get($color-options, a),
        $caption-color: map-get($color-options, a)
    );

    @include headings(
        $h2-font: b,
        $h3-font: c,
        $h4-font: c,
        $h5-font: d,
        $h6-font: d,
        // $h2-font-weight: default,
        // $h3-font-weight: default,
        // $h4-font-weight: default,
        // $h5-font-weight: default,
        // $h6-font-weight: default,
    );
    @include headings-modifier(
        $h2-color: map-get($color-options, a),
        $h3-color: map-get($color-options, e),
        $h4-color: map-get($color-options, f),
        $h5-color: map-get($color-options, a),
        $h6-color: map-get($color-options, a),
    );

    @include links(
        $link-class: g--link-01
    );
    // @include links-modifier(
    //     $link-class-modifier: g--link-01--second
    // );

    @include lists(
        $text-font: d,
        $one-number-width: 22px,
        $first-level-dot-width: $measure,
        $first-level-dot-top: 13px,
        // $second-level-dot-width: default,
        // $second-level-dot-top: default,
        // $third-level-dot-width: default,
        // $third-level-dot-top:default,
        // $text-font-weight: default,
    );
    @include lists-modifier(
        $text-color: map-get($color-options, a),
        $number-color: map-get($color-options, f),
        // $first-level-dot-image: default,
        // $first-level-dot-background: default,
        // $first-level-dot-border-width: default,
        // $first-level-dot-border-color: default,
        // $second-level-dot-image: default,
        // $second-level-dot-background: default,
        // $second-level-dot-border-width: default,
        // $second-level-dot-border-color: default,
        // $third-level-dot-image: default,
        // $third-level-dot-background: default,
        // $third-level-dot-border-width: default,
        // $third-level-dot-border-color: default,
    );

    @include paragraphs(
        $text-font: d,
        // $text-font-weight: default,
    );
    @include paragraphs-modifier(
        $text-color: map-get($color-options, a)
    );

    @include utilities();
    
    *:last-child {
        margin-bottom: 0px;
    }
}
```

All blocks except utilities have 2 mixins, one for styles and the other one for colors and modifiers.

### block-btn

Styles the default wordpress block.
With the block-btn mixin, you can choose an existing class for the btn.
With the block-btn-modifier mixin, you can add a modifier class to the btn, you can add this mixin or not.
* All classes you add here must exist and be included in the entry before the c--content stylesheet

#### Editable variables

- $btn-class

#### Editable variables for Modifiers

- $btn-class-modifier


### block-footnote

This is a custom block.

#### Editable variables

- $text-font
- $text-font-weight: false by default

#### Editable variables for Modifiers

- $text-color


### block-highlighted (highlighted paragraph)
This is a custom block.

#### Editable variables

- $text-font
- $text-font-weight: false by default

#### Editable variables for Modifiers

- $text-color


### block-image

Styles the default wordpress block.

#### Editable variables

- $caption-font
- $caption-font-weight: false by default
- $img-border-radius: false by default

#### Editable variables for Modifiers

- $caption-color


### block-quote

Styles the default wordpress block.

#### Editable variables

- $quote-font
- $quote-font-style
- $cite-font
- $cite-font-style
- $quote-font-weight: false by default
- $cite-font-weight: false by default

#### Editable variables for Modifiers

- $quote-color
- $cite-color
- $border-color
- $border-width


### block-separator

Styles the default wordpress block.

#### Editable variables

It doesn't have default editable variables

#### Editable variables for Modifiers

- $separator-width
- $separator-color


### block-table

Styles the default wordpress block.

#### Editable variables

- $first-row-font
- $other-rows-font
- $caption-font
- $first-row-font-weight: false by default
- $other-rows-font-weight: false by default
- $caption-font-weight: false by default

#### Editable variables for Modifiers

- $first-row-border-width
- $first-row-border-color
- $other-rows-border-width
- $other-rows-border-color
- $first-row-background
- $even-rows-background
- $odd-rows-background
- $first-row-text-color
- $other-rows-text-color
- $caption-color


### headings

Styles the default wordpress blocks.

#### Editable variables

- $h2-font
- $h3-font
- $h4-font
- $h5-font
- $h6-font
- $h2-font-weight: false by default
- $h3-font-weight: false by default
- $h4-font-weight: false by default
- $h5-font-weight: false by default
- $h6-font-weight: false by default

#### Editable variables for Modifiers

- $h2-color
- $h3-color
- $h4-color
- $h5-color
- $h6-color


### links

Styles the default wordpress block.
With the links mixin, you can choose an existing class for the link.
With the links-modifier mixin, you can add a modifier class to the link, you can add this mixin or not.
* All classes you add here must exist and be included in the entry before the c--content stylesheet

#### Editable variables

- $link-class

#### Editable variables for Modifiers

- $link-class-modifier


### lists

Styles the default wordpress blocks.

#### Editable variables

- $text-font
- $one-number-width
- $first-level-dot-width
- $first-level-dot-top
- $second-level-dot-width: false by default
- $second-level-dot-top: false by default
- $third-level-dot-width: false by default
- $third-level-dot-top: false by default
- $text-font-weight: false by default

#### Editable variables for Modifiers

- $text-color
- $number-color
- $first-level-dot-image: false by default
- $first-level-dot-background: false by default
- $first-level-dot-border-width: false by default
- $first-level-dot-border-color: false by default
- $second-level-dot-image: false by default
- $second-level-dot-background: false by default
- $second-level-dot-border-width: false by default
- $second-level-dot-border-color: false by default
- $third-level-dot-image: false by default
- $third-level-dot-background: false by default
- $third-level-dot-border-width: false by default
- $third-level-dot-border-color: false by default


### paragraphs

Styles the default wordpress block.

#### Editable variables

- $text-font
- $text-font-weight: false by default

#### Editable variables for Modifiers

- $text-color


### utilities

Here are the classes Wordpress uses to align blocks left/right/center