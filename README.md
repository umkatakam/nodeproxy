# nodeproxy
A simple proxy server built using nodeJS. This repo is a part of pre work of codepath nodeJS course.

Below are set up instructions and feature examples:

# Set up
- clone the repo 
```
git clone https://github.com/umkatakam/nodeproxy.git
```
- install dependecies 
```
npm install
```

# Start node server

1. Using `babel-node`

```
babel-node index.js
```

2. Using `nodemon`
```
nodemon --exec babel-node -- index.js
```
![alt tag](https://github.com/umkatakam/nodeproxy/blob/master/images/start-server-nodemon.gif)

3. Using npm start script
```
npm start
```
![alt tag](https://github.com/umkatakam/nodeproxy/blob/master/images/start-server-npm-start.gif)

# Features
- _Echo Server_:
To use the echo server. Start the node server using one of the above mentioned methods. Then use the `curl` command and make a request. As shown in the below demo. The echo server is running on port `8000`
![alt tag](https://github.com/umkatakam/nodeproxy/blob/master/images/feature-echo-server.gif)

- _Proxy Server_:
To use the proxy server. Start the node server using one of the above mentioned methods. Then use the `curl` command and make a request. As shown in the below demo. The proxy server is running on the port `8001`. In this example the destination server by default is the echo server running on port `8000`.
![alt tag](https://github.com/umkatakam/nodeproxy/blob/master/images/feature-basic-proxy-server.gif)

- _CLI with argv_:
To pass in custom destination url during server start up. Pass it as arguments. Possible arguments are `url`, `port` & `host`. An example of passing custom arguments during start up

```
nodemon --exec babel-node -- index.js --url http://www.google.com
```
![alt tag](https://github.com/umkatakam/nodeproxy/blob/master/images/feature-cli-argv-url.gif)

- _CLI pass destination url as request header_:
To pass destination url in the request header pass it under the header name `x-destination-url`.
```
e.g.: curl -v http://127.0.0.1:8001 -H 'x-destination-url:http://www.google.com'
```
![alt tag](https://github.com/umkatakam/nodeproxy/blob/master/images/feature-cli-header-url.gif)

- _Logging to stdout_:
By deafult all the logs are written to `stdout`. Below is an example of how the log statements look.
![alt tag](https://github.com/umkatakam/nodeproxy/blob/master/images/feature-logging-stdout.gif)

- _Confgiuring the output stream_:
In case you want to configure your log output stream and want all the logs to go into a log file. You can specify that as an argument during server start up. The argument would be `stream`.
e.g. of logging into a log file
```
nodemon --exec babel-node -- index.js --stream=/tmp/nodeproxy.log
```
![alt tag](https://github.com/umkatakam/nodeproxy/blob/master/images/feature-logging-log-file.gif)
