# pushbots-nodejs
[![All Contributors](https://img.shields.io/badge/all_contributors-2-orange.svg?style=flat-square)](#contributors)
[![npm](https://img.shields.io/npm/dt/pushbots.svg)](https://www.npmjs.com/package/pushbots)
[![npm](https://img.shields.io/npm/v/pushbots.svg)](https://www.npmjs.com/package/pushbots)
[![Twitter Follow](https://img.shields.io/twitter/follow/pushbots.svg?style=social&label=Follow&style=plastic)](https://twitter.com/pushbots)

### Installation
```bash
npm install pushbots
```

### Usage

```javascript

var pushbots = require('pushbots');
var Pushbots = new pushbots.api({
	id:'548ef5901d0ab1f3228b456a',
	secret:'646f1ac2fd86ea14ae5a95db7fef724c'
});
Pushbots.setMessage("Hi from new nodeJS API!");//sending to (android and ios) platforms by default add optional paramater "0" for iOS, "1" for Android and "2" for Chrome.
Pushbots.customFields({"article_id":"1234"});
Pushbots.customNotificationTitle("CUSTOM TITLE");
//to send by tags
Pushbots.sendByTags(["myTag"]);

//to push to all
Pushbots.push(function(response){
	console.log(response);
});

//to push to one device 
var token = "APA91bEeYRWNVo2oc6DdTpSABGkqLm5QrTTbHVJbTGc6Bpjjlau";
Pushbots.pushOne(token, function(response){
    console.log(response);
});

//to push to multiple device up to 1,000 token
var tokens = ["APA91bEeYRWNVo2oc6DdTpSABGkqLm5QrTTbHVJbTGc6Bpjjlau"];
Pushbots.pushByToken(tokens, function(response){
    console.log(response);
});
```

## Contributors

Thanks goes to these wonderful people:

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
| [<img src="https://avatars0.githubusercontent.com/u/6784122?v=4" width="50px;"/><br /><sub><b>amrsobhy</b></sub>](http://amrsobhy.com)<br />[💻](https://github.com/PushBots/pushbots-nodejs/commits?author=amrsobhy "Code") | [<img src="https://avatars2.githubusercontent.com/u/733794?v=4" width="50px;"/><br /><sub><b>Abdullah Diaa</b></sub>](https://abdullahdiaa.com)<br />[💻](https://github.com/PushBots/pushbots-nodejs/commits?author=AbdullahDiaa "Code") |
| :---: | :---: |
<!-- ALL-CONTRIBUTORS-LIST:END -->
Contributions of any kind welcome!
