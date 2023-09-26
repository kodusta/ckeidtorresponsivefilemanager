# CKEditor Integration with Bootstrap

This guide demonstrates how to integrate CKEditor into a Bootstrap-based HTML form. CKEditor is a powerful WYSIWYG editor for web applications.

## Getting Started

To integrate CKEditor into your web page, follow these steps:

1. Include the required CSS and JavaScript libraries for Bootstrap and CKEditor in the `<head>` section of your HTML file.

```html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>
<script src="ckeditor/ckeditor.js"></script>
```

Create an HTML form with a container to hold the CKEditor instance.

```html
<div class="container">
  <h2>Vertical (basic) form</h2>
  <form action="/action_page.php">
    <div class="form-group">
      <label for="pwd">Password2:</label>
      <!-- CKEditor container -->
      <div id="editor"></div>
    </div>
  </form>
</div>
```

Initialize CKEditor in your JavaScript code by targeting the editor container and configuring the file browser URLs if needed.

```html
<script>
  CKEDITOR.replace('editor', {
    filebrowserBrowseUrl: 'filemanager/filemanager/dialog.php?type=2&editor=ckeditor&fldr=',
    filebrowserUploadUrl: 'filemanager/filemanager/dialog.php?type=2&editor=ckeditor&fldr=',
    filebrowserImageBrowseUrl: 'filemanager/filemanager/dialog.php?type=1&editor=ckeditor&fldr='
  });
</script>
```

# Usage

With this integration, you can now use CKEditor within your Bootstrap-based form to provide rich text editing capabilities.

# License

This project is licensed under the MIT License. See the LICENSE file for details.
