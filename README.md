# mos

judge mobile OS

```
module.exports = function() {
  var nvgt = navigator.userAgent, platform;
  if (nvgt.indexOf('Android') > -1 || nvgt.indexOf('Adr') > -1) {
    platform = 'android';
  }
  //此处为IOS手机
  if (!!nvgt.match(/\(i[^;]+;( U;)? CPU.+Mac OS X/)) {
    platform = 'ios';
  }
  return platform;
};
```

### npm i --save judge-mos

var platform = require('judge-mos')

if (platform() == 'ios') {
   console.log('ios');
} else if (platform() == 'android') {
  console.log('android');
}
