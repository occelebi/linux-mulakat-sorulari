Linux Sistem Yoneticisi/DevOps Mulakat Sorulari
====================================================

https://github.com/chassing/linux-sysadmin-interview-questions sayfasinin turkce cevirisidir.

## <a name='toc'>Table of Contents</a>

  1. [General Questions](#general)
  1. [Simple Linux Questions](#simple)
  1. [Medium Linux Questions](#medium)
  1. [Hard Linux Questions](#hard)
  1. [Expert Linux Questions](#expert)
  1. [Networking Questions](#network)
  1. [MySQL Questions](#mysql)
  1. [DevOps Questions](#devop)
  1. [Fun Questions](#fun)
  1. [Demo Time](#demo)
  1. [Other Great References](#references)


####[[⬆]](#toc) <a name='general'>General Questions:</a>

* Dun/gecen hafta ne ogrendin ?
* Tercih ettigin gelistirme/yonetim ortamindan bahset.(OS, Editor, Browsers, Tools etc.)
* En son yaptigin linux projesinden bahset.
* En son yaptigin en buyuk hatadan bahset, bugun nasil cozerdin ? Neler ogrendin ?
* Neden seni secmeliyiz ?
* Agda DNS'in ne gibi bir rolu var ?
* HTTP nedir ?
* HTTP proxy nedir, nasil calisir ?
* Kisaca HTTPS'in nasil caligtigini acikla.
* SMTP nedir ? Mail nasil SMTP araciligiyla ulastirilir ?
* RAID nedir ? RAID0, RAID1, RAID5, RAID10 nedir ?
* level 0 backup nedir ? Incremental(artan) backup nedir ?
* Linux sisteminin genel dosya sistemi hiyerarsisini acikla.


####[[⬆]](#toc) <a name='simple'>Simple Linux Questions:</a>

* Admin kullanicisinin adi ve UID'si nedir ?
* Bir dizin icindeki sakli dosyalar dahil butun dosyalari nasil listelersin ?
* Bir dizini ve icindekileri silen Linux komutu nedir ?
* Kullanilabilir/kullanilmis bellegi nasil goruruz ? Kullanilmamis bellek Linux'te mevcut mudur ?
* "my konfi is the best" cumlesini dizindeki dosyalarda ve altindaki dizinlerde nasil arariz ?
* Uzaktaki makinaya nasil baglaniriz veya SSH nedir ?
* Butun ortam degiskenleri nasil goruruz ve nasil kullaniriz ?
* ```ifconfig -a``` komutunu calistirdigimda "command not found" hatasi aliyorsam problem ne olabilir ?
* Iki kez TAB tusuna basarsam ne olur ?
* Linux sistemlerde kullanabilir disk alanini gosteren komut nedir ?
* DNS kayitlarini kontrol etmek icin hangi komutlar kullanilir ?
* Hangi Linux komutlari dosyanin aidiyetini ve izinleri degistirir ?
* ```chmod +x FILENAME``` komutu ne yapar ?
* 0750 izninin dosya uzerinde etkisi nedir ?
* 0750 izninin dizin uzerinde etkisi nedir ?
* Erisim(login) izni vermeden nasil kullanici olusturulur ?
* Bir kullaniciya nasil grup nasil eklenir, silinir ?
* Bash alias ne demektir ?
* Root veya bir kullanicinin mail adresini nasil ayarlarsin ?
* CTRL-c ne yapar ?
* /etc/services dosyanin icinde ne saklanir ?
* Standart cikis ve hatayi bash dilinde nasil yeniden yonlendirirsin ? (> /dev/null 2>&1)
* UNIX ile Linux arasindaki fark nedir ?
* Telnet ve SSH arasindaki fark nedir ?
* Uc yuk ortamasini(three load averages) acikla, neyi gosterirler ?


####[[⬆]](#toc) <a name='medium'>Medium Linux Questions:</a>

* Asagidaki komutlar ne ise yarar, nasil kullanilir ?
 * ```tee```
 * ```awk```
 * ```tr```
 * ```cut```
 * ```tac```
 * ```curl```
 * ```wget```
 * ```watch```
 * ```head```
 * ```tail```
* ```&``` karakteri komuttan sonra gelirse nasil etki gosterir ?
* ```& disown``` karakteri komuttan sonra gelirse ne etki gosterir ?
* Paket filtreleme nedir, nasil kullanilir ?
* Sanal bellek(virtual memory) nedir ?
* Swap nedir, ne icin kullanilir ?
* A, NS, PTR, CNAME, MX kayitlari ne anlama gelir ?
* Bilinen baska RR(resource record) var mi, nasil kullanilirlar ?
* Split-Horizon DNS nedir ?
* Sticky bit nedir ? 
* immutable bitin dosya uzerindeki etkisi nedir ? 
* Hardlink ve sembolik linkin arasindaki fark nedir ? Bunlarin kaynagini silinirse her iki durum icinde ne olur ?
* Inode nedir ve ne tur bilgiler tutar ?
* Dosya sistemi kontrolu siradaki yeniden baslatma surecinde nasil zorlanir ?
* SNMP nedir ne icin kullanilir ?
* runlevel nedir nasil gorulur ?
* What is a runlevel and how to get the current runlevel?
* What is SSH port forwarding?
* What is SSH port forwarding?
* What is the difference between local and remote port forwarding?
* What is the difference between local and remote port forwarding?
* What are the steps to add a user to a system without using useradd/adduser?
* What are the steps to add a user to a system without using useradd/adduser?
* What is MAJOR and MINOR numbers of special files?
* What is MAJOR and MINOR numbers of special files?
* Describe a scenario when you get a "filesystem is full" error, but 'df' shows there is free space.
* Describe a scenario when you get a "filesystem is full" error, but 'df' shows there is free space.
* Describe a scenario when deleting a file, but 'df' not showing the space being freed.
* Describe a scenario when deleting a file, but 'df' not showing the space being freed.
* Describe how 'ps' works.
* Describe how 'ps' works.
* What happens to a child process that dies and has no parent process to wait for it and what’s bad about this?
* What happens to a child process that dies and has no parent process to wait for it and what’s bad about this?
* Explain briefly each one of the process states.
* Explain briefly each one of the process states.
* How to know which process listens on a specific port?
* How to know which process listens on a specific port?
* What is a zombie process and what could be the cause of it?
* What is a zombie process and what could be the cause of it?
* You run a bash script and you want to see its output on your terminal and save it to a file at the same time. How could you do it?
* You run a bash script and you want to see its output on your terminal and save it to a file at the same time. How could you do it?
* Explain what echo "1" > /proc/sys/net/ipv4/ip_forward does.
* Explain what echo "1" > /proc/sys/net/ipv4/ip_forward does.
* Describe briefly the steps you need to take in order to create and install a valid certificate for the site https://foo.example.com.
* Describe briefly the steps you need to take in order to create and install a valid certificate for the site https://foo.example.com.
* Can you have several HTTPS virtual hosts sharing the same IP?
* Can you have several HTTPS virtual hosts sharing the same IP?
* What is a wildcard certificate?
* What is a wildcard certificate?
* Which Linux file types do you know?
* Which Linux file types do you know?
* What is the difference between a process and a thread? And parent and child processes after a fork system call?
* What is the difference between a process and a thread? And parent and child processes after a fork system call?
* What is the difference between exec and fork?
* What is the difference between exec and fork?
* What is "nohup" used for?
* What is "nohup" used for?
* What is the difference between these two commands?
* What is the difference between these two commands?
 * ```myvar=hello```
 * ```myvar=hello```
 * ```export myvar=hello```
 * ```export myvar=hello```
* How many NTP servers would you configure in your local ntp.conf?
* How many NTP servers would you configure in your local ntp.conf?
* What does the column 'reach' mean in ```ntpq -p``` output?
* What does the column 'reach' mean in ```ntpq -p``` output?
* You need to upgrade kernel at 100-1000 servers, how you would do this?
* You need to upgrade kernel at 100-1000 servers, how you would do this?
* How can you get Host, Channel, ID, LUN of SCSI disk?
* How can you get Host, Channel, ID, LUN of SCSI disk?
* How can you limit process memory usage?
* How can you limit process memory usage?


####[[⬆]](#toc) <a name='hard'>Hard Linux Questions:</a>
####[[⬆]](#toc) <a name='hard'>Hard Linux Questions:</a>


* What is a tunnel and how you can bypass a http proxy?
* What is a tunnel and how you can bypass a http proxy?
* What is the difference between IDS and IPS?
* What is the difference between IDS and IPS?
* What shortcuts do you use on a regular basis?
* What shortcuts do you use on a regular basis?
* What is the Linux Standard Base?
* What is the Linux Standard Base?
* What is an atomic operation?
* What is an atomic operation?
* Your freshly configured http server is not running after a restart, what can you do?
* Your freshly configured http server is not running after a restart, what can you do?
* What kind of keys are in ~/.ssh/authorized_keys and what it is this file used for?
* What kind of keys are in ~/.ssh/authorized_keys and what it is this file used for?
* I've added my public ssh key into authorized_keys but I'm still getting a password prompt, what can be wrong?
* I've added my public ssh key into authorized_keys but I'm still getting a password prompt, what can be wrong?
* Did you ever create RPM's, DEB's or solaris pkg's?
* Did you ever create RPM's, DEB's or solaris pkg's?
* What does ```:(){ :|:& };:``` do on your system?
* What does ```:(){ :|:& };:``` do on your system?
* How do you catch a Linux signal on a script?
* How do you catch a Linux signal on a script?
* Can you catch a SIGKILL?
* Can you catch a SIGKILL?
* What's happening when the Linux kernel is starting the OOM killer and how does it choose which process to kill first?
* What's happening when the Linux kernel is starting the OOM killer and how does it choose which process to kill first?
* Describe the linux boot process with as much detail as possible, starting from when the system is powered on and ending when you get a prompt.
* Describe the linux boot process with as much detail as possible, starting from when the system is powered on and ending when you get a prompt.
* What's a chroot jail?
* What's a chroot jail?
* When trying to umount a directory it says it's busy, how to find out which PID holds the directory?
* When trying to umount a directory it says it's busy, how to find out which PID holds the directory?
* What's LD_PRELOAD and when it's used?
* What's LD_PRELOAD and when it's used?
* You ran a binary and nothing happened. How would you debug this?
* You ran a binary and nothing happened. How would you debug this?
* What are cgroups? Can you specify a scenario where you could use them?
* What are cgroups? Can you specify a scenario where you could use them?




####[[⬆]](#toc) <a name='expert'>Expert Linux Questions:</a>
####[[⬆]](#toc) <a name='expert'>Expert Linux Questions:</a>


* A running process gets ```EAGAIN: Resource temporarily unavailable``` on reading a socket. How can you close this bad socket/file descriptor without killing the process?
* A running process gets ```EAGAIN: Resource temporarily unavailable``` on reading a socket. How can you close this bad socket/file descriptor without killing the process?




####[[⬆]](#toc) <a name='network'>Networking Questions:</a>
####[[⬆]](#toc) <a name='network'>Networking Questions:</a>


* What is localhost and why would ```ping localhost``` fail?
* What is localhost and why would ```ping localhost``` fail?
* What is the similarity between "ping" & "traceroute" ? How is traceroute able to find the hops.
* What is the similarity between "ping" & "traceroute" ? How is traceroute able to find the hops.
* What is the command used to show all open ports and/or socket connections on a machine?
* What is the command used to show all open ports and/or socket connections on a machine?
* Is 300.168.0.123 a valid IPv4 address?
* Is 300.168.0.123 a valid IPv4 address?
* Which IP ranges/subnets are "private" or "non-routable" (RFC 1918)?
* Which IP ranges/subnets are "private" or "non-routable" (RFC 1918)?
* What is a VLAN?
* What is a VLAN?
* What is ARP and what is it used for?
* What is ARP and what is it used for?
* What is the difference between TCP and UDP?
* What is the difference between TCP and UDP?
* What is the purpose of a default gateway?
* What is the purpose of a default gateway?
* What is command used to show the routing table on a Linux box?
* What is command used to show the routing table on a Linux box?
* A TCP connection on a network can be uniquely defined by 4 things. What are those things?
* A TCP connection on a network can be uniquely defined by 4 things. What are those things?
* When a client running a web browser connects to a web server, what is the source port and what is the destination port of the connection?
* When a client running a web browser connects to a web server, what is the source port and what is the destination port of the connection?
* How do you add an IPv6 address to a specific interface?
* How do you add an IPv6 address to a specific interface?
* You have added an IPv4 and IPv6 address to interface eth0. A ping to the v4 address is working but a ping to the v6 address gives yout the response ```sendmsg: operation not permitted```. What could be wrong?
* You have added an IPv4 and IPv6 address to interface eth0. A ping to the v4 address is working but a ping to the v6 address gives yout the response ```sendmsg: operation not permitted```. What could be wrong?
* What is SNAT and when should be used?
* What is SNAT and when should be used?
* Explain how could you ssh login into a Linux system that DROPs all new incomming packets using a SSH tunnel.
* Explain how could you ssh login into a Linux system that DROPs all new incomming packets using a SSH tunnel.
* How do you stop a DDoS?
* How do you stop a DDoS?
* How can you see content of ip packet?
* How can you see content of ip packet?




####[[⬆]](#toc) <a name='mysql'>MySQL questions:</a>
####[[⬆]](#toc) <a name='mysql'>MySQL questions:</a>


* How do you create a user?
* How do you create a user?
* How do you provide privileges to a user?
* How do you provide privileges to a user?
* What is the difference between a "left" and a "right" join?
* What is the difference between a "left" and a "right" join?
* Explain briefly the differences between InnoDB and MyISAM.
* Explain briefly the differences between InnoDB and MyISAM.
* Describe briefly the steps you need to follow in order to create a simple master/slave cluster.
* Describe briefly the steps you need to follow in order to create a simple master/slave cluster.
* Why should you run "mysql_secure_installation" after installing MySQL?
* Why should you run "mysql_secure_installation" after installing MySQL?
* How do you check which jobs are running?
* How do you check which jobs are running?




####[[⬆]](#toc) <a name='devop'>DevOps Questions:</a>
####[[⬆]](#toc) <a name='devop'>DevOps Questions:</a>


* Can you describe your workflow when you create a script?
* Can you describe your workflow when you create a script?
* What is GIT?
* What is GIT?
* What is a dynamically/statically linked file?
* What is a dynamically/statically linked file?
* What does "configure && make && make install" do?
* What does "configure && make && make install" do?
* What is puppet/chef/ansible used for?
* What is puppet/chef/ansible used for?
* How do you create a new postgres user?
* How do you create a new postgres user?
* What is a virtual IP address? What is a cluster?
* What is a virtual IP address? What is a cluster?
* How do you print all strings of printable characters present in a file?
* How do you print all strings of printable characters present in a file?
* How do you find shared library dependencies?
* How do you find shared library dependencies?
* What is Automake and Autoconf?
* What is Automake and Autoconf?
* ./configure shows an error that libfoobar is missing on your system, how could you fix this, what could be wrong?
* ./configure shows an error that libfoobar is missing on your system, how could you fix this, what could be wrong?
* What are the Advantages/disadvantages of script vs compiled program?
* What are the Advantages/disadvantages of script vs compiled program?
* What's the relationship between continuous delivery and DevOps?
* What's the relationship between continuous delivery and DevOps?
* What are the important aspects of a system of continous integration and deployment?
* What are the important aspects of a system of continous integration and deployment?




####[[⬆]](#toc) <a name='fun'>Fun Questions:</a>
####[[⬆]](#toc) <a name='fun'>Fun Questions:</a>


* A careless sysadmin executes the following command: ```chmod 444 /bin/chmod ``` - what do you do to fix this?
* A careless sysadmin executes the following command: ```chmod 444 /bin/chmod ``` - what do you do to fix this?
* I've lost my root password, what can I do?
* I've lost my root password, what can I do?
* I've rebooted a remote server but after 10 minutes I'm still not able to ssh into it, what can be wrong?
* I've rebooted a remote server but after 10 minutes I'm still not able to ssh into it, what can be wrong?
* If you were stuck on a desert island with only 5 command-line utilities, which would you choose?
* If you were stuck on a desert island with only 5 command-line utilities, which would you choose?
* You come across a random computer and it appears to be a command console for the universe. What is the first thing you type?
* You come across a random computer and it appears to be a command console for the universe. What is the first thing you type?
* Tell me about a creative way that you've used SSH?
* Tell me about a creative way that you've used SSH?
* You have deleted by error a running script, what could you do to restore it?
* You have deleted by error a running script, what could you do to restore it?




####[[⬆]](#toc) <a name='demo'>Demo Time:</a>
####[[⬆]](#toc) <a name='demo'>Demo Time:</a>


* Unpack test.tar.gz without man pages or google.
* Unpack test.tar.gz without man pages or google.
* Remove all "*.pyc" files from testdir recursively?
* Remove all "*.pyc" files from testdir recursively?
* Search for "my konfu is the best" in all *.py files.
* Search for "my konfu is the best" in all *.py files.
* Replace the occurrence of "my konfu is the best" with "I'm a linux jedi master" in all *.txt files.
* Replace the occurrence of "my konfu is the best" with "I'm a linux jedi master" in all *.txt files.
* Test if port 443 on a machine with IP address X.X.X.X is reachable.
* Test if port 443 on a machine with IP address X.X.X.X is reachable.
* Get http://myinternal.webserver.local/test.html via telnet.
* Get http://myinternal.webserver.local/test.html via telnet.
* How to send an email without a mail client, just on the command line?
* How to send an email without a mail client, just on the command line?
* Write a ```get_prim``` method in python/perl/bash/pseudo.
* Write a ```get_prim``` method in python/perl/bash/pseudo.
* Find all files which have been accessed within the last 30 days.
* Find all files which have been accessed within the last 30 days.
* Explain the following command ```(date ; ps -ef | awk ‘{print $1}’ | sort | uniq | wc -l ) >> Activity.log```
* Explain the following command ```(date ; ps -ef | awk ‘{print $1}’ | sort | uniq | wc -l ) >> Activity.log```
* Write a script to list all the differences between two directories.
* Write a script to list all the differences between two directories.
* In a log file with contents as ```<TIME> : [MESSAGE] : [ERROR_NO] - Human readable text``` display summary/count of specific error numbers that occured every hour or a specific hour.
* In a log file with contents as ```<TIME> : [MESSAGE] : [ERROR_NO] - Human readable text``` display summary/count of specific error numbers that occured every hour or a specific hour.




####[[⬆]](#toc) <a name='references'>Other Great References:</a>
####[[⬆]](#toc) <a name='references'>Other Great References:</a>


Some questions are 'borrowed' from other great references like:
Some questions are 'borrowed' from other great references like:


* https://github.com/darcyclarke/Front-end-Developer-Interview-Questions
* https://github.com/darcyclarke/Front-end-Developer-Interview-Questions
* https://github.com/kylejohnson/linux-sysadmin-interview-questions/blob/master/test.md
* https://github.com/kylejohnson/linux-sysadmin-interview-questions/blob/master/test.md
* https://github.com/gurmeet1109/docgurmeet/tree/master/InterviewQuestionsSamples
* https://github.com/gurmeet1109/docgurmeet/tree/master/InterviewQuestionsSamples
* http://slideshare.net/kavyasri790693/linux-admin-interview-questions
* http://slideshare.net/kavyasri790693/linux-admin-interview-questions
* https://github.com/gurmeet1109/docgurmeet/tree/master/InterviewQuestionsSamples
* https://github.com/gurmeet1109/docgurmeet/tree/master/InterviewQuestionsSamples
* https://github.com/kylejohnson/linux-sysadmin-interview-questions/blob/master/test.md
* https://github.com/kylejohnson/linux-sysadmin-interview-questions/blob/master/test.md
