# Edityuk-Web-photo-editor

# Getting Started

# Integration
Note:
Before integrating pixie, make sure to copy assets folder from the .zip file to your server or anywhere else where the assets can be publicly accessed via a url (s3 bucket for example).
Vanilla JS
The snippet below includes minimal code necessary to get the editor running in a simple web file.

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
A couple of notes about above example:

<script src="dist/pixie.umd.js"></script> loads pixie editor. You can find this file in pixie/dist folder in the .zip downloaded from codecanyon.
<div id="editor-container"></div> is where the editor will be rendered. Pixie will inherit the size of this container, so you might want to give it width and height.
Pixie.init initiates the editor. You will want to use baseUrl to specify where pixie asset files (images and fonts) are publicly accessible, baseUrl accepts either an absolute (https://site.com/assets) url or a relative one (assets).
React JS
Create a local_modules folder and paste pixie folder into it. 
Install pixie locally by using this command from project root: npm install ./local_modules/
Now you can import Pixie module into your app as any other dependency.
The snippet below includes minimal code necessary to get the editor running in a react component.

import React, {useEffect} from "react";
import { Pixie } from "pixie";

export function EditorDemo() {
  useEffect(() => {
    Pixie.init({
      selector: "#container",
      baseUrl: "pixie",
      image: "pixie/images/samples/sample1.jpg",
    }).then((instance) => {
      // editor is fully loaded!
      console.log(instance);
    });
  }, []);
  return <div id="container" />;
}

