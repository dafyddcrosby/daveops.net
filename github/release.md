---
title: GitHub - Release
---

## Signing releases

```bash
git tag -s software-0.1
git push --tags
# publish a release
# download tarball
# verify tarball matches git
gpg --armor --detach-sign software-0.1.tar.gz
# add gpg signature to release
```
