[Back to README](README.md)
# Prime Factors kata.
### Node.js version of Uncle bobs example.

```
cd ~/workspace
express prime-factors-kata
```
Output:
```
   create : prime-factors-kata
   create : prime-factors-kata/package.json
   create : prime-factors-kata/app.js
   create : prime-factors-kata/public
   create : prime-factors-kata/public/javascripts
   create : prime-factors-kata/routes
   create : prime-factors-kata/routes/index.js
   create : prime-factors-kata/routes/users.js
   create : prime-factors-kata/views
   create : prime-factors-kata/views/index.jade
   create : prime-factors-kata/views/layout.jade
   create : prime-factors-kata/views/error.jade
   create : prime-factors-kata/bin
   create : prime-factors-kata/bin/www
   create : prime-factors-kata/public/images
   create : prime-factors-kata/public/stylesheets
   create : prime-factors-kata/public/stylesheets/style.css

   install dependencies:
     $ cd prime-factors-kata && npm install

   run the app:
     $ DEBUG=prime-factors-kata:* npm start
```
Run the two commands at the end of the console output:
```
cd prime-factors-kata && npm install
DEBUG=prime-factors-kata:* npm start
```
Navigate to http://localhost:3000 in your browser. You will get the default welcome page.
```
Express

Welcome to Express
```

Initialise application for source control and add. See [Git Notes](Git-Notes.md)

Add your `favicon.ico` to `public` folder and uncomment line in app.js

`npm install --save-dev nodemon`

change `node` to `nodemon` in `package.json`

<hr>

create `test` and `ui_tests` directories.

<hr>

Add codeceptjs: `npm install --save-dev codeceptjs`

Install webdriverio `npm install --save-dev webdriverio`

Install phantomjs npm package ` npm install --save-dev phantomjs-prebuilt`

<hr>

Initialise codeceptjs:
* If installed globally use
```
codeceptjs init
```
* or if installed locally use
```
node_modules/.bin/codeceptjs init
```

<hr>

Generate 1st test:
<br>
`codeceptjs gt` if globally installed or `node_modules/.bin/codeceptjs gt` if local. <br>
Edit the generated `_test.js` file.

```
Feature('Prime Factors kata');

Scenario('We enter a Number and it returns the prime factors', (I) => {
  I.amOnPage('/');
  I.see('Prime Factors Kata');
  I.fillField('numberToFactor', '150');
  I.dontSee('4');

  I.click('Find Factors');
  I.see('2, 3, 5, 5');
  I.dontSee('4');
});
```
<hr>

Run the tests:
```
phantomjs --webdriver=4444
```
* If codeceptjs installed globally use
```
codeceptjs run --steps
```
* or if codeceptjs installed locally use
```
node_modules/.bin/codeceptjs run --steps
```

<hr>

Run the tests in debug:
```
phantomjs --webdriver=4444
```
* If codeceptjs installed globally use
```
codeceptjs run --debug
```
* or if codeceptjs installed locally use
```
node_modules/.bin/codeceptjs run --debug
```

<hr>

Install mocha
```
npm install --save-dev mocha
```

<hr>

Install supertest and chai. (Using nodejs assert `var assert = require('assert');`)
```
npm install --save-dev supertest chai
```

<hr>

Create integration test `./test/integration/index_test.js`
```
var request = require('supertest');
var app = require('../../app');
var expect = require('chai').expect;

describe('Prime Factors page', function () {
  it('shows the factors of number entered.', function (done) {
    request(app).post('/')
    .send({numberToFactor: '25'})
    .end(function (req, res) {
      expect(res.status).to.equal(200);
      expect(res.text).to.contain('5, 5');
      done();
    });
  });
});
```
`npm test test/integration/index_test.js`


pass object to render and update jade template
```
extends layout

block content
  h1= title
  p Welcome to #{title}
  p
    form(action='/', method='POST', name='prime_factors')
      div
        label(for='numberToFactor') Number To Factor:
        input(type='text' name='numberToFactor')
      div
        input(type='submit' value='Find Factors')
    div
      | Factors are #{factors}
```

<hr>

Add another test:
```
  it('shows the correct factors of 35.', function (done) {
    request(app).post('/')
    .send({numberToFactor: '35'})
    .end(function (req, res) {
      expect(res.status).to.equal(200);
      expect(res.text).to.contain('5, 7');
      done();
    });
  });
```

Test fails.

<hr>

We know we will need a function to give us the factors so start creating unit test.




Error: Cannot find module '../../routes/factorsOf'

`Create module '../../routes/factorsOf'`

1) Prime Factors diaplays the prime factors of 25:
     TypeError: factorsOf is not a function

```
function factorsOf () {

}
module.exports = factorsOf;
```

1) Prime Factors diaplays the prime factors of 25:
     AssertionError: undefined deepEqual [ 5, 5 ]

```
function factorsOf () {
  return [5, 5];
}
module.exports = factorsOf;
```
Test Passes.

<hr>

Write next test
