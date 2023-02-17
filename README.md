# wysiwyg-content

## Stylized blocks
- btn
- footnote
- highlited paragraph


## Use
Install package
```sh
npm i @teamthunderfoot/wysiwyg-content
```

Import content mixins at the beginning of the c--content stylesheet
```sh
@import "@teamthunderfoot/wysiwyg-content/src/scss/_mixins.scss";
```

```sh
.c--content-a {
    @include block-btn(
        $btn-class: g--btn-01
    );
    @include block-btn-modifier(
        $btn-class-modifier: g--btn-01--second
    );
    @include block-footnote(
        $text-font: e,
        $text-font-weight: 300,
    );
    @include block-footnote-modifier(
        $text-color: map-get($color-options, a)
    );
    @include block-highlighted(
        $text-font: c,
        // $text-font-weight: false,
    );
    @include block-highlighted-modifier(
        $text-color: map-get($color-options, a)
    );
    @include block-image(
        $caption-font: g,
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
        // $quote-font-weight: false,
        // $cite-font-weight: false,
    );
    @include block-quote-modifier(
        $quote-color: map-get($color-options, a), //* quote color
        $cite-color: map-get($color-options, a), //* cite color
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
        $first-row-font-weight: 500,
        // $other-rows-font-weight: false,
        // $caption-font-weight: false,
    );
    @include block-table-modifier(
        $first-row-border-width: 1px, //* first row border
        $first-row-border-color: map-get($color-options, a), //* first row border
        $other-rows-border-width: 1px, //* other rows border
        $other-rows-border-color: transparent, //* other rows border
        $first-row-background: map-get($color-options, a), //* first row background
        $even-rows-background: map-get($color-options, d), //* even rows background
        $odd-rows-background: map-get($color-options, b), //* odd rows background (except the first one)
        $first-row-text-color: map-get($color-options, d), //* first row text color
        $other-rows-text-color: map-get($color-options, a), //* other rows text color
        $caption-color: map-get($color-options, a) //* caption text color
    );
    @include headings(
        $h2-font: b,
        $h3-font: c,
        $h4-font: c,
        $h5-font: d,
        $h6-font: d,
        // $h2-font-weight: false,
        $h3-font-weight: 500,
        // $h4-font-weight: false,
        $h5-font-weight: 500,
        // $h6-font-weight: false,
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
        // $second-level-dot-width:false,
        // $second-level-dot-top:false,
        $third-level-dot-width: 6px,
        // $third-level-dot-top:false,
        // $text-font-weight: false,
    );
    @include lists-modifier(
        $text-color: map-get($color-options, a),
        $number-color: map-get($color-options, f),
        // $first-level-dot-image: 'https://picsum.photos/20',
        $first-level-dot-background: map-get($color-options, f),
        // $first-level-dot-border-width: false,
        // $first-level-dot-border-color: false,
        // $second-level-dot-image: false,
        // $second-level-dot-background: false,
        $second-level-dot-border-width: 2px,
        $second-level-dot-border-color: map-get($color-options, f),
        // $third-level-dot-image: false,
        // $third-level-dot-background: false,
        $third-level-dot-border-width: 1px,
        $third-level-dot-border-color: map-get($color-options, g),
    );
    @include paragraphs(
        $text-font: d,
        // $text-font-weight: false,
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