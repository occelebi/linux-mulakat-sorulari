Linux Sistem Yöneticisi/DevOps Mühendisi Mülakat/İş Görüşmesi Soruları
====================================================

https://github.com/chassing/linux-sysadmin-interview-questions sayfasının türkçe çevirisidir.

## <a name='toc'>İçerik</a>

1. [Genel Sorular](#general)
1. [Basit Linux Soruları](#simple)
1. [Orta Seviye Linux Soruları](#medium)
1. [Zor Linux Soruları](#hard)
1. [Uzman Linux Soruları](#expert)
1. [Ağ Soruları](#network)
1. [MySQL Soruları](#mysql)
1. [DevOps Soruları](#devop)
1. [Eğlenceli Sorular](#fun)
1. [Demo Zamanı](#demo)
1. [Yapılacaklar](#todo)
1. [Çeviri İçin Katkıda Bulunanlar](#contributors)


#### [[⬆]](#toc) <a name='general'>Genel Sorular:</a>

* Dün/geçen hafta ne öğrendin?
* Tercih ettiğin geliştirme/yönetim ortamından bahset.(OS, Editör, Browsers, Tools etc.)
* Son yaptığın Linux projesinden bahset.
* Son yaptığın en büyük hatadan bahset, bugün nasıl çözerdin? Neler öğrendin?
* Neden seni seçmeliyiz?
* Ağda DNS'in ne gibi bir rolü var?
* HTTP nedir?
* HTTP proxy nedir, nasıl çalışır?
* Kısaca HTTPS'in nasıl çalıştığını açıkla.
* SMTP nedir? Mail nasıl SMTP aracılığıyla ulaştırılır?
* RAID nedir? RAID0, RAID1, RAID5, RAID10 nedir?
* Level 0 backup nedir? Incremental(artan) backup nedir?
* Linux sisteminin genel dosya sistemi hiyerarşisini açıkla.
* Public ve private SSH anahtarı arasında ne gibi farklar vardır?


#### [[⬆]](#toc) <a name='simple'>Basit Linux Soruları:</a>

* Admin kullanıcısının adı ve UID'si nedir?
* Bir dizin içindeki saklı dosyalar dahil bütün dosyaları nasıl listelersin?
* Bir dizini ve içindekileri silen Linux komutu nedir?
* Kullanılabilir/kullanılmış belleği nasıl görürüz? Kullanılmamış bellek Linux'te mevcut mudur?
* "my konfi is the best" cümlesini dizindeki dosyalarda ve altındaki dizinlerde nasıl ararız?
* Uzaktaki makinaya nasıl bağlanırız veya SSH nedir?
* Bütün ortam değişkenleri nasıl görürüz ve nasıl kullanırız?
* ```ifconfig -a``` komutunu çalıştırdığımda "command not found" hatası alıyorsam problem ne olabilir?
* İki kez TAB tuşuna basarsam ne olur?
* Linux sistemlerde kullanabilir disk alanını gösteren komut nedir?
* DNS kayıtlarını kontrol etmek için hangi komutlar kullanılır?
* Hangi Linux komutları dosyanın aidiyetini ve izinleri değiştirir?
* ```chmod +x FILENAME``` komutu ne yapar?
* 0750 izninin dosya üzerindeki etkisi nedir?
* 0750 izninin dizin üzerindeki etkisi nedir?
* Erişim (login) izni vermeden nasıl yeni kullanıcı oluşturulur?
* Bir kullanıcıya nasıl grup nasıl eklenir, silinir?
* Bash alias ne demektir?
* root veya bir kullanıcının mail adresini nasıl ayarlarsın?
* CTRL-c ne yapar?
* CTRL-d ne yapar?
* CTRL-z ne yapar?
* /etc/services dosyanın içinde ne saklanır?
* Standart çıkış ve hatayı Bash dilinde nasıl yeniden yönlendirirsin? (> /dev/null 2>&1)
* UNIX ile Linux arasındaki fark nedir?
* Telnet ve SSH arasındaki fark nedir?
* Üç yük ortalamasını (three load averages) açıkla, neyi gösterirler? Yük ortalamalarını görüntülemek için hangi komut kullanılabilir?
* GNU ```ls``` için geçerli olmayan bir küçük harf parametresi söyleyebilir misiniz?
* Linux kernel modülü nedir?
* Bir hatayı gidermek için single user mode'u nasıl boot edersin adım adım gösterir misin?
* Yönettiğiniz bir web uygulamasındaki 404 hatasını gidermek için atacağınız adımları anlatır mısın? 
* ICMP protokolü nedir? Neden kullanırız?

#### [[⬆]](#toc) <a name='medium'>Orta seviye Linux Soruları:</a>

* Aşağıdaki komutlar ne işe yarar, nasıl kullanılır?
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
* ```less```
* ```cat```
* ```touch```
* ```sar```
* ```netstat```
* ```tcpdump```
* ```lsof```
* ```&``` karakteri komuttan sonra gelirse nasıl etki gösterir?
* ```& disown``` karakteri komuttan sonra gelirse ne etki gösterir?
* Paket filtreleme nedir, nasıl kullanılır?
* Sanal bellek (virtual memory) nedir?
* Swap nedir, ne için kullanılır?
* A, NS, PTR, CNAME, MX kayıtları ne anlama gelir?
* Bilinen başka RR (resource record) var mı, nasıl kullanılırlar?
* Split-Horizon DNS nedir?
* Sticky bit nedir?
* Immutable bitin dosya üzerindeki etkisi nedir?
* Hardlink ve sembolik link arasındaki fark nedir? Bunların kaynağını silinirse her iki durum içinde ne olur?
* Inode nedir ve ne tür bilgiler tutar?
* Dosya sistemi kontrolü sıradaki yeniden başlatma sürecinde nasıl zorlanır?
* SNMP nedir ne için kullanılır?
* runlevel nedir nasıl görülür?
* SSH port yönlendirme (forwarding) nedir?
* Yerel ve uzaktaki port yönlendirme arasındaki fark nedir?
* useradd/adduser komutlarını kullanmadan sistemi kullanıcı eklemenin adımları nelerdir?
* Özel dosyalardaki MAJOR ve MINOR numaraları ne anlama gelir?
* mknod komutunu ve ne zaman kullanıldığını açıklayın.
* "filesystem is full" hatası alındığında 'df' komutu kullanabilir alan gösteriyorsa sebebi ne olabilir?
* Dosya silindikten sonra df komutunun boşalan alanı göstermemesinin sebebi ne olabilir?
* 'ps' komutu nasıl çalışır?
* Ölen yavru sürecin onu bekleyen ebeveyn süreci yoksa ne olur? Bu neden kötüdür?
* Bir sürecin tüm süreçlerini kısaca açıkla.
* Hangi sürecin hangi portu dinlediği nasıl öğrenilir?
* Zombie süreç nedir ve ne sebep olur?
* Bir bash scripti çalışırken aynı anda hem terminale çıktı versin hem de dosyaya yazılsın istiyorsan ne yapmalıyız?
* echo "1" > /proc/sys/net/ipv4/ip_forward komutu ne yapar?
* https://foo.example.com sitesi için geçerli sertifika oluşturup yüklemenin adımlarını kısaca açıkla.
* Birkaç HTTPS sanal host aynı IP'yi paylaşabilir mi?
* Wildcard sertifika nedir?
* Hangi Linux dosya tiplerini biliyorsun?
* Süreç (process) ile thread arasındaki fark nedir? Fork sistem çağrısından sonra ebeveyn ve yavru süreçler arasındaki fark nasıl olur?
* Fork ve exec arasındaki fark nedir?
* "nohup" ne için kullanılır?
* Aşağıdaki iki komutun farkı nedir?
* ```myvar=hello```
* ```export myvar=hello```
* Yerel ntp.conf dosyasında kaç tane NTP sunucusu bulundururdun?
* ```ntpq -p``` komutunun çıktısında 'reach' sütunu ne anlama gelir?
* 100-1000 sunucunu arasındaki bir sayıdaki sunucunun kernel güncellemesini nasıl yapardın?
* SCSI diskin, Host, Channel, ID, LUN değerlerini nasıl görürsün?
* Bir sürecin bellek kullanımını nasıl kısıtlarsın?
* Bash quick substitution/caret replace(^x^y) nedir?
* Farklı kabuk (shell) çeşitleri biliyor musun? Evetse, kullanma imkanın oldu mu?
* Tarpipe nedir? (ya da hard linkler ve özel dosyalar dahil olmak üzere birşeyi bir sunucudan diğerine komple olarak nasıl kopyalarsın?)
* httpd paketinin kurulu olup olmadığını nasıl anlarsın?
* Bir paketin içeriğini nasıl listeleyebilirsin?
* Hangi paketin daha iyi olduğunu nasıl anlayabilirsin: openssh-server-5.3p1-118.1.el6_8.x86_64 veya openssh-server-6.6p1-1.el6.x86_64 ?
* Blok tabanlı(block based) ve nesne tabanlı(object based) depolama arasındaki farkı bana açıklayabilir misin?

#### [[⬆]](#toc) <a name='hard'>Zor Linux soruları:</a>

* Tünel nedir, HTTP Proxy'i nasıl bypass edersin?
* IDS ve IPS arasındaki fark nedir?
* Genelde ne tür kısayolları kullanılırsın?
* Linux Standard Base nedir?
* Atomik operasyon nedir?
* Yeni yapılandırdığın HTTP sunucusu makina yeniden başlatıldıktan sonra çalışmıyorsa ne yaparsın?
* ~/.ssh/authorized_keys dosyasında ne tür anahtarlar tutulur ve ne için kullanılır?
* Public SSH anahtarımı authorized_keys dosyasına ekledim ama hala şifre girmem gerekiyor, sorun nerde olabilir?
* RPM, DEB veya Solaris paketi oluşturdun mu hiç?
* ```:(){ :|:& };:``` komutu ne işe yarar?
* Linux sinyalini script aracılığıyla nasıl yakalarsın?
* SIGKILL sinyali yakalanabilir mi?
* Linux çekirdiği OOM killer sürecini başlattığında ne olur, hangi süreci ilk durduracağını nasıl seçer?
* Linux boot sürecini makinaya enerji vermekten promptu alana kadar olabildiğince detaylı anlat.
* Chroot jail nedir?
* Umount komutu dizinin meşgul olduğunu söylüyorsa dizini alıkoyan sürecin PID'sini nasıl buluruz?
* LD_PRELOAD nedir, ne zaman kullanılır?
* Bir ikili (binary) dosya çalıştırdın ama hiç birşey olmadı, nasıl debug edilir?
* Cgroup nedir? Ne gibi bir durumda kullanılırlar?
* Yalnızca yazdırılamayan/yazılamayan(non-printable/non-type-able) karakterlerden oluşan dosya adına sahip bir dosyayı nasıl kaldırabilir/silebilirsin(remove/delete)?
* Linux'ta bir sürecin önceliğini nasıl artırabilir veya azaltabilirsin?


#### [[⬆]](#toc) <a name='expert'>Uzman Linux Soruları:</a>

* Çalışan bir süreç socketi okurken ```EAGAIN: Resource temporarily unavaılable``` hatası alıyor. Süreci durdurmadan socket veya file descriptor'u nasıl kapatırsın?
* Swappiness ile neyi kontrol edersin?
* TCP stack buffer'ını nasıl değiştirirsin? Nasıl hesaplarsın?
* Huge Tables nedir? Neden varsayılan olarak etkin değildir? Neden ve ne zaman kullanılır?
* LUKS nedir? Nasıl kullanılır?

#### [[⬆]](#toc) <a name='network'>Ağ Soruları:</a>

* Localhost nedir? Neden ```ping localhost``` komutu hata verir?
* "ping" & "traceroute" komutu arasında benzerlik nedir? Traceroute hopları nasıl bulur?
* Bütün port ve socket bağlantılarını gösteren komut nedir?
* 300.168.0.123 geçerli bir IPv4 adresi midir?
* Hangi IP aralıkları/altağları "private" veya "non-routable" (RFC 1918) kategorisine girer?
* VLAN nedir?
* ARP nedir ve ne için kullanılır?
* TCP ve UDP arasındaki fark nedir?
* Varsayılan gateway ne için kullanılır?
* Linux box'ta yönlendirme tablosunu gösteren komut nedir?
* Bir TCP bağlantısı ağda 4 farklı eşsiz şey ile tanımlanır. Bunlar nedir?
* İstemci web tarayıcısı ile web sunucusuna bağlandığında bağlantının kaynak ve hedef portu ne olur?
* Özel bir arayüze IPv6 adres nasıl eklenir?
* Eth0 arayüzüne IPv4 ve IPv6 adresine ekledikten sonra v4 adresine gönderilen ping çalışıyor fakat v6 adresine gönderilen pingin sonucu ```sendmsg: operation not permitted``` hatası alınıyorsa problem ne olabilir?
* SNAT nedir ne için kullanılır? 
* SSH tünelinden gelen bütün bağlantı paketlerini DROP eden bir Linux sistemine SSH ile nasıl bağlanırsınız? 
* DDoS saldırısını durdurmak için en yaparsın?
* IP paketinin içeriğini nasıl görürsün?
* IPoAC nedir? (RFC 1149)
* Port 0'ı bind ettiğinde ne olur?


#### [[⬆]](#toc) <a name='mysql'>MySQL Soruları:</a>

* Kullanıcı nasıl oluşturulur?
* Kullanıcıya nasıl yetki verilir?
* "left" ve "right" join arasındaki fark nedir?
* InnoDB ve MyISAM arasındaki farkı kısaca açıklar mısın?
* Basit bir master/slave cluster kurmak için hangi adımlar gereklidir?
* MySQL'i kurduktan sonra neden "mysql_secure_installation" çalıstırılmalıdır? 
* Hangi işlerin çalıştığını nasıl görülür?
* Bir MySQL veritabanının yedeğini nasıl alırsın?

#### [[⬆]](#toc) <a name='devop'>DevOps Soruları:</a>

* Bir script oluştururkenki çalışma akışını (workflow) açıklar mısın?
* GIT nedir?
* Dinamik ya da statik olarak bağlı dosya ne anlam ifade eder?
* "./configure && make && make install" komutu ne işe yarar?
* puppet/chef/ansible neden kullanılır?
* Nagios/Zenoss/NewRelic ne içindir?
* Jenkins/TeamCity/GoCI ne içindir?
* Konteyner ile VM (sanal makina) arasındaki fark nedir?
* Yeni bir postgres kullanıcısı nasıl oluşturulur?
* Sanal IP nedir? Cluster nedir?
* Bir dosyadaki tüm yazdırılabilir karakterler nasıl yazdırılır?
* Paylaşılan kütüphane bağımlılıkları (shared library dependicies) nasıl bulunur?
* Automake ve Autoconf nedir?
* ./configure komutu ```libfoobar is missing on your system``` hatası veriyorsa, problem ne olabilir nasıl çözülür?
* Script veya derlenmiş programların avantajları ve dezavantajları nelerdir?
* Devamlı teslim (continuous delivery) ve DevOps arasındaki bağlantı nedir?
* Sistemin devamlı integrasyon (continous integration) ve devamlı canlıya alma (continous deployment) süreçlerinde önemli noktalar nelerdir?
* Birden çok kullanılabilirlik alanındaki EC2 bulut sunucularının verileri paylaşmasına izin verecek şekilde AWS içinde ağ dosyası paylaşımını nasıl etkinleştirirsiniz?


#### [[⬆]](#toc) <a name='fun'>Eğlenceli Sorular:</a>

* Dikkatsiz bir sistem yöneticisi şu komutu çalıştırdıysa: ```chmod 444 /bin/chmod ``` - nasıl düzeltirdin?
* root şifresini kaybettin, bu durumda ne yapılabilir?
* Uzaktaki bir sunucuyu yeniden başlattım ama 10 dakika geçmesine rağmen hala SSH ile sisteme bağlanılmıyorsa problem ne olabilir?
* Issız bir adaya düşsen yanına alacağın 5 Linux komutu nedir?
* SSH protokolü farklı şekillerde nasıl kullanılabilir?
* Çalışan bir script yanlışlıkla sildin, nasıl geri getirirsin?
* Rastgele bir bilgisayarla karşılaşıyorsun ve bu evrenin komut satırı gibi duruyor. Yazacağın ilk şey nedir?
* Bana SSH'ı kullandığın yaratıcı bir durumdan bahseder misin?
* Çalışan bir scripti yanlışlıkla sildin, geri yüklemek için ne yapabilirsin?
* 19 Ocak 2038 tarihinde ne olacak?
* Yeniden başlatma komutu yanıt vermediğinde sunucu nasıl yeniden başlatılır?



#### [[⬆]](#toc) <a name='demo'>Demo Zamanı:</a>

* test.tar.gz dosyasını man sayfalarına ya da Google'a bakmadan nasıl açarsın?
* testdir dizininden bütün "*.pyc" dosyalarını nasıl silinir?
* "my konfu is the best" içeriği bütün *.py dosyalarında nasıl aranır?
* Bütün *.txt dosyalarındaki her "my konfu is the best" metinini "I'm a Linux jedi master" ile değiştir.
* IP adresi X.X.X.X olan makinanın 443 portunun erişilir olduğu nasıl kontrol edilir?
* Telnet ile http://myinternal.webserver.local/test.html sayfası nasıl indirilir? 
* Bir mail istemci olmadan komut satırı ile bir mail nasıl yollanılır?
* python/perl/bash/pseudo dillerinde ```get_prim``` methodu nasıl yazılır?
* Son 30 gün içerisinde erişilmiş bütün dosyalar nasıl bulunur?
* ```(date ; ps -ef | awk '{print $1}' | sort | uniq | wc -l ) >> Activity.log``` komutunun işlevi nedir?
* İki dizin arasındaki bütün farkları listeyen scripti yaz.
* ```<TIME> : [MESSAGE] : [ERROR_NO] - Human readable text``` formatındaki bir log dosyasındaki her saat veya belirli bir saatte oluşan belirli bir hata nasıl gösterilir?


#### [[⬆]](#toc) <a name='todo'>Yapılacaklar:</a>

* Mülakat soruları diye açıldı ama soruların cevapları da fena olmaz gibi geldi
* Gözden kaçan yazım hatalarına da açığım tabii :)
* Ara ara gelen güncellemeleri pek takip edemedim. Orjinal siteden çevirmek isteyen varsa hoş olur.


#### [[⬆]](#toc) <a name='contributors'>Çeviri İçin Katkıda Bulunanlar:</a>

* [Cem Celebi](https://github.com/occelebi)
* [Batuhan Taskaya](https://github.com/isidentical)
* [Mehmet Soylu](https://github.com/mssoylu)
* [Muhammed Sabri Yildirim](https://github.com/mhammedyildirim)
