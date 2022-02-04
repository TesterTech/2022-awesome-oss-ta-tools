# 2022 Awesome OSS Test Automation tools 
- This repo will show 10 test automation (related) tools in the OpenSource Software (OSS) space. The list is by no means complete and will show some well-known tools in the OSS space.

## SeleniumBase
- Python
- Can automate/test
    - Webbrowser, API, Visual, Mobile
- Features
    - Reports, Dashboard, Recorder (early release), Interactive debugging, Webdriver grid/manager, Screenshots.
- Official release 2016
- https://seleniumbase.io
- https://github.com/seleniumbase/SeleniumBase

```
#!/bin/bash
sudo dnf install -y python3-pip 
echo clone SeleniumBase
git clone https://github.com/seleniumbase/SeleniumBase.git
cd SeleniumBase
echo Create the virtual environment
python -m venv . 
. bin/activate 
pip install . 
## For Jenkins (xvfb)
# dnf install xorg-x11-server-Xvfb python3-pytest-xvfb python3-xvfbwrapper
```

```
pytest examples/test_swag_labs.py --browser=firefox
```

## Cerberus
- Webbased
- Can automate/test
    - Webbrowser, API, Mobile, Database
- Features
    - Reports, Dashboard, Test case management, Requirements, Screenshots.
- 1st commit on Github 2013
- https://cerberus-testing.com
- https://github.com/cerberustesting
- Install guide Linux: https://github.com/cerberustesting/cerberus-source/blob/master/INSTALL

## Cypress
- Node
- Can automate/test
    - Webbrowser, API, Mobile, Database
- Features
    - Reports, Dashboard, Time travel, Screenshots/videos.
- 1st Github commit 2014
- https://www.cypress.io/
- https://github.com/cypress-io/cypress
- Install: https://docs.cypress.io/guides/getting-started/installing-cypress#Direct-download

```
# Linux (Fedora)
sudo dnf install npm -y 
sudo dnf install -y xorg-x11-server-Xvfb gtk2-devel gtk3-devel libnotify-devel GConf2 nss libXScrnSaver alsa-lib
npm install cypress
```

## RobotFramework
- Python
- Can automate/test
    - Webbrowser, API, Mobile, Database and many more
- Features
    - Keyword driven testing, Reports, Dashboard, Screenshots
- 1st version 2005
- https://robotframework.org
- https://github.com/robotframework
```
# VSCodium
sudo rpmkeys --import https://gitlab.com/paulcarroty/vscodium-deb-rpm-repo/-/raw/master/pub.gpg
printf "[gitlab.com_paulcarroty_vscodium_repo]\nname=download.vscodium.com\nbaseurl=https://download.vscodium.com/rpms/\nenabled=1\ngpgcheck=1\nrepo_gpgcheck=1\ngpgkey=https://gitlab.com/paulcarroty/vscodium-deb-rpm-repo/-/raw/master/pub.gpg\nmetadata_expire=1h" | sudo tee -a /etc/yum.repos.d/vscodium.repo
sudo dnf update -y 
sudo dnf install -y codium
```
```
# Chromedriver 
https://chromedriver.storage.googleapis.com/98.0.4758.48/chromedriver_linux64.zip
unzip chromedriver_linux64.zip 
sudo cp chromedriver /usr/local/bin
```
```
# WebDemo
mkdir git && cd git
git clone https://github.com/robotframework/WebDemo
cd WebDemo
python -m venv .
. bin/activate
pip install -r requirements.txt 
nohup python demoapp/server.py > my.log 2>&1 &
echo $! > save_pid.txt
```
```
# Launch the tests
robot --variable browser:chrome login_tests
kill -9 `cat save_pid.txt`
rm save_pid.txt
```

## Cucumber-JVM
- JAVA
- Can automate/test
    - You can extend Cucumber with all testing libraries in JAVA 
- Features
    - Reports, Dashboard.
- 1st version 2012
- https://cucumber.io/
- https://github.com/cucumber/cucumber-jvm
- https://github.com/TesterTech/cucumber-java-skeleton
- https://github.com/rest-assured/rest-assured/wiki/Usage

```
# install jdk 
sudo dnf install -y java-11-openjdk-devel maven 
```






