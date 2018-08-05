# Lesson Five, tables in index.html

On your gh-pages site in index.html, under your list of links, add a html table.

Read up about tables in the html reference on the main developer training page.

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
    <li><img class="small_image" src="https://i.imgur.com/Remo7td.png" /></li>
  </ol>
  <table>
    <th><td>Id</td><td>Name</td></th>
    <tr><td>1</td><td>Alpha</td></tr>
    <tr><td>2</td><td>Beta</td></tr>
  </table>
  <script>
      function onLoad () {
        document.getElementById('banano').innerHTML = 'Coranos Bananos';
      }
    </script>
</body>
</html>
```
