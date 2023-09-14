<h1 align="center">Hi 👋, I'm Dasep Moch Luay</h1>
<h3 align="center">A passionate Web developer from Indonesia</h3>
<div align="center">
    <img src="https://github.com/dasepmoch/Edityuk-Web-photo-editor/raw/main/Screenshot%202023-09-15%20005849.png" alt="Screenshot" />
</div>

# INTEGRATION

```html
# Pixie Image Editor

Pixie is a powerful image editor that can be easily integrated into your web projects. With Pixie, you can provide image editing capabilities to your users quickly and easily. This is a brief guide on how to get started with Pixie in various development environments.

## Vanilla JS

### Basic Usage

Below is the minimal HTML code required to run Pixie in a simple web file:

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
    <title>Pixie Example</title>
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

A few notes about the above example:
- `<script src="dist/pixie.umd.js"></script>` loads the Pixie editor. You can find this file in the `pixie/dist` folder in the `.zip` downloaded from codecanyon.
- `<div id="editor-container"></div>` is where the editor will be rendered. Pixie will inherit the size of this container, so you might want to give it width and height.
- `Pixie.init` initializes the editor. You will want to use `baseUrl` to specify where Pixie asset files (images and fonts) are publicly accessible. `baseUrl` accepts either an absolute (https://site.com/assets) URL or a relative one (assets).
```

You can customize the content and styling further to suit your needs.
