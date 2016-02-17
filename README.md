# netatalk-cleanspec
Netatalk (Cleanspec)
Solid background reference: http://netatalk.sourceforge.net/wiki/index.php/Install_Netatalk_3.1.8_on_Ubuntu_14.04_Trusty

docker run -it -v /media/172a34d1-f9f5-421b-8152-0dbb0701d4b5/share:/media/share -v /etc/localtime:/etc/localtime:ro --publish 548:548 smalltree/netatalk-cleanspec:latest /bin/bash

adduser edit5

Backup /usr/local/etc/afp.conf

Edit afp.conf
Insert "spotlight = yes" under [Global]

Create [Share] for example:

[Share]
path = /media/share
valid users = edit5

Check features and paths, using "afpd -V".

service avahi-daemon start
service netatalk start
