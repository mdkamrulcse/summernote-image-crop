# summernote-image-crop-then-insert-to-editor

A plugin for [Summernote](https://github.com/summernote/summernote/) WYSIWYG editor.

Image toolbar with plugin for summernote with image crop/resize and insert to editor

## Dependencies
- [Summernote](https://summernote.org/): Summernote WYSIWYG editor.
- [Bootstrap](http://getbootstrap.com/): `HTML` markup in the code depends on Bootstrap 3's styling.
- [Font Awesome](http://fontawesome.io/): Use some icons for button 


## Installation

### 1. Include `CSS` & `JS` files

Include the following code:
```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.13.0/css/all.css" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/summernote@0.8.18/dist/summernote.min.css">
    <link rel="stylesheet" href="assets/css/image-ext-plugin.css">
```

and

```html
    <script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/summernote@0.8.18/dist/summernote.min.js"></script>
    <script src="assets/js/summernote-ext-image.js"></script>
```

### 2. Customize Summernote options

Basic customization of the options:

```javascript
$(document).ready(function() {
            $('#summernote').summernote({
                height: 300,
                toolbar:[
                    ['font', ['bold', 'underline', 'clear']],
                    ['color', ['color']],
                    ['para', ['ul', 'ol', 'paragraph']],
                    ['table', ['table']],
                    ['insert', ['link', 'imagePlugin', 'video']],
                    ['view', ['fullscreen', 'codeview', 'help']]
                ],
                imagePlugin: {
                    icon: '<i class="note-icon-picture"/>',
                    tooltip: 'Insert Image',
                    insertToBodySelector: 'imagecontainer', // for insert cropped image to body
                    id: 'summernote' // the textarea id
                }
            });
        });
```

## License

This plugin may be freely distributed and is licensed under the MIT license.
