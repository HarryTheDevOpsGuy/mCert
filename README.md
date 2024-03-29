**Join Us**: [![Slack](https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white)](https://harrythedevopsguy.slack.com)  [![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/TheDevOpsProfessionals)  [![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://chat.whatsapp.com/Go0FgwQs9GtKp6js2l6RTG)

# mCert Version
 **Version**        : v0.2.3 <br>
 **Release Date**   : 26-Nov-22 <br>


 [![mCert - Monitor your SSL Certificate Smartly](http://img.youtube.com/vi/iR8SUlDbVSg/0.jpg)](https://www.youtube.com/watch?v=iR8SUlDbVSg "Get SSL Notification before SSL getting expired")

- **You can support us by** -> [Joining Our DevOps Group](https://t.me/TheDevOpsProfessionals)

- **Lets Monitor SSL with mCert free of cost** : [mCert-Tracker - Demo ](https://harrythedevopsguy.medium.com/monitor-website-uptime-status-free-of-cost-311d87d0b991)



#### What is mCert ?
mCert is small script to notify before ssl expiration. it will help you to renew your ssl before getting expired.

#### Mode of alert Notification
There are two Notification methods are available. you can use both or any one.
  - Email Notification
  - Slack Notification

#### Prerequisite
if you want get notification on your email you must need to install mSlack. if you want to get slack notification you must need to install mSlack accordingly. or you can install and configure both if you wish to get notification on both.

 - mSend - To get email notification - [Installation steps](https://github.com/HarryTheDevOpsGuy/mSend)
 - mSlack - To get slack notification - It will install automatically.


##### Step 1: Install mCert.
```bash
sudo curl -sL "https://github.com/HarryTheDevOpsGuy/mCert/raw/master/$(uname -p)/mcert" -o /usr/bin/mcert
sudo chmod +x /usr/bin/mcert

# Verify installation
mcert -v

# Check SSL Status
mcert -d "www.google.com facebook.com"

```

#### Getting Start with help

```bash
## mcert -h

mCert [OPTION]
-d domain_name   Domain to test ssl expiration
-x days          Certificate expiration interval (eg. if cert_date days)
-f domain_file   File with a list of FQDNs|domains
-a email         Send Email Notification (Combine Report).
-e email         Send Email Notification
-s '#devops'      Send Slack Notification
-q               Don't print anything on the console
-b               Display header on the console
-r               Attach full csv report with combine report
-V               enable verbose
-h               Display this help
-v               Display version
```

#### Example 1
To Test `www.google.com` ssl certificate if certificate expiry remaining day less than 60 day. it will send email notification at `your_email@domain.com`.

```bash
mcert -d www.google.com -e your_email@domain.com -x 60 -V
```
* `-x 60` check certificate expiration days.
* `-V`  enable verbose mode

#### Example 2

if you want to test multiple domains you can run below command. it will send email and slack notification if any domain is going to expire within 60 days.

```bash
mcert -d "www.google.com facebook.com" -s "#devops" -e "your_email@domain.com" -x 60 -V
```
#### Example 3

if you want to test multiple domains you can run below command. it will send email and slack notification if any domain is going to expire within 60 days.

Here you can create list of domains in txt file.

```bash
#cat /opt/domains.txt
www.google.com
www.facebook.com
www.apple.com
```

```bash
mcert -f "/opt/domains.txt" -s "#devops" -e "your_email@domain.com" -x 60 -V
```
* `-f` - to provide domain list file path.


#### Email Notification Template | Report

 ![mCert email alert templates](https://raw.githubusercontent.com/HarryTheDevOpsGuy/mCert/master/assets/img/email_snapshot.png)

 ![mCert email alert templates](https://cdn.jsdelivr.net/gh/mCloud-Automation/mData/images/mCert_Email.png)


 #### Do you want monitor your website free of cost ?
 **Yes**, its free of cost, you can submit your websites and email id, and we will notify you accordingly.

 **Step To submit New Domain** : [mCert-Tracker](https://harrythedevopsguy.medium.com/monitor-website-uptime-status-free-of-cost-311d87d0b991)

#### Thanks you
**Feel free to join us** -> [The DevOps Professionals Group](https://t.me/TheDevOpsProfessionals)
