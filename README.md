<p align="center"><img width="40%" src="https://getbitex.oss-cn-beijing.aliyuncs.com/projects/image/logo.svg" /></p>

GitBitEx is an open source cryptocurrency exchange.

## Demo
We deployed a demo version on a cloud server (2 Cores CPU 4G RAM). All programs run on this server. include (mysql,kafka,redis,gitbitex-spot,nginx,web...).

https://gitbitex.com:8080/trade/BTC-USDT

## Dependencies
`vue`
`vuex`
`vue-router`
`vue-property-decorator`
`typescript`
`webpack`

## Install
### Server
* git clone https://github.com/gitbitex/gitbitex-spot.git
* Create database and make sure **BINLOG[ROW format]** enabled
* Execute ddl.sql
* Modify conf.json
* Run go build
* Run ./gitbitex-spot
### Web
* git clone https://github.com/gitbitex/gitbitex-web.git
* Run `npm install`
* Run `npm start`
* Run `npm run build` to build production

## Configure BackEnd
Backend configured to run locally by default 127.0.0.1

If you'd like to use another ports and adresses:
* Configure back-end host in `gulpfile.js` use proxy
```
apiProxy = 'http://yourip:port/';
```
* Configure websocket host in `src/script/constant.ts`
```
static SOCKET_SERVER = 'ws://yourip:port/ws';
```
