## Install MongoDB 4.4 di High Sierra

Langkah ini saya jumpai ketika saya mencoba install baru MongoDB di High Sierra, dimana sudah muncul OS baru dan [MongoDB](https://www.mongodb.org) sudah muncul versi 5.0.2.


* Lakukan **update Homebrew** terlebih dahulu : `$ brew update`
Silahkan lompat ke [sini](#brew-update) jika kalian tidak melakukan perubahan pada Xcode kalian.

Kamu akan menjumpai error seperti di bawah ini, jika kamu sebelumnya baru saja melakukan update/upgrade aplikasi xcode:
```
Error: You have not agreed to the Xcode license. Please resolve this by running:
  sudo xcodebuild -license accept
```
* Lakukan perintah ini `$ sudo xcodebuild -license accept` untuk mendapatkan license Xcode di macbook kalian.


### $ brew update
* Kemudian lakukan **update Homebrew** dengan perintah ini kembali: `$ brew update`
Pesan ini kalian bakal dapatkan, jika system mendeteksi bahawa Homebrew kalian out of date
```
You can upgrade them with brew upgrade
or list them with brew outdated.
```

### $ brew install mongodb
* Lakukan **install MongoDB** dengan perintah ini : `$ brew install mongodb`

Jika di mac kalian mendapatkan pesan seperti yang ada di bawah ini, artinya MacOS kalian sudah jadul, dan repository mongoDB akan menyuguhkan pilihan mongoDB lama yang bisa kalian install sebagai alternatif.

System akan menyarankan aplikasi yang bisa kalian instal di Mac kalian, dengan memberi tanda `✔`pada aplikasi yang di maksud.
```
These similarly named formulae were found:
mongodb/brew/libmongocrypt                               mongodb/brew/mongodb-community@4.2
mongodb/brew/mongocli                                    **mongodb/brew/mongodb-community@4.4 ✔**
mongodb/brew/mongodb-community                           **mongodb/brew/mongodb-database-tools ✔**
mongodb/brew/mongodb-community-shell                     mongodb/brew/mongodb-mongocryptd
mongodb/brew/mongodb-community@3.2                       mongodb/brew/mongodb-mongocryptd@4.2
mongodb/brew/mongodb-community@3.4                       mongodb/brew/mongodb-mongocryptd@4.4
mongodb/brew/mongodb-community@3.6                       mongosh
mongodb/brew/mongodb-community@4.0                       monetdb
```

* Lakutan **install MongoDB** sekali lagi dengan sesuai dengan instruksi system, contoh nya seperti ini :
`$ brew install mongodb/brew/mongodb-community@4.4`

* Lakukan perintah ini jika mongoDB di mac kalian gagal di install/sebelumnya pernah di install:
`$ brew reinstall mongodb-community@4.4`
