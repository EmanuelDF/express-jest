Express com Jest

- npm install express-generator -g
- express myapp
- cd myapp
- npm install
- mkdir js
- cd js

// sum.js
function sum(value1, value2) {
    return value1 + value2;
}
module.exports = sum;

// test/sum-test.js
jest.dontMock('../sum');

describe('sum', function() {
    it('adds 1 + 2 to equal 3', function() {
        var sum = require('../sum');
        expect(sum(1,2)).toBe(3);   
    })
});

- npm install jest-cli --save-dev

"scripts": {
    "test": "jest"
}

- npm test -- --watchAll