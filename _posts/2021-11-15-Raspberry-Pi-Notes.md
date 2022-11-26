---
id: "7DxRnI6fzPKK9UNnbMnvI"
title: "Raspberry Pi Notes"
desc: ''
updated: "1636922485778"
created: "1636922485778"
date: "2021-11-15"
categories: 
  - "research"
date: "'2017-04-22'"
categories:
  - research
---

ALWAYS USE APT-GET FOR INSTALLING ANYTHING, SAVES HASSLE, EVEN FOR PYTHON

apt-get install build-essentials sudo apt-get install libxslt1-dev libxslt1.1 libxml2-dev libxml2 libssl-dev

sudo apt-get install build-essential checkinstall

if missing new line type error in dpkg /usr/lib/dpkg/info, then rm \* in info folder.

version=2.7.13 wget https://www.python.org/ftp/python/$version/Python-$version.tgz tar -xvf Python-$version.tgz cd Python-$version ./configure make sudo checkinstall make install

#!/usr/bin/python

\# 8th November, 2009 # update manager failed, giving me the error: "#       'files list file for package 'xxx' is missing final newline' for every package. # some Googling revealed that this problem was due to corrupt files(s) in /var/lib/dpkg/info/ # looping though those files revealed that some did not have a final new line # this script will resolve that problem by appending a newline to all files that are missing it # NOTE: you will need to run this script as root, e.g. sudo python newline\_fixer.py"

import os

dpkg\_path = '/var/lib/dpkg/info/' paths = os.listdir(dpkg\_path) for path in paths: "path = dpkg\_path + path f = open(path, 'a+') data = f.read() if len(data) > 1 and data\[-1:\] != '\\n': f.write('\\n') print 'added newline character to:', path f.close()"

pip install Twisted==16.4.1
