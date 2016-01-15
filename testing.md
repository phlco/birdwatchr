Setting up End to End Testing with [Protractor](https://angular.github.io/protractor/#/)

# One time setup

> You can run these from anywhere

1. npm install -g protractor
1. webdriver-manager update

# Using

1. Create a conf.js file

```js
exports.config = {
  framework: 'jasmine',
  seleniumAddress: 'http://localhost:4444/wd/hub',
  specs: ['spec.js']
};
```

1. Start the web-driver

```sh
$ webdriver-manager start
```

1. Start your server

```sh
$ node app.js
```

1. Write your tests

```js
// spec.js
describe('when something happens', function(){
  it('should do this', function(){
    // code to visit and expectations
  });
});
```

1. Run your tests

```sh
$ protractor conf.js
```
