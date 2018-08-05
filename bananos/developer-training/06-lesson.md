# Lesson Six, loading data from JSON

Read up about json in the javascript reference on the main developer training page.

6.1) On your gh-pages site add a new file called index.json with the following contents.
```
[
	{
		"id": 1,
		"name": "Alpha"
	},
	{
		"id": 2,
		"name": "Beta"
	}
]
```

6.2) On your gh-pages site in index.html, inside the script, modify the onLoad function to load the json.
```
<!DOCTYPE html>
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
