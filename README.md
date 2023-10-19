# api-bloxfruit
BloxFruit API

```javascript
const jsonLink = "https://bloxfruit-api.soappanel.repl.co";

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

function displayBuahInfo(buah) {
  console.log("Fruit Name: " + buah.buah);
  console.log("Fruit Image: " + buah.img);
  console.log("Fruit Price: " + buah.harga);
}

loadJSON(jsonLink, function (data) {
  var buah = random(data);
  displayBuahInfo(buah);
});
```

### Fruit
[ApiLink](https://bloxfruit-api.soappanel.repl.co)
