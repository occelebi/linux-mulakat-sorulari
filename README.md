Linux Sistem Yoneticisi/DevOps Mülakat Soruları
====================================================

https://github.com/chassing/linux-sysadmin-interview-questions sayfasinin turkce cevirisidir.

## <a name='toc'>Icerik</a>

  1. [Genel Sorular](#general)
  1. [Basit Linux Soruları](#simple)
  1. [Orta Seviye Linux Soruları](#medium)
  1. [Zor Linux Soruları](#hard)
  1. [Uzman Linux Soruları](#expert)
  1. [Networking Soruları](#network)
  1. [MySQL Soruları](#mysql)
  1. [DevOps Soruları](#devop)
  1. [Eglenceli Sorular](#fun)
  1. [Demo Time](#demo)
  1. [Other Great References](#references)


####[[⬆]](#toc) <a name='general'>Genel Sorular:</a>

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


####[[⬆]](#toc) <a name='simple'>Basit Linux Sorulari:</a>

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


####[[⬆]](#toc) <a name='medium'>Orta seviye Linux Sorulari:</a>

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
* SSH port yonlendirme(forwarding) nedir ?
* Yerel ve uzaktaki port yonlendirme arasindaki fark nedir ?
* useradd/adduser komutlarini kullanmadan sistemi kullanici eklemenin adimlari nelerdir ?
* Ozel dosyalardaki MAJOR ve MINOR numaralari ne anlama gelir ?
* "filesystem is full" hatasi alindiginda 'df' komutu kullanabilir alan gosteriyorsa sebebi ne olabilir ?
* Dosya silindikten sonra df komutunun bosalan alani gostermemesinin sebebi ne olabilir ?
* 'ps' komutu nasil calisir ?
* Olen yavru surecin onu bekleyen ebeveyn sureci yoksa ne olur ? Bu neden kotudur ?
* Bir surecin tum sureclerini kisaca acikla.
* Hangi surecin hangi portu dinledigi nasil ogrenilir ?
* Zombie surec nedir ve ne sebep olur ?
* Bir bash scripti calisirken ayni anda hem terminale cikti versin hem de dosyaya yazilsin istiyorsan ne yapmaliyiz ?
* echo "1" > /proc/sys/net/ipv4/ip_forward komutu ne yapar ?
* https://foo.example.com sitesi icin gecerli sertifika olusturup yuklemenin adimlarini kisaca acikla.
* Birkac HTTPS sanal host ayni IP'yi paylasabilir mi ? 
* Wildcard sertifika nedir ?
* Hangi Linux dosya tiplerini biliyorsun ?
* Surec(process) ile thread arasindaki fark nedir ? Fork sistem cagrisindan sonra ebeveyn ve yavru surecler arasindaki fark nasil olur ?
* Fork ve exec arasindaki fark nedir ?
* "nohup" ne icin kullanilir ?
* Asagidaki iki komutun farki nedir ?
 * ```myvar=hello```
 * ```export myvar=hello```
* Yerel ntp.conf dosyasinda kac tane NTP sunucusu bulundururdun ?
* ```ntpq -p``` komutunun ciktisinda 'reach' sutunu ne anlama gelir ?
* 100-1000 sunucunu arasindaki bir sayidaki sunucunun kernel guncellemesini nasil yapardin ?
* SCSI diskin, Host, Channel, ID, LUN degerlerini nasil gorursun ?
* Bir surecin bellek kullanimini nasil kisitlarsin ?


####[[⬆]](#toc) <a name='hard'>Zor linux sorulari:</a>

* Tunel nedir, http proxy'i nasil bypass edersin ?
* IDS ve IPS arasindaki fark nedir ?
* Ne tur kisayollari genelde kullanilirsin ?
* Linux Standard Base nedir ?
* Atomik operasyon nedir ?
* Yeni yapilandirdigin http sunucusu yeniden makina yeniden baslatildiktan sonra calismiyorsa ne yaparsin ?
* ~/.ssh/authorized_keys dosyasinda ne tur anahtarlar tutulur ve ne icin kullanilir ?
* Public ssh anahtarimi authorized_keys dosyasina ekledim ama hala sifre girmem gerekiyor, sorun nerde olabilir ?
* RPM, DEB veya solaris paketi olusturdun mu hic ? 
* ```:(){ :|:& };:``` komutu ne ise yarar ?
* Linux sinyalini script araciligiyla nasil yakalarsin ?
* SIGKILL sinyali yakalanabilir mi ?
* Linux cekirdigi OOM killer'i baslattiginde ne olur, hangi sureci ilk durduracagini nasil secer ?
* Linux boot surecini makinaya enerji vermekten promtu alana kadar olabildigince detayli anlatin. 
* Chroot jail nedir ?
* umount komutu dizinin mesgul oldugunu soyluyorsa dizini alikoyan surecin PID'sini nasil buluruz ? 
* LD_PRELOAD nedir, ne zaman kullanilir ?
* Bir ikili(binary) dosya calistirdin ama hic birsey olmadi, nasil debug edersiniz ?
* cgroup nedir ? Ne gibi bir durumda kullanilirlar ?


####[[⬆]](#toc) <a name='expert'>Uzman Linux Sorulari:</a>


* Calisan bir surec soketi okurken ```EAGAIN: Resource temporarily unavailable``` hatasi aliyor. Sureci durdurmadan soket veya dosya descriptoru nasil kapatirsin ?


####[[⬆]](#toc) <a name='network'>Ag Sorulari:</a>

* localhost nedir ? Neden ```ping localhost``` komutu hata verir ?
* "ping" & "traceroute" komutu arasinda benzerlik nedir ? traceroute hoplari nasil bulur ?
* Butun port ve soket baglantilarini gosteren komut nedir ?
* 300.168.0.123 gecerli bir IPv4 adresi midir ?
* Hangi IP araliklari/altaglari "private" veya "non-routable" (RFC 1918) kategorisine girer ?
* VLAN nedir ?
* ARP nedir ve ne icin kullanilir ?
* TCP ve UDP arasindaki fark nedir ?
* Varsayilan gateway ne icin kullanilir ?
* Yonlendirme tablosunu gosteren komut nedir ?
* Bir TCP baglantisi agda 4 farkli essiz sey ile tanimlanir. Bunlar nedir ?
* Istemci web tarayicisi ile web sunucusuna baglandiginda baglantinin kaynak ve hedef portu ne olur ?
* Ozel bir arayuze IPv6 adres nasil eklenir ?
* eth0 arayüzüne IPv4 ve IPv6 adresine ekledikten sonra v4 adresine gönderilen ping çalışıyor fakat v6 adresine gönderilen pingin sonucu ```sendmsg: operation not permitted``` hatası alınıyorsa problem ne olabilir ?
* SNAT nedir ne için kullanılır ? 
* SSH tünelinden gelen bütün bağlantı paketlerini DROP eden bir linux sistemine ssh ile nasıl bağlanırsınız ? 
* DDoS'u durdurmak için en yaparsın ?
* IP paketinin içerini nasıl görürsün ?


####[[⬆]](#toc) <a name='mysql'>MySQL Soruları:</a>

* Kullanıcı nasıl oluşturulur ?
* Kullanıcıya nasıl yetki verilir ?
* "left" ve "right" join arasındaki fark nedir ?
* InnoDB ve MyISAM arasındaki farkı kısaca açıklar mısın ?.
* Basit bir master/slave cluster kurmak için hangi adımlar gereklidir ?
* MySQL'i kurduktan sonra neden "mysql_secure_installation" çalıstırılmalıdır ? 
* Hangi işlerin çalıştığını nasıl görülür ?


####[[⬆]](#toc) <a name='devop'>DevOps Soruları:</a>

* Bir script oluştururkenki çalışma akışını(workflow) açıklar mısın ?
* GIT nedir ?
* Dinamik ya da statik olarak bağlı dosya ne anlam ifade eder ?
* "configure && make && make install" komutu ne işe yarar ?
* puppet/chef/ansible neden kullanılır ?
* Yeni bir postgres kullanıcısı nasıl oluşturulur ?
* Sanal IP nedir ? Cluster nedir ?
* What is a virtual IP address? What is a cluster?
* Bir dosyadaki tüm yazdırılabilir karakterler nasıl yazdırılır ?
* Paylaşılan kütüphane bağımlılıkları(shared library dependicies) nasıl bulunur ?
* Automake ve Autoconf nedir ?
* ./configure komutu ```libfoobar is missing on your system``` hatası veriyorsa, problem ne olabilir nasıl çözülür ?
* Script veya derlenmiş programların avantajları ve dezavantajları nelerdir ?
* Devamlı teslim(continuous delivery) ve DevOps arasındaki bağlantı nedir ?
* Sistemin devamlı integrasyon(continous integration) ve devamlı canlıya alma(continous deployment) süreçlerinde önemli noktalar nelerdir ?


####[[⬆]](#toc) <a name='fun'>Eğlenceli Sorular:</a>

* Dikkatsiz bir sistem yöneticisi şu komutu çalıştırdıysa: ```chmod 444 /bin/chmod ``` - nasıl düzeltirdin ?
* root şifresini kaybettin, bu durumda ne yapılabilir ?
* Uzaktaki bir sunucuyu yeniden başlattım ama 10 dakika geçmesine rağmen hala ssh ile sisteme bağlanılmıyorsa problem ne olabilir ?
* Issız bir adaya düşsen yanına alacağın 5 linux komutu nedir ?
* Rastgele bir makinaya denk geldin, ilk olarak çalıştıracağın komut ne olurdu ?
* SSH protokolünü farklı şekilde kullandın mı hiç ? 
* Çalışan bir script yanlışlıkla sildin, nasıl geri getirirsin ?


####[[⬆]](#toc) <a name='demo'>Demo Zamanı:</a>


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
