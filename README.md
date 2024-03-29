# wysiwyg-content

## Stylized blocks

- [block-btn](#block-btn)
- [block-columns](#block-columns)
- [block-footnote](#block-footnote)
- [block-highlighted](#block-highlighted-highlighted-paragraph) (highlighted paragraph)
- [block-image](#block-image)
- [block-quote](#block-quote)
- [block-separator](#block-separator)
- [block-table](#block-table)
- [block-video](#block-video)
- [headings](#headings)
- [links](#links)
- [lists](#lists)
- [paragraphs](#paragraphs)
- [utilities](#utilities)

## Blocks

All blocks except utilities have 2 mixins, one for styles and the other one for colors and modifiers.

### block-btn

Styles the default wordpress block.
With the block-btn mixin, you can choose an existing class for the btn.
With the block-btn-modifier mixin, you can add a modifier class to the btn, you can add this mixin or not.
> Note: All classes you add here must exist and be included in the entry before the c--content stylesheet

#### Editable variables

- $btn-class
- $btn-class-modifier
- $btn-margin-bottom

#### Editable variables for Modifiers

- $btn-class-modifier

```scss
    @include block-btn(
        $btn-class: g--btn-01,
        // $btn-margin-bottom: $measure*4
    );
    // @include block-btn-modifier(
    //     $btn-class-modifier: g--btn-01--second
    // );
```

### block-columns

Styles the default wordpress block.
With the block-columns mixin, you set the margin-bottom for columns, make all components inside them the same height and make the columns breakpoint tablets.

#### Editable variables

- $columns-margin-bottom

```scss
    @include block-columns(
        // $columns-margin-bottom: $measure*4
    );
```


### block-footnote

This is a custom block.

#### Editable variables

- $footnote-margin-bottom
- $text-font
- $text-font-weight: false by default
- $text-color

#### Editable variables for Modifiers

- $text-color

```scss
    @include block-footnote(
        $text-font: e,
        // $footnote-margin-bottom: $measure * 2,
        // $text-font-weight: default,
    );
    @include block-footnote-modifier(
        $text-color: map-get($color-options, a)
    );
```


### block-highlighted (highlighted paragraph)
This is a custom block.

#### Editable variables

- $highlighted-margin-bottom
- $highlighted-padding-top
- $text-font
- $text-font-weight: false by default
- $text-color

#### Editable variables for Modifiers

- $text-color

```scss
    @include block-highlighted(
        $text-font: c,
        // $highlighted-margin-bottom: $measure * 4,
        // $highlighted-padding-top: 0,
        // $text-font-weight: false,
    );
    @include block-highlighted-modifier(
        $text-color: map-get($color-options, a)
    );
```


### block-image

Styles the default wordpress block.

#### Editable variables

- $caption-align: right,
- $caption-font
- $caption-font-weight
- $caption-margin-top
- $image-block-margin-bottom
- $image-text-aligned-margin-x
- $img-border-radius
- $caption-color

#### Editable variables for Modifiers

- $caption-color

```scss
    @include block-image(
        $caption-align: right,
        $caption-font: g,
        // $image-block-margin-bottom: $measure*5,
        // $image-text-aligned-margin-x: $measure*5,
        // $caption-margin-top: $measure*2,
        // $caption-font-weight: false,
        // $img-border-radius: false
    );
    @include block-image-modifier(
        $caption-color: map-get($color-options, a)
    );
```


### block-quote

Styles the default wordpress block.

#### Editable variables

- $quote-font
- $quote-font-style
- $cite-font
- $cite-font-style
- $quote-font-weight
- $cite-font-weight
- $quote-color
- $quote-padding
- $quote-margin-top
- $quote-margin-bottom
- $cite-margin-top
- $cite-color
- $border-color
- $border-width

#### Editable variables for Modifiers

- $quote-color
- $cite-color
- $border-color
- $border-width

```scss
    @include block-quote(
        $quote-font: d,
        $quote-font-style: italic,
        $cite-font: e,
        $cite-font-style: normal,
        // $quote-padding: $measure * 3 0,
        // $quote-margin-top: $measure*5,
        // $quote-margin-bottom: $measure*6,
        // $cite-margin-top: $measure*3,
        // $quote-font-weight: false,
        // $cite-font-weight: false,
    );
    @include block-quote-modifier(
        $quote-color: map-get($color-options, a),
        $cite-color: map-get($color-options, a),
        $border-color: map-get($color-options, e),
        $border-width: 1px,
    );
```


### block-separator

Styles the default wordpress block.

#### Editable variables

- $separator-margin
- $separator-width
- $separator-color

#### Editable variables for Modifiers

- $separator-width
- $separator-color

```scss
    @include block-separator(
        // $separator-margin: $measure * 6 0
    );
    @include block-separator-modifier(
        $separator-width: 1px,
        $separator-color: map-get($color-options, e),
    );
```


### block-table

Styles the default wordpress block.

![alt text][table]

[table]: https://raw.githubusercontent.com/team-thunderfoot/wysiwyg-content/main/src/img/table.png

#### Editable variables

- $header-font
- $body-rows-font
- $caption-font
- $table-margin-bottom
- $header-cells-padding
- $body-cells-padding
- $caption-margin-top
- $header-font-weight
- $body-rows-font-weight
- $caption-align: right,
- $caption-font-weight
- $header-border-width
- $header-border-color
- $body-rows-border-width
- $body-rows-border-color
- $header-background
- $even-rows-background
- $odd-rows-background
- $header-text-color
- $body-rows-text-color
- $caption-color

#### Editable variables for Modifiers

- $header-border-width
- $header-border-color
- $body-rows-border-width
- $body-rows-border-color
- $header-background
- $even-rows-background
- $odd-rows-background
- $header-text-color
- $body-rows-text-color
- $caption-color

```scss
    @include block-table(
        $header-font: d,
        $body-rows-font: d,
        $caption-align: right,
        $caption-font: f,
        // $table-margin-bottom: $measure*4,
        // $header-cells-padding: $measure*2,
        // $body-cells-padding: $measure $measure * 2,
        // $caption-margin-top: $measure * 2,
        // $header-font-weight: false,
        // $body-rows-font-weight: false,
        // $caption-font-weight: false,
    );
    @include block-table-modifier(
        $header-border-width: 1px,
        $header-border-color: map-get($color-options, a),
        $body-rows-border-width: 1px,
        $body-rows-border-color: transparent,
        $header-background: map-get($color-options, a),
        $even-rows-background: map-get($color-options, d),
        $odd-rows-background: map-get($color-options, b),
        $header-text-color: map-get($color-options, d),
        $body-rows-text-color: map-get($color-options, a),
        $caption-color: map-get($color-options, a)
    );
```


### block-video

Styles the default wordpress block.
With the block-video mixin, you set the aspect-ratio for the video iframes.

#### Editable variables

- $video-block-margin-bottom

```scss
    @include block-video(
        // $video-block-margin-bottom: $measure*5,
    );
```


### headings

Styles the default wordpress blocks.

#### Editable variables

- $h2-font
- $h3-font
- $h4-font
- $h5-font
- $h6-font
- $h2-padding-top
- $h2-margin-bottom
- $h3-padding-top
- $h3-margin-bottom
- $h4-padding-top
- $h4-margin-bottom
- $h5-padding-top
- $h5-margin-bottom
- $h6-padding-top
- $h6-margin-bottom
- $h2-font-weight
- $h2-font-weight-bold
- $h3-font-weight
- $h3-font-weight-bold
- $h4-font-weight
- $h4-font-weight-bold
- $h5-font-weight
- $h5-font-weight-bold
- $h6-font-weight
- $h6-font-weight-bold
- $h2-color
- $h3-color
- $h4-color
- $h5-color
- $h6-color

#### Editable variables for Modifiers

- $h2-color
- $h3-color
- $h4-color
- $h5-color
- $h6-color

```scss
    @include headings(
        $h2-font: b,
        $h3-font: c,
        $h4-font: c,
        $h5-font: d,
        $h6-font: d,
        // $h2-padding-top: $measure*5,
        // $h2-margin-bottom: $measure*3,
        // $h3-padding-top: $measure*5,
        // $h3-margin-bottom: $measure*3,
        // $h4-padding-top: $measure*5,
        // $h4-margin-bottom: $measure*2,
        // $h5-padding-top: $measure*5,
        // $h5-margin-bottom: $measure*2,
        // $h6-padding-top: $measure*5,
        // $h6-margin-bottom: $measure,
        // $h2-font-weight: false,
        // $h2-font-weight-bold: false,
        // $h3-font-weight: false,
        // $h3-font-weight-bold: false,
        // $h4-font-weight: false,
        // $h4-font-weight-bold: false,
        // $h5-font-weight: false,
        // $h5-font-weight-bold: false,
        // $h6-font-weight: false,
        // $h6-font-weight-bold: false,
    );
    @include headings-modifier(
        $h2-color: map-get($color-options, a),
        $h3-color: map-get($color-options, e),
        $h4-color: map-get($color-options, f),
        $h5-color: map-get($color-options, a),
        $h6-color: map-get($color-options, a),
    );
```


### links

Styles the default wordpress block.
With the links mixin, you can choose an existing class for the link.
With the links-modifier mixin, you can add a modifier class to the link, you can add this mixin or not.
> Note: All classes you add here must exist and be included in the entry before the c--content stylesheet

#### Editable variables

- $link-class
- $link-class-modifier

#### Editable variables for Modifiers

- $link-class-modifier

```scss
    @include links(
        $link-class: g--link-01
    );
    // @include links-modifier(
    //     $link-class-modifier: g--link-01--second
    // );
```


### lists

Styles the default wordpress blocks.
Unordered list artworks can be circles, squares or images, it depends on the variables we add ($X-artwork-X). If they're circles or squares they can be filled or just bordered.
> Note: Variables named $second-level-artwork-X or $third-level-artwork-X should only be added in case we want a different value for them than for the other levels.

![alt text][ul-lists]

[ul-lists]: https://raw.githubusercontent.com/team-thunderfoot/wysiwyg-content/main/src/img/ul-lists.png

![alt text][ol-lists]

[ol-lists]: https://raw.githubusercontent.com/team-thunderfoot/wysiwyg-content/main/src/img/ol-lists.png

#### Editable variables

- $text-font
- $first-number-width
- $first-level-artwork-width
- $first-level-artwork-top
- $lists-margin-bottom
- $lists-items-margin-bottom
- $second-level-artwork-width
- $second-level-artwork-top
- $third-level-artwork-width
- $third-level-artwork-top
- $text-font-weight
- $text-color
- $number-color
- $first-level-artwork-image
- $first-level-artwork-border-radius
- $first-level-artwork-background
- $first-level-artwork-border-width
- $first-level-artwork-border-color
- $second-level-artwork-image
- $second-level-artwork-border-radius
- $second-level-artwork-background
- $second-level-artwork-border-width
- $second-level-artwork-border-color
- $third-level-artwork-image
- $third-level-artwork-border-radius
- $third-level-artwork-background
- $third-level-artwork-border-width
- $third-level-artwork-border-color

#### Editable variables for Modifiers

- $text-color
- $number-color
- $first-level-artwork-image
- $first-level-artwork-border-radius
- $first-level-artwork-background
- $first-level-artwork-border-width
- $first-level-artwork-border-color
- $second-level-artwork-image
- $second-level-artwork-border-radius
- $second-level-artwork-background
- $second-level-artwork-border-width
- $second-level-artwork-border-color
- $third-level-artwork-image
- $third-level-artwork-border-radius
- $third-level-artwork-background
- $third-level-artwork-border-width
- $third-level-artwork-border-color

```scss
    @include lists(
        $text-font: d,
        $first-number-width: 22px,
        $first-level-artwork-width: $measure,
        $first-level-artwork-top: 13px,
        // $lists-margin-bottom: $measure * 4,
        // $lists-items-margin-bottom: $measure * 2,
        // $second-level-artwork-width: false,
        // $second-level-artwork-top: false,
        // $third-level-artwork-width: false,
        // $third-level-artwork-top:false,
        // $text-font-weight: false,
    );
    @include lists-modifier(
        $text-color: map-get($color-options, a),
        $number-color: map-get($color-options, f),
        // $first-level-artwork-image: false,
        // $first-level-artwork-border-radius: false,
        // $first-level-artwork-background: false,
        // $first-level-artwork-border-width: false,
        // $first-level-artwork-border-color: false,
        // $second-level-artwork-image: false,
        // $second-level-artwork-border-radius: false,
        // $second-level-artwork-background: false,
        // $second-level-artwork-border-width: false,
        // $second-level-artwork-border-color: false,
        // $third-level-artwork-image: false,
        // $third-level-artwork-border-radius: false,
        // $third-level-artwork-background: false,
        // $third-level-artwork-border-width: false,
        // $third-level-artwork-border-color: false,
    );
```

> #### Variables needed for circles:
> 
> - $first-level-artwork-width
> - $first-level-artwork-top
> - $first-level-artwork-border-radius
> - $first-level-artwork-background (if its filled)
> - $first-level-artwork-border-width and $first-level-artwork-border-color (if its bordered)

> #### Variables needed for squares:
> 
> - $first-level-artwork-width
> - $first-level-artwork-top
> - $first-level-artwork-background (if its filled)
> - $first-level-artwork-border-width and $first-level-artwork-border-color (if its bordered)

> #### Variables needed for images:
> 
> - $first-level-artwork-width
> - $first-level-artwork-top
> - $first-level-artwork-image


### paragraphs

Styles the default wordpress block.

#### Editable variables

- $bold-font-weight
- $text-font
- $paragraphs-margin-bottom
- $paragraphs-before-lists-margin-bottom
- $text-font-weight
- $text-color

#### Editable variables for Modifiers

- $text-color

```scss
    @include paragraphs(
        $bold-font-weight: 600,
        $text-font: d,
        // $paragraphs-margin-bottom: $measure * 4,
        // $paragraphs-before-lists-margin-bottom: $measure * 3,
        // $text-font-weight: false,
    );
    @include paragraphs-modifier(
        $text-color: map-get($color-options, a)
    );
```


### utilities

Here are the classes Wordpress uses to align blocks left/right/center

#### Editable variables

- $media-text-aligned-margin-x

```scss
    @include utilities(
        // $media-text-aligned-margin-x: $measure*5
    );
```

## Use

Install package
```sh
npm i @teamthunderfoot/wysiwyg-content
```

Import content mixins at the beginning of the c--content stylesheet
```scss
@import "@teamthunderfoot/wysiwyg-content/src/scss/_mixins.scss";
```

Your HTML structure should look like this

```php
<div class="c--content-a">
  <?= apply_filters('the_content',get_the_content()) ?>
</div>
```

Copy c--content styles and change parameters with the ones we want
```scss
    .c--content-a {
        @include block-btn(
            $btn-class: g--btn-01,
            // $btn-margin-bottom: $measure*4
        );
        // @include block-btn-modifier(
        //     $btn-class-modifier: g--btn-01--second
        // );

        @include block-columns(
            // $columns-margin-bottom: $measure*4
        );

        @include block-footnote(
            $text-font: e,
            // $footnote-margin-bottom: $measure * 2,
            // $text-font-weight: default,
        );
        @include block-footnote-modifier(
            $text-color: map-get($color-options, a)
        );

        @include block-highlighted(
            $text-font: c,
            // $highlighted-margin-bottom: $measure * 4,
            // $highlighted-padding-top: 0,
            // $text-font-weight: false,
        );
        @include block-highlighted-modifier(
            $text-color: map-get($color-options, a)
        );

        @include block-image(
            $caption-align: right,
            $caption-font: g,
            // $image-block-margin-bottom: $measure*5,
            // $image-text-aligned-margin-x: $measure*5,
            // $caption-margin-top: $measure*2,
            // $caption-font-weight: false,
            // $img-border-radius: false
        );
        @include block-image-modifier(
            $caption-color: map-get($color-options, a)
        );

        @include block-quote(
            $quote-font: d,
            $quote-font-style: italic,
            $cite-font: e,
            $cite-font-style: normal,
            // $quote-padding: $measure * 3 0,
            // $quote-margin-top: $measure*5,
            // $quote-margin-bottom: $measure*6,
            // $cite-margin-top: $measure*3,
            // $quote-font-weight: false,
            // $cite-font-weight: false,
        );
        @include block-quote-modifier(
            $quote-color: map-get($color-options, a),
            $cite-color: map-get($color-options, a),
            $border-color: map-get($color-options, e),
            $border-width: 1px,
        );

        @include block-separator(
            // $separator-margin: $measure * 6 0
        );
        @include block-separator-modifier(
            $separator-width: 1px,
            $separator-color: map-get($color-options, e),
        );

        @include block-table(
            $header-font: d,
            $body-rows-font: d,
            $caption-align: right,
            $caption-font: f,
            // $table-margin-bottom: $measure*4,
            // $header-cells-padding: $measure*2,
            // $body-cells-padding: $measure $measure * 2,
            // $caption-margin-top: $measure * 2,
            // $header-font-weight: false,
            // $body-rows-font-weight: false,
            // $caption-font-weight: false,
        );
        @include block-table-modifier(
            $header-border-width: 1px,
            $header-border-color: map-get($color-options, a),
            $body-rows-border-width: 1px,
            $body-rows-border-color: transparent,
            $header-background: map-get($color-options, a),
            $even-rows-background: map-get($color-options, d),
            $odd-rows-background: map-get($color-options, b),
            $header-text-color: map-get($color-options, d),
            $body-rows-text-color: map-get($color-options, a),
            $caption-color: map-get($color-options, a)
        );

        @include block-video(
            // $video-block-margin-bottom: $measure*5,
        );

        @include headings(
            $h2-font: b,
            $h3-font: c,
            $h4-font: c,
            $h5-font: d,
            $h6-font: d,
            // $h2-padding-top: $measure*5,
            // $h2-margin-bottom: $measure*3,
            // $h3-padding-top: $measure*5,
            // $h3-margin-bottom: $measure*3,
            // $h4-padding-top: $measure*5,
            // $h4-margin-bottom: $measure*2,
            // $h5-padding-top: $measure*5,
            // $h5-margin-bottom: $measure*2,
            // $h6-padding-top: $measure*5,
            // $h6-margin-bottom: $measure,
            // $h2-font-weight: false,
            // $h2-font-weight-bold: false,
            // $h3-font-weight: false,
            // $h3-font-weight-bold: false,
            // $h4-font-weight: false,
            // $h4-font-weight-bold: false,
            // $h5-font-weight: false,
            // $h5-font-weight-bold: false,
            // $h6-font-weight: false,
            // $h6-font-weight-bold: false,
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
            $first-number-width: 22px,
            $first-level-artwork-width: $measure,
            $first-level-artwork-top: 13px,
            // $lists-margin-bottom: $measure * 4,
            // $lists-items-margin-bottom: $measure * 2,
            // $second-level-artwork-width: false,
            // $second-level-artwork-top: false,
            // $third-level-artwork-width: false,
            // $third-level-artwork-top:false,
            // $text-font-weight: false,
        );
        @include lists-modifier(
            $text-color: map-get($color-options, a),
            $number-color: map-get($color-options, f),
            // $first-level-artwork-image: false,
            // $first-level-artwork-border-radius: false,
            // $first-level-artwork-background: false,
            // $first-level-artwork-border-width: false,
            // $first-level-artwork-border-color: false,
            // $second-level-artwork-image: false,
            // $second-level-artwork-border-radius: false,
            // $second-level-artwork-background: false,
            // $second-level-artwork-border-width: false,
            // $second-level-artwork-border-color: false,
            // $third-level-artwork-image: false,
            // $third-level-artwork-border-radius: false,
            // $third-level-artwork-background: false,
            // $third-level-artwork-border-width: false,
            // $third-level-artwork-border-color: false,
        );

        @include paragraphs(
            $bold-font-weight: 600,
            $text-font: d,
            // $paragraphs-margin-bottom: $measure * 4,
            // $paragraphs-before-lists-margin-bottom: $measure * 3,
            // $text-font-weight: false,
        );
        @include paragraphs-modifier(
            $text-color: map-get($color-options, a)
        );

        @include utilities(
            // $media-text-aligned-margin-x: $measure*5
        );
        
        & > h2:first-child,
        & > h3:first-child,
        & > h4:first-child,
        & > h5:first-child,
        & > h6:first-child,
        & > p:first-child  {   
            padding-top: 0;
        }

        *:last-child {
            margin-bottom: 0;
        }
    }
```