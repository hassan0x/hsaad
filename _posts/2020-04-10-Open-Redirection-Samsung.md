---
layout: single
title: "Open Redirection on Samsung and Yahoo"
header:
  overlay_image: blog-cover.png
---

## Samsung Vulnerability Writeup

Affected Endpoint: ```https://smetrics.samsung.com/b/ss/```

Used Payload: ```Host: bing.com```

### How to Reproduce

1- Open this URL ```https://smetrics.samsung.com/b/ss/``` and send it to the repeater in burp suite.

2- Change the value in the ```Host Header``` to any domain you want for example: ```Host: bing.com```.

3- It will directly redirect to bing.com

### Impact

Whenever a user visits this URL, it will redirect them to ```bing.com``` or any other malicious site, It is used in phishing attacks.

### Proof of Concept

Orignal Request

<p align="center"><a href="/images/samsung1.jpg"><img src="/images/samsung1.jpg"></a></p>

Malicious Request

<p align="center"><a href="/images/samsung2.jpg"><img src="/images/samsung2.jpg"></a></p>

<p align="center"><a href="/images/samsung3.jpg"><img src="/images/samsung3.jpg"></a></p>


## Yahoo Vulnerability Writeup

Affected Endpoint: ```https://bomgar.corp.yahoo.com/login```

Used Payload: ```Host: bing.com```

### How to Reproduce

1- Open this URL ```https://bomgar.corp.yahoo.com/login``` and send it to the repeater in burp suite.

2- Change the value in the ```Host Header``` to any domain you want for example: ```Host: bing.com```.

3- It will directly redirect to bing.com

### Impact

Whenever a user visits this URL, it will redirect them to ```bing.com``` or any other malicious site, It is used in phishing attacks.

### Proof of Concept

Orignal Request

<p align="center"><a href="/images/yahoo1.jpg"><img src="/images/yahoo1.jpg"></a></p>

Malicious Request

<p align="center"><a href="/images/yahoo2.jpg"><img src="/images/yahoo2.jpg"></a></p>

<p align="center"><a href="/images/yahoo3.jpg"><img src="/images/yahoo3.jpg"></a></p>
