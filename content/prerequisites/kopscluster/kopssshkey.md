---
title: "Create an SSH key"
chapter: false
weight: 31
pre: "<b>4. </b>"
---

Please run this command to generate SSH Key in Cloud9. This key will be used on the worker node instances to allow ssh access if necessary.

```bash
ssh-keygen
```

{{% notice tip %}}
Press `enter` 3 times to take the default choices
{{% /notice %}}

Upload the public key to your EC2 region:

```bash
aws ec2 import-key-pair --key-name "kopsnetworkshop" --public-key-material file://~/.ssh/id_rsa.pub
```
