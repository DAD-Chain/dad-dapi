<h1 align="center"> DAD dApi </h1>

# dad-dapi

API for dApps on DAD blockchain. This is an implementation of dAPI from [OEP-6](https://github.com/backslash47/OEPs/blob/oep-dapp-api/OEP-6/OEP-6.mediawiki) communication protocol.

It is necessary to have installed suitable **dAPI provider** . Reference implementation is [Cyano Wallet](https://github.com/DAD-Chain/dad-wallet).

The library is written in TypeScript, so all the methods and objects are typed. It is therefore usable in TypeScript projects as well as vanilla JavaScript projects.

## How to use 
dad-dapi can be used as CommonJS/ES6 module or directly referencing in web page html. 

### Install CommonJS/ES module
```
npm install dad-dapi
```

### Import CommonJS
```
var client = require('dad-dapi').client;
```

### Import ES6 module
```
import { client } from 'dad-dapi';
```

### Web require
The browser.js file under the '/lib' folder needs to be referenced from the page:
```
<script src="./lib/browser.js"></script>
```

The use of the code is required under the global namespace of DAD.
```
var client = dApi.client;
```

### Initialisation
dApp needs to register itself as a client with the dad-dapi library to enable the communication.

```
import { client } from 'dad-dapi';

client.registerClient({});
```

# Build

### Required Tools and Dependencies

* Node
* Npm

### Developing

Execute these commands in the project's root directory:

#### Download
```
git clone 'https://github.com/DAD-Chain/dad-dapi.git'
cd dad-dapi
```

#### Install

```
npm install
```

#### Development build
This will build the project with minimum polyfilling for better debug experience.

````
npm run build:dev
````

You will get the packaged code under '/lib'.

#### Production build 

````
npm run build:prod
````

You will get the packaged code under '/lib'

## Built With

* [TypeScript](https://www.typescriptlang.org/) - Used language
* [Node.js](https://nodejs.org) - JavaScript runtime for building
