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
```javascript
<!DOCTYPE html>
<body onload="onLoad();">
  <div id="banano"></div>
  <script>
      const loadJson = () => {
        const xhttp = new XMLHttpRequest();
        xhttp.onreadystatechange = function () {
          if (this.readyState == 4 && this.status == 200) {
            loadJsonCallback(this.response);
          }
        }
        xhttp.responseType = 'json';
        xhttp.open('GET', 'index.json', true);
        xhttp.send();
      }

      const loadJsonCallback = (json) => {
        const banano = document.getElementById('banano');
        
        const header = document.createTextNode('Coranos Bananos');
        
        banano.appendChild(header);

        const table = document.createElement('table');      
        banano.appendChild(table);
        
        const tableHeaderRow = document.createElement('tr');
        table.appendChild(tableHeaderRow);

        if(json.length == 0) {
          return;
        }
        
        for (const [key, value] of Object.entries(json[0])) {
          const tableHeaderElt = document.createElement('th');
          tableHeaderRow.appendChild(tableHeaderElt);
          tableHeaderElt.appendChild(document.createTextNode(key));
        }
        
        json.forEach((jsonElt,jsonEltIx) => {
          const tableDataRow = document.createElement('tr');
          table.appendChild(tableDataRow);

          for (const [key, value] of Object.entries(jsonElt)) {
            const tableDataElt = document.createElement('td');
            tableDataRow.appendChild(tableDataElt);
            tableDataElt.appendChild(document.createTextNode(value));
          }
        });
      }

      const onLoad = () => {
        loadJson();
      }
    </script>
</body>
</html>
```
