## Install MongoDB on macOS Sierra

This procedure explains how to install [MongoDB](https://www.mongodb.org) using [Homebrew](http://brew.sh) on macOS Sierra 10.12.
Official MongoDB install documentation: [here](https://docs.mongodb.org/manual/tutorial/install-mongodb-on-os-x/)



### Install Homebrew
* Installing Homebrew is effortless, open Terminal and enter :
 `$  /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
* **Note:** Homebrew will download and install Command Line Tools for Xcode 8.0 as part of the installation process.



### Install MongoDB
At this time of writing, Homebrew has MongoDB version **3.2.10** as default formulae in its main repository :

* Enter the following command : `$ brew info mongodb`
* Expected output: **mongodb: stable 3.2.10 (bottled)**

To install MongoDB enter : `$ brew install mongodb`


## Additional configuration
### Homebrew
To load and start the MongoDB background service, open Terminal and execute the following commands :

* Install **brew services** first : `$ brew tap homebrew/services`
* Load and start the MongoDB service : `$ brew services start mongodb`.
Expected output : **Successfully started `mongodb` (label: homebrew.mxcl.mongodb)**

* Check of the MongoDB service has been loaded : `$ brew services list` <sup>[1](#1)</sup>

* Verify the installed MongoDB instance : `$ mongod --version`.
Expected output : **db version v3.2.10**


#### Comments
<a name="1"><sup>1</sup></a> The `brew services start mongodb` - instruction is equal to :

```
ln -sfv /usr/local/opt/mongodb/*.plist ~/Library/LaunchAgents
launchctl load ~/Library/LaunchAgents/homebrew.mxcl.mongodb.plist
```
