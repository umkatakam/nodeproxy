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

- Using `babel-node`
```
babel-node index.js
```
- Using `nodemon`
```
nodemon --exec babel-node -- index.js
```
![alt tag](https://github.com/umkatakam/nodeproxy/blob/master/images/start-server-nodemon.gif)
- Using npm start script
```
npm start
```
![alt tag](https://github.com/umkatakam/nodeproxy/blob/master/images/start-server-npm-start.gif)

# Features
- Echo Server:
To use the echo server. Start the node server using one of the above mentioned methods. Then use the `curl` command and make a request. As shown in the below demo. The echo server is running on port `8000`
![alt tag](https://github.com/umkatakam/nodeproxy/blob/master/images/feature-echo-server.gif)

- Proxy Server:
To use the proxy server. Start the node server using one of the above mentioned methods. Then use the `curl` command and make a request. As shown in the below demo. The proxy server is running on the port `8001`. In this example the destination server by default is the echo server running on port `8000`.
![alt tag](https://github.com/umkatakam/nodeproxy/blob/master/images/feature-basic-proxy-server.gif)
