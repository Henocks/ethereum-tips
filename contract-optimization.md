# Smart Contract Optimization Tips

### GAS Fee
  - Transaction fee for ethereum blockchain network
  - Must pay for transaction confirmation
  - On Smart Contract, heavier contract needs more GAS Fee

### RLP
  - Smart Contract uses RLP : Recursive Length Prefix for data storing
  - On ethereum block, they store 256-bytes at once
  - Every single variable we declare eats 256-byte storage, even if it's <code>bool</code>
  - single (256-byte) storage needs significant amount of 20000 GAS

### Storage & Variable Optimization
  - We have to use <code>Struct</code> to solve this problem

Ethereum & solidity works *pretty well*, even on test network

> Ethereum : Really Attractive
>
> :D
>
> :>
>
> :o

### Tech

Dillinger uses a number of open source projects to work properly:

* [AngularJS] - HTML enhanced for web apps!
* [Ace Editor] - awesome web-based text editor
* [markdown-it] - Markdown parser done right. Fast and easy to extend.
* [Twitter Bootstrap] - great UI boilerplate for modern web apps
* [node.js] - evented I/O for the backend
* [Express] - fast node.js network app framework [@tjholowaychuk]
* [Gulp] - the streaming build system
* [Breakdance](http://breakdance.io) - HTML to Markdown converter
* [jQuery] - duh


```sh
$ cd dillinger
$ npm install -d
$ node app
```

For production environments...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Plugins

Dillinger is currently extended with the following plugins. Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| Github | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |
