# api-bloxfruit
BloxFruit API

```javascript
const jsonLink =
        "https://raw.githubusercontent.com/nperma/api-bloxfruit/main/bloxfruit/bloxfruitAPI.json";
    
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
        document.getElementById("buah-img").src = buah.img;
        document.getElementById("harga").textContent = buah.harga;
        document.title = "Buah - " + buah.buah;
      }

      loadJSON(jsonLink, populateBuah);
```

### Fruit
[ApiLink](https://raw.githubusercontent.com/nperma/api-bloxfruit/main/bloxfruit/bloxfruitAPI.json)
