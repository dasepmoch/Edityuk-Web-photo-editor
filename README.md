<h1 align="center">Website Photo Editor</h1>
<h3 align="center">Demo https://dasepmoch.github.io/Website-photo-editor/</h3>
<div align="center">
    <img src="https://github.com/dasepmoch/Edityuk-Web-photo-editor/raw/main/Screenshot%202023-09-15%20005849.png" alt="Screenshot" />
</div>

# INTEGRATION

```html

## Vanilla JS

### Basic Usage

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <style>
        html, body, #editor-container {
            width: 100%;
            height: 100%;
        }
    </style>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0 user-scalable=no" />
    <title>Photo Editor By Dasepmoch</title>
    <script src="dist/pixie.umd.js"></script>
</head>
<body>
<div id="editor-container"></div>
<script>
    Pixie.init({
        selector: "#editor-container",
        baseUrl: 'assets',
        image: "assets/images/samples/sample1.jpg",
    });
</script>
</body>
</html>
```

You can customize the content and styling further to suit your needs.
