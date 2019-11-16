# Wiki_by_nha
all things I always forget

## Host remotely
### Expose postgres port: 5432
```docker run --name posttest -d -p 5432:5432 -e POSTGRES_PASSWORD=dongbang009095 postgres:alpine```

### List all opening ports
```netstat -tulpn```

## Flutter build error:
- Firebase For Flutter Execution failed for task ':app:transformClassesWithDexForDebug': update gradle and google service

## Flutter build flavor
###IOS
```flutter run -d 350F9D48-A958-4551-88D5-21243897CB14 --flavor lop9_ios -t lib/main_lop9_ios.dart ```


## Jav Spring running
ps -A |grep java
kill -9 8959
java -jar MySchool-0.5.3.jar -d

## Copy file to host
scp path_to_file root@ip:/direct_path


## Ubuntu free space
sudo apt-get autoclean
sudo apt-get autoremove 

## 
Uninstalled Docker using:
```yum remove docker-engine.x86_64 docker-engine-selinux.noarch

Installed again using:

curl -fsSL https://get.docker.com/ | sh

chkconfig docker on

service docker start

The result of last command is:
Redirecting...
```


## sort by size

du -hs * | sort -h


## java service manager

What follows is the easiest way to install a Java application as system service in Linux.

Let's assume you are using systemd (which any modern distro nowadays does):

Firstly, create a service file in /etc/systemd/system named e.g. javaservice.service with this content:

```
[Unit]
Description=Java Service

[Service]
User=nobody
# The configuration file application.properties should be here:
WorkingDirectory=/data 
ExecStart=/usr/bin/java -Xmx256m -jar application.jar --server.port=8081
SuccessExitStatus=143
TimeoutStopSec=10
Restart=on-failure
RestartSec=5

[Install]
WantedBy=multi-user.target
```
Secondly, notify systemd of the new service file:

```systemctl daemon-reload```
and enable it, so it runs on boot:

```systemctl enable javaservice.service```
Eventually, you can use the following commands to start/stop your new service:
```
systemctl start javaservice
systemctl stop javaservice
systemctl restart javaservice
systemctl status javaservice
```
