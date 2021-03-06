# Equihash - BeamHash Implementation
nodejs native binding to check for valid Equihash solutions

# Dependencies
````
sudo apt-get install build-essential libsodium-dev libboost-system-dev
````

# Usage
````javascript
var ev = require('bindings')('equihashverify.node');

var header = new Buffer(..., 'hex');
var solution = new Buffer(..., 'hex'); //do not include byte size preamble "fd4005"

ev.verify(header, nonce, solution, n, k, r); // default is BeamHashI 150/5/0
//returns boolean
````

# Backward compatibility
````javascript
ev.verify(header, nonce, solution);
````

# Test Suite:
````
sudo npm install -g mocha
npm install
mocha
````

