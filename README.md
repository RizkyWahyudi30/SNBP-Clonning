# SNBP Clonning

Hi guys, I was inspired by the GitHub of `@anuGrahBodi` for this SNBP Clonning website, so here I want to recreate or copy the website by tidying up the main page to make it neater and more beautiful.

The Tech Stack that I use here is 3, namely: </br>

![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=plastic&logo=css3&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=plastic&logo=html5&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=plastic&logo=javascript&logoColor=%23F7DF1E) ![Bootstrap](https://img.shields.io/badge/bootstrap-%238511FA.svg?style=plastic&logo=bootstrap&logoColor=white)

and also using `cdnjs fontawesome and qrcode`:
- `🔐 font:  <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/js/all.min.js"></script>`
- `🔐 qrcode:  <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>`

# Fitur fitur 

pertama, kalian harus menginstall dulu `Node.js, MySql, XAMPP` di komputer atau laptop kalian
- 🎯 Node.js = (https://nodejs.org/en/download)
- 🎯 MySql = (https://www.mysql.com/downloads/)
- 🎯 XAMPP = (https://www.apachefriends.org/download.html)
  
- Kedua, setelah kalian menginstall ketiga itu, kalian buat folder untuk tempat file ngoding kalian. Setelah membuat itu, kalian buka folder itu di text editor kalian, kalo aku di `vscode`. Setelah di vscode nya, kalian buka `terminal` vscodenya, lalu ketikkan

```bash
npm init -y
```

setelah kalian `npm init -y` di folder kalian muncul file `package.json`. Seetelah itu buat file lagi, namanya `server.js`

- Ketiga, kalau sudah, kalian nyalakan dulu XAMPP nya, setelah dinyalakan kalian ke browser kalian, kalo aku di `Microsoft edge`, lalu ketikkan `localhost/phpmyadmin/`. Setelah itu buat satu database

- Keempat, kembali ke `vscode` lalu ketikka kode seperti ini di file server.js

```bash
const express = require("express");
const mysql = require("mysql");

const app = express();

app.get("/", (req, res) => {
  res.send("OK ROUTE OPEN");
})

app.listen(8000, () => {
  console.log("server ready..")
})

// port 8000 bisa kalian custom semau kalian, tidak harus 8000
```

setelah dibuat lalu, kalian ketikkan di terminal teks editor kalian `$ node server.js`, kalian ke browser kalian tadi, lalu buka tab baru, ketikkan `localhost:8000`

```bash
const express = require("express");
const mysql = require("mysql");

const app = express();

const db = mysql.createConnection({
  host: "localhost",
  database: "(nama db kalian)",
  user: "root",
  password: ""
})

db.connect((err) => {
  if (err) throw err
  console.log("database connected..");
  app.get("/", (req, res) => {
    res.send("OK ROUTE OPEN")
  })
})

app.listen(8000, () => {
  console.log("server ready..")
})
```

lalu kalian jalankan lagi seperti tadi.

- Kelima, kalian install `ejs` nya :

```bash
npm i ejs
```

setelah kalian install `ejs`, kalian perlu install nodemon juga

```bash
npm i -g nodemon
```

setelah itu, kalia bisa ngecek apakah sudah terinstall atau belum nodemon kalian :

```bash
nodemon -v
```

- Ketujuh, Setelah diinstall kalian perlu membuat satu folder lagi dan satu file : `views\index.ejs`

- Kedelapan, untuk styling nya kalian bisa memakai libary css, salah satunya `bootstrap`. Kalian bisa mengekstrak dengan cara

```bash
https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css
```

```bash
https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js
```

Link ini ditaro di file index.ejs

_Setelah ini, kalian bisa melihat tutorialnya di youtube bang Dea : https://youtu.be/JmwDuKzbkNA?si=K7CGAg8oYnBP6RRx_

## Connection

mari kita saling koneksi :)
