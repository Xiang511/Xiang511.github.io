---
title:  Instagram-Follow-Back-Tracker
author: LiHsiang
date: 2024-07-17 10:00:00 +0800
categories: [Side Project,Website]
tags: [HTML,CSS,Javascript,Instagram,Instagram-follower]
# pin: true
image:
  path: /assets/img/Instagram-Follow-Back-Tracker.png
  lqip: /assets/img/Instagram-Follow-Back-Tracker.png
---

![GitHub last commit](https://img.shields.io/github/last-commit/Xiang511/Instagram-Follow-Back-Tracker?display_timestamp=committer&style=for-the-badge){: .normal } ![GitHub Created At](https://img.shields.io/github/created-at/Xiang511/Instagram-Follow-Back-Tracker?style=for-the-badge){: .normal } ![GitHub License](https://img.shields.io/github/license/Xiang511/Instagram-Follow-Back-Tracker?style=for-the-badge){: .normal }


This method utilizes Instagram's "Download Your Data" feature to retrieve a list of your followers and following. By comparing the two lists, you can identify those who no longer follow you back.This tool only requires a JSON file and does not require any authorization or authentication.

## Features

- [x] Optimize website interface
- [x] See who's not following me back on Instagram
- [ ] Add a timeline to show how long a user has been following someone


## Usage

### Preparation

Navigate to the Account Management Center and Locate Your Information and Privacy Page

Click "Download information" > partail Information > Followers and followers list (only) > data range : all the time > Format select json

```
https://accountscenter.instagram.com/info_and_permissions/
```

### Process Downloaded Data

Once you receive the download completion email, click the link to download the ZIP file.

Extract the ZIP file and locate the ```followers.json``` and ```following.json``` files.

After the above steps are ready, you can go to the website and upload your JSON file.

## demo

{% include embed/youtube.html id='0XyRyZL3BO4?si=EXrGkiY3ETAXmoGF' %}

> Project Link
>
> [https://xiang511.com/Instagram-Follow-Back-Tracker/zh-TW.html](https://xiang511.com/Instagram-Follow-Back-Tracker/zh-TW.html)
{: .prompt-info }

## Data Privacy Policy

This website does not retain any relevant information, it only offers search capabilities.


## License

This project is published under GPL-3.0 License.
