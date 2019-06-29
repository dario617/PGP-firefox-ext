# PGP-firefox-ext

A firefox extension for sending private messages through a public forum using PGP.

## Acknowledgments

This was only possible by the kind opensource projects listed bellow:
* OpenPGP.js for providing the encryption logic and a helpfull documentation [repo](https://github.com/openpgpjs/openpgpjs).
* React-extension-boilerplate for providing an out of the box configuration for extension developpement [repo](https://github.com/kryptokinght/react-extension-boilerplate).

## Current features

* Manage a list of contacts with public keys.
* Create a private/public key pair on the browser.

## Future work

* Improve security of storage of private keys.
* Add support for importing keys.
* Improve contact management.
* Improve UI using any react module.
* Add support for ES6 syntax on webpack configuration.

## Current installation instructions

Go to the extension root folder and install the node dependencies.
```shell
$ npm install
```
To run you can follow the inherited documentation on the root folder or simply compile using:
```shell
$ npm run build
```
Finally to add this development version to the browser refer to [MDN web docs](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/Temporary_Installation_in_Firefox)

## Folder structure
* root
..* extension: build
..* react-extension: code and dev utils

## Use instructions
1. Go to options on addons and create your pairs
2. Add contacts on the options menu. IMPORTANT NOTE: It is important to write the public key following the standard format. Otherwise the code will not be able to parse the key and thus no decryption/encryption completed.
3. Go to any website and post a public (private) message selecting a contact and writing your passphrase by using the popup menu. 

## Trouble shooting
* If it doesn't compile on your unix system change the "windows" value to "unix" on line 39 of react-extension/.eslintrc.js