# StepNumberChange (SNC)

**2026.06.06 Update** — Issues fixed, now working properly. Please note the following:<br>
1. Currently only tested with email login. Users with phone number login can test it yourself; submit an Issue if there are problems.<br>
2. Fill in your email on line 8, and your password on line 9.<br>
3. Set the minimum step count on line 10, and the maximum desired step count on line 11.<br>
4. Tested and working on Alibaba Cloud. Tencent Cloud users can also give it a try — it should work in theory.

**2024.10.12 Update** — Fixed Taobao timestamp error. The code is now usable.

**2023.03.05 Update** — Phone number login is no longer supported. Use email login instead (works for both Alipay and WeChat). Simply enter your email in the account field. Code has been updated.

## 🚶‍♂️ Project Introduction

This project modifies step count data in the Xiaomi Sport app via `bushu.py`, then syncs it to WeChat and Alipay steps. Combined with Tencent Cloud's timer, it automatically generates random step counts daily (20,000–29,999 steps), configurable to any range.

Detailed usage documentation is provided below.

<hr>

## 👀 Important Clause

**1. Do not use any content from this repository for commercial or illegal purposes. You alone are responsible for any consequences.**

2. Any indirect user of this script, including but not limited to those who set up VPS or distribute it in violation of national/regional laws or regulations, is solely responsible for any privacy leaks or other consequences arising therefrom.

3. If any individual or organization believes that the scripts in this project may infringe their rights, they shall promptly notify us and provide proof of identity and ownership. We will remove the relevant scripts upon receiving verified documentation.

4. Anyone who views this project in any way, or directly or indirectly uses any script from this project, should read this disclaimer carefully. We reserve the right to modify or supplement this disclaimer at any time. By using or copying any script or rule from this project, you accept this disclaimer.

<hr>

## 🔨 Instructions

* This function references images from [a blogger's site](https://www.iloveu.top/) and code provided by the WeChat public account "Gwen博客". The final summarized method was written by me and uploaded to GitHub. If there is any infringement, please contact me immediately for removal.

**[Tencent Docs] SNC README** https://docs.qq.com/doc/DWmFLWU1MV2NpcVNQ — Full usage guide with screenshots is available in Tencent Docs. Below is the text version.

**[Tencent Docs] SNC Alibaba Cloud Tutorial** https://docs.qq.com/doc/DWk5rTVN1SldEdWNk — Alibaba Cloud version, relatively brief. Updated 2022.10.23, working properly.

**[Tencent Docs] SNC WeChat/Alipay Sync Troubleshooting** https://docs.qq.com/doc/DWkd6ZFRseUh5YXZi — If your steps aren't updating, check this document!

**Project Summary:** This project modifies the Xiaomi Sport app via code, then syncs the step data to WeChat and Alipay (**works on both iOS and Android, no root required**). Using Tencent Cloud's timer, it automatically generates random steps daily (20,000–29,999 steps).

If the default range is too high, you can modify it or enter a fixed step count on line 152. The random function can also be adjusted on line 91: `step = str(random.randint(min_steps, max_steps))`.

(Text tutorial below. A visual guide with screenshots is available in the Tencent Docs link above.)

1. Download the Xiaomi Sport app from the app store or browser. Open it and log in with your phone number (do not use third-party accounts).
2. Go to Profile → Third-Party Access and bind the platforms you want to sync. Note: For WeChat sync, follow the official account as instructed.
3. Download `bushu.py` and deploy it in Tencent Cloud Functions, placing it in `index.py`.
4. Enter your account and password on lines 148 and 150 for automatic login.
5. To set a custom step count, enter it on line 152. Leave blank for a random count (20,000–29,999).
6. Go to Trigger Management, create a trigger, and set the desired execution time.
7. Deploy and test. If successful, your step count will show up in Alipay.
8. Optional: Add notification scripts (QQ/WeChat). For QQ, use Qmsg酱 (register and fill in the token on line 123 in `qqtalk`). For WeChat, use Server酱 (https://sct.ftqq.com/). Explore on your own — entirely optional.

### If you have any issues, please leave an Issue. I'll reply to every one and help as best I can.

<hr>

## ✍🏻️ Personal Proposal

**I personally use step syncing for three purposes:**

1. Ant Forest — 296g energy per day;
2. Alipay → Ant Forest → Walking Donations → donate steps for charity (Alipay daily donation limit ~1,000,000 steps);
3. WeChat Movement → Leaderboard → My Profile → scroll down → Donate Steps → One Step Mini Program. (One Step also gives Little Red Flowers, redeemable for gifts. WeChat daily donation limit ~500,000 steps.)

(WeChat Movement direct donation is no longer available — just open the One Step mini program directly.)

**Using code to do some good for the world is, I believe, a meaningful thing. Code makes me feel like I've made a small contribution to this world. I hope everyone can use code to make the world a little better.**

**"I hope I can get to know this world again, and not waste the hardships I've endured in this life. If I can still do something to make others' lives better, then this life has been worth it."**
— From the acknowledgment section of Dr. Huang Guoping's doctoral thesis (UCAS, 2017)

<hr>

**Finally, a parting thought: Never fail to do good, no matter how small; never do evil, no matter how small.**

<hr>

### 📷 Screenshots

<hr>
<blockquote>
<img src="https://sszblog.oss-cn-shenzhen.aliyuncs.com/img/step0414.png" width="35%">  
<img src="https://sszblog.oss-cn-shenzhen.aliyuncs.com/img/step260608.jpg" width="30%">
<img src="https://sszblog.oss-cn-shenzhen.aliyuncs.com/img/step260609.jpg" width="30%">

<div align=center>

<img src="https://sszblog.oss-cn-shenzhen.aliyuncs.com/img/微信截图_20220612142253.png" width="30%">  
<img src="https://sszblog.oss-cn-shenzhen.aliyuncs.com/img/sc0612.png" width="30%">
<img src="https://sszblog.oss-cn-shenzhen.aliyuncs.com/img/redflower.png" width="35%">

The image above shows gifts redeemable in the Tencent Charity program. Limited daily quantities — available starting at 9:00 AM daily. A small perk. Personally confirmed that the bag is redeemable (limited to 50 per day). [Last updated 2022.10 — no longer available for redemption.]
</div>
</blockquote>
<hr>

<blockquote>
<h2>❤ Special Thanks</h2>
* Images from [the blogger's site](https://www.iloveu.top/)
* WeChat public account: Gwen博客
* Thanks a lot
</blockquote>

### 🌟 Star History

<hr>

[![Star History Chart](https://api.star-history.com/svg?repos=EEEugene/StepNumberChangeSNC&type=Date)](https://star-history.com/#bytebase/star-history&Date)

<hr>

### Support

<div align=center>

<img src="https://sszblog.oss-cn-shenzhen.aliyuncs.com/img/zfb.jpg" width="30%">
<img src="https://sszblog.oss-cn-shenzhen.aliyuncs.com/img/wx06.png" width="30%">
</div>

<h1 align="center">Leave a star before you go 🌟🌟🌟</h1>
