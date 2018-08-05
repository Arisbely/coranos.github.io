# Lesson Four, add HTML to your index.html, use CSS

4.1) using atom, in your github pages site, add a file called index.css that contains the following code:

```
.small_image {
  height: 100px;
  width: 100px;
}
```

4.2) in your github pages site, add an ordered list of images. set the image's width and height to be 100 pixels using CSS classes.
```
<!DOCTYPE html>
<html>
<meta charset="utf-8" />
<head>
<title>Banano</title>
<link rel="stylesheet" type="text/css" href="index.css">
</head>
<body onload="onLoad();">
  <div id="banano"></div>
  <ol>
    <li><img class="small_image" src="https://cdn.discordapp.com/attachments/416341951416369153/473520270309720064/kinderschoko.jpg" /></li>
  </ol>
  <script>
      function onLoad () {
        document.getElementById('banano').innerHTML = 'Coranos Bananos';
      }
    </script>
</body>
</html>
```
