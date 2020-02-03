---
layout: default
title: IP Camera BAT 310 Hacking
dd: ipcamerabat310
category: timeline
tags: article
---

## Software
- use this document to update goaccess to the latest version: https://goaccess.io/download
- use this document to find the suitable log format: https://github.com/allinurl/goaccess/blob/master/config/goaccess.conf
- install jq linux tool
- 
## Analysis K8S nginx log
```bash
find */* -type f  -exec jq ".textPayload" \{\} \; | goaccess --log-format='%^ %^ [%h] %^ %^ [%d:%t %^] \"%r\" %^ %b \"%R\" \"%u\" %^ %^ [%v] %^:%^ %^ %T %^ %^' --date-format=%d/%b/%Y --time-format=%H:%M:%S - --with-output-resolver -o out.html
```


