# Lesson Three, simple index.html.

3.1) in your github pages site, add an index.html with the following code:
```
    <!DOCTYPE html>
    <html>
    <meta charset="utf-8" />
    <head>
    <title>Banano</title>
    </head>
    <body onload="onLoad();">
      <div id="banano"></div>
      <script>
          function onLoad () {
            document.getElementById('banano').innerHTML = 'Coranos Bananos';
          }
        </script>
    </body>
    </html>
```
3.2) update this page with a link to your Github Pages
```
git pull;git commit -a -m "updated index.html";git push;
```

