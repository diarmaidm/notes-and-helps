[Back to README](README.md)
#### [Node.js](https://nodejs.org/en/)

#### [npm repository](https://www.npmjs.com)
#### [npm docs](https://docs.npmjs.com)

### Install node.js
See http://nodejs.org for various methods to install.

* Binary Directly from nodejs.org - follow instructions under **Binary Directly from nodejs.org** http://stackabuse.com/how-to-install-node-js-on-ubuntu/
```
wget http://nodejs.org/dist/v4.4.2/node-v4.4.2-linux-x64.tar.gz
sudo tar -C /usr/local --strip-components 1 -xzf node-v4.4.2-linux-x64.tar.gz
```
* You can install using package manager https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions

* You can use nvm for multiple node versions https://github.com/creationix/nvm#install-script

### Prepare environment before creating a new node.js application
1. Install express globally ```npm install -g express```
1. Install express application generator globally ```npm install -g express-generator```
1. Install bower globally ```npm install -g bower```

### Create a new node.js express application
#### In the following steps **replace** `<work directory>` and `<application name>` with the actual names
1. Navigate to the work directory ```cd <work directory>```
1. Create the new application ```express <application name>```
1. Run the 2 commands from end of previous step
  * ```cd <application name> && npm install```
  * ```DEBUG=<application name>:* npm start```
  * In chrome navigate to http://localhost:3000/ to verify its working
  * Close tab in Chrome and Ctrl+C to stop the local server
1. Add libraries for testing as dev dependancies ```npm install --save-dev supertest mocha chai```

[This Stack Overflow question has answers with lots of helps](http://stackoverflow.com/questions/2353818/how-do-i-get-started-with-node-js)

#### General npm notes.
List packages in the current application:
```
npm ls --depth=0
```
```
├── body-parser@1.13.3
├── codeceptjs@0.3.4
├── cookie-parser@1.3.5
├── debug@2.2.0
├── express@4.13.4
├── jade@1.11.0
├── morgan@1.6.1
├── nodemon@1.9.2
├── phantomjs-prebuilt@2.1.7
├── serve-favicon@2.3.0
└── webdriverio@4.0.7
```
List all global installed packages:
```
npm ls -g --depth=0
```
```
├── express@4.13.4
├── express-generator@4.13.1
├── live-server@1.0.0
├── nodemon@1.9.2
├── npm@2.15.1
```
List with more detail.
```
npm ll -g --depth=0
```
or
```
npm la -g --depth=0
```


##### Trends:
* http://www.npmtrends.com/mocha-vs-chai-vs-jasmine
* http://www.npmtrends.com/react-vs-angular
**Note: Angular is a framework whereas react is a library.**
* http://www.npmtrends.com/backbone-vs-angular-vs-react **Backbone vs Angular. React included for reference.**
* http://www.npmtrends.com/gulp-vs-grunt
