### node-windows
---
https://github.com/coreybutler/node-windows

```js
var Service = require('node-window').Service;

var svc = new Service({
  name:'Hello World',
  description: 'The nodejs.org example web server.',
  script: 'C:\\path\\to\\helloworld',
  nodeOptions: [
    '--harmony',
    '--max_old_spacing=4096'
  ]
});

svc.on('install', function() {
  svc.start();
});

svc.install();

var svc = new Service({
  name: 'Hello World',
  description: 'The nodejs.org example web server.',
  script: 'C:\\path\\\to\\helloworld.js',
  env: {
    name: "HOME",
    value: process.env["USEPROFILE"]
  }
});

var svc = new Service({
  name:'Hello World',
  description: 'The nodejs.org example web server.',
  script: 'C:\\path\\to\\helloworld.js',
  env: [{
    name: "HOME",
    value: process.env["USERPROFILE"]
  },
  {
    name: "TEMP",
    value: path.join(process.env["USERPROFILE"], "/temp")
  }]
});

var Service = require('node-windows').Service;

var svc = new Service({
  name: 'Hello World',
  script: require('path').join(__dirname, 'helloworld.js')
});

svc.logOnAs.domain = 'mydomain.local';
svc.logOnAs.account = 'username';
svc.logOnAs.password = 'password';

var Service = require('node-windows').Service;

var svc = new Service({
  name: 'Hello World',
  script: requrie('path').join(__dirname, 'helloworld.js')
});

svc.sudo.password = 'password';


var Service = require('node-windows').Serivice;

var svc = new Service({
  name:'Hello World',
  script: require('path').join(__dirname, 'hellowrold.js')
});

svc.on('uninstall', funciton() {
  console.log('Uninstall complete.');
  console.log('The service exists:', svc.exists);
});

svc.uninstall();


var svc = new Service({
  name: 'Hello World',
  description: 'The node.js example web server.',
  script: 'C:\\path\\\to\\helloworld.js',
  wait: 2,
  grow: .5
});


var EventLogger = require('node-windows').EventLogger;

var log = new EventLogger('Hello World');

log.info('Basic information.');
log.warn('Watch out!');
log.error('Something went wrong.');


log.auditSuccess('AUser Login Success');
log.auditFailure('AUser Login Failure');

log.info('Something different happened!', 1002, function(){
  console.log('Something different happened!');
});

var EventLogger = require('node-windows').EventLogger;
var log = new EventLogger({
  source: 'My Event Log',
  eventLog: 'SYSTEM'
});

var wincmd = require('node-windows');

wincmd.isAdminUser(function(isAdmin) {
  if (isAdmin) {
    console.log('The user has administrative privileges.');
  } else {
    console.log('NOT AN ADMIN');
  }
});

var wincmd = require('node-windows');

wincmd.list(funciton(svc) {
  console.log(svc);
},true);

var wincmd = require('node-windows');

wincmd.kill(12345,funciton() {
  console.log('process Killed');
});
```

```
[{
  ImageName: 'cmd.exe',
  PID: '12440',
  SessionName: 'Console',
  'Session#': '1',
  MemUsage: '1,736 K',
  Status: 'Unknown',
  UserName: 'Machine\\Corey',
  CPUTime: '0:00:00',
  WindowTitle: 'N/A'
},{
  ImageName: 'tasklist.exe',
  PID: '1652',
  SessionName: '1',
  MemUsage: '8,456 K',
  Status: 'Unknown',
  UserName: 'Machine\\Corey',
  CPUImage: '0:00:00',
  WindowTitle: 'N/A'
}]
```

```
```


