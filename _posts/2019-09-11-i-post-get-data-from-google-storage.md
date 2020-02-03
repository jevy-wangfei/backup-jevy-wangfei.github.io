---
layout: default
title: IP Camera BAT 310 Hacking
dd: ipcamerabat310
category: timeline
tags: article
---

## Software
- Install gcloud with gsutil included
- 

## Login google cloud using json file
document: https://cloud.google.com/sdk/gcloud/reference/auth/activate-service-account

```bash
gcloud auth activate-service-account test@test.iam.gserviceaccount.com --key-file=./secret.json

```

## Copy data
reference this document for detail: https://cloud.google.com/storage/docs/gsutil/commands/cp

-copy bucket data to local
```bash
gsutil -m cp -r gs://my-bucket/data ./data
```

## rsync data
reference this document for detail: https://cloud.google.com/storage/docs/gsutil/commands/rsync

- rsync local data from bucket
```bash
gsutil -m rsync -d -r gs://mybucket/data  ./data
```
