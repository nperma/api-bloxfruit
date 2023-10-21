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
const jsonLink = "https://raw.githubusercontent.com/nperma/api-bloxfruit/main/scripts/bf-fruit/api.json";

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

function findFruitByName(data, fruitName) {
  const fruit = data.find(item => item.buah.toLowerCase() === fruitName.toLowerCase());
  if (fruit) {
    console.log("Name Fruit:", fruit.buah);
    console.log("Price:", fruit.harga);
    console.log("Image:", fruit.img);
  } else {
    console.log("Fruit Undefined");
  }
}

const fruitName = "KIlo";
loadJSON(jsonLink, (data) => findFruitByName(data, fruitName));
```
