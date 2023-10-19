# api-bloxfruit
BloxFruit API

```javascript
const jsonLink =
        "https://raw.githubusercontent.com/nperma/api-bloxfruit/main/bloxfruitAPI.json";
    
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

      /**
      * @property {buah} fruit
      * @property {img} image
      * @property {harga} price
      */

      function populateBuah(data) {
        var buah = random(data);
        console.log(buah.buah) //fruitname
        console.log(buah.img) //image url
        console.log(buah.harga) //price
      }

      loadJSON(jsonLink, populateBuah);
```

### Fruit
[ApiLink](https://raw.githubusercontent.com/nperma/api-bloxfruit/main/bloxfruitAPI.json)
