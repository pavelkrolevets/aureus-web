## Open source cryptocurrency and derivatives exchange.

### Dependencies
`vue`
`vuex`
`vue-router`
`vue-property-decorator`
`typescript`
`webpack`

### Install
#### Server
* git clone https://github.com/pavelkrolevets/aureus.git
* Create database and make sure **BINLOG[ROW format]** enabled
* Execute ddl.sql
* Modify conf.json
* Run go build
* Run ./aureus

#### Web
* git clone https://github.com/pavelkrolevets/aureus-web.git
* Run `npm install`
* Run `npm start`
* Run `npm run build` to build production

### Configure BackEnd
Backend configured to run locally by default 127.0.0.1

If you have another ports and addresses in `conf.json` in backend:

* Configure back-end host in `gulpfile.js` use proxy
```
apiProxy = 'http://yourip:port/';
```
* Configure websocket host in `src/script/constant.ts`
```
static SOCKET_SERVER = 'ws://yourip:port/ws';
```
#### Referenced and respect
This project is a fork and continue of the original [gitbitex](https://github.com/gitbitex/gitbitex-web) work.