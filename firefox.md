---
title: Firefox
---

## list of about: pages


  about:about

<https://developer.mozilla.org/en-US/Firefox/The_about_protocol>


## Debug logging
<https://developer.mozilla.org/en-US/docs/Mozilla/Debugging/HTTP_logging>

```bash
export NSPR_LOG_MODULES=timestamp,nsHttp:5,nsSocketTransport:5,nsStreamPump:5,nsHostResolver:5
export NSPR_LOG_FILE=~/Desktop/log.txt
./firefox
```

## Disable screenshots
extensions.screenshots.disabled -> true

## Disable new tab page
browser.newtabpage.enabled -> false

## Container tabs

* https://addons.mozilla.org/en-US/firefox/addon/multi-account-containers/