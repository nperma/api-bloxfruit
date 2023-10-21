# Example

### Randomly

```javascript
const jsonLink =
  "https://raw.githubusercontent.com/nperma/api-bloxfruit/main/scripts/bf-fruit/api.json";

function loadJSON(url, callback) {
  var xhr = new XMLHttpRequest();
  xhr.open("GET", url, true);
  xhr.onreadystatechange = function () {
    if (xhr.readyState == 4 && xhr.status == 200) {
      callback(JSON.parse(xhr.responseText));
    }
  };
  xhr.send();
}

function random(arr) {
  return arr[Math.floor(Math.random() * arr.length)];
}

function populateBuah(data) {
  var buah = random(data);
  /**
   * @property {buah.img};
   * @property {buah.harga};
   * @property {buah.buah};
   **/
  //console.log(buah.buah)
}

loadJSON(jsonLink, populateBuah);
```

### Store

```javascript

```
