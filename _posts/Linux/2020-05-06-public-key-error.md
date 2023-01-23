---
title:  "Fix apt-get update “the following signatures couldn’t be verified because the public key is not available”"
author: Rupesh Bhandari
date:   2021-04-06 06:40:00 +0545
categories: [Linux, Ubuntu, Kali, Debian]
tags: [ubuntu]
---

If you tried adding another repository in the `etc/apt/sources.list`, you might have come across this problem as shown below:

![Error Message](/assets/img/keyerror/error.png)

This is due to the apt package management system's authentication mechanism. The sources has to be trusted for the package to be installed on a system so it validates for the key stored at `apt-key list`.

We are missing a key here, so to add that key we can the following command:

```shell
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys [Your KEY]
```

![Solution](/assets/img/keyerror/sol.png)

References:
- Various Sources
