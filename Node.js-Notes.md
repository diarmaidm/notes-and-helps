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

### General npm and node helps
Trends:
1. http://www.npmtrends.com/mocha-vs-chai-vs-jasmine
1. http://www.npmtrends.com/react-vs-angular
**Note: Angular is a framework whereas react is a library.**
1. http://www.npmtrends.com/backbone-vs-angular-vs-react **Backbone vs Angular. React included for reference.**
1. http://www.npmtrends.com/gulp-vs-grunt
