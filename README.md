# cordova-plugin-secure-key-store
Cordova plugin for securely saving keys, passwords or strings on devices.

## Installation

The plugin can be installed via the Cordova command line interface:

```sh
cordova plugin add cordova-plugin-securekeystore
```

or via github

```sh


## Usage

This plugin will add three new methods to window scope, for saving sensitive data, retrieving saved data and for removing data.

- For saving use `cordova.plugins.SecureKeyStore.set` 

```js
cordova.plugins.SecureKeyStore.set(function (res) {
  console.log(res); // res - string securely stored
}, function (error) {
  console.log(error);
}, "key", 'string to encrypt');
```

- For retrieving use `cordova.plugins.SecureKeyStore.get`.

```js
cordova.plugins.SecureKeyStore.get(function (res) {
  console.log(res); // res - string retrieved
}, function (error) {
  console.log(error);
}, "key");
```
- And for removing `cordova.plugins.SecureKeyStore.remove`

```js
cordova.plugins.SecureKeyStore.remove(function (res) {
  console.log(res); // res - string removed
}, function (error) {
  console.log(error);
}, "key");
```
