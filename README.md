Linux Sistem Yöneticisi/DevOps Mülakat Soruları
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


####[[⬆]](#toc) <a name='general'>Genel Sorular:</a>

* Dün/geçen hafta ne öğrendin ?
* Tercih ettiğin geliştirme/yönetim ortamından bahset.(OS, Editör, Browsers, Tools etc.)
* En son yaptığın linux projesinden bahset.
* En son yaptığın en büyük hatadan bahset, bugün nasıl çözerdin ? Neler öğrendin ?
* Neden seni seçmeliyiz ?
* Ağda DNS'in ne gibi bir rolü var ?
* HTTP nedir ?
* HTTP proxy nedir, nasıl çalışır ?
* Kısaca HTTPS'in nasıl çalıştığını açıkla.
* SMTP nedir ? Mail nasıl SMTP aracılığıyla ulaştırılır ?
* RAID nedir ? RAID0, RAID1, RAID5, RAID10 nedir ?
* level 0 backup nedir ? Incremental(artan) backup nedir ?
* Linux sisteminin genel dosya sistemi hiyerarşisini açıkla.


####[[⬆]](#toc) <a name='simple'>Basit Linux Soruları:</a>

* Admin kullanıcısının adı ve UID'si nedir ?
* Bir dizin içindeki saklı dosyalar dahil bütün dosyaları nasıl listelersin ?
* Bir dizini ve içindekileri silen Linux komutu nedir ?
* Kullanılabilir/kullanılmış belleği nasıl görürüz ? Kullanılmamış bellek Lınux'te mevcut mudur ?
* "my konfi is the best" cümlesini dizindeki dosyalarda ve altındaki dizinlerde nasıl ararız ?
* Uzaktaki makinaya nasıl bağlanırız veya SSH nedir ?
* Bütün ortam değişkenleri nasıl görürüz ve nasıl kullanırız ?
* ```ifconfig -a``` komutunu çalıştırdığımda "command not found" hatası alıyorsam problem ne olabilir ?
* İki kez TAB tuşuna basarsam ne olur ?
* Linux sistemlerde kullanabilir disk alanını gösteren komut nedir ?
* DNS kayıtlarını kontrol etmek için hangi komutlar kullanılır ?
* Hangi Linux komutları dosyanın aidiyetini ve izinleri değiştirir ?
* ```chmod +x FILENAME``` komutu ne yapar ?
* 0750 izninin dosya üzerinde etkisi nedir ?
* 0750 izninin dizin üzerinde etkisi nedir ?
* Erişim(login) izni vermeden nasıl kullanıcı oluşturulur ?
* Bir kullanıcıya nasıl grup nasıl eklenir, silinir ?
* Bash alias ne demektir ?
* root veya bir kullanıcının mail adresini nasıl ayarlarsın ?
* CTRL-c ne yapar ?
* /etc/services dosyanın içinde ne saklanır ?
* Standart çıkış ve hatayı bash dilinde nasıl yeniden yönlendirirsin ? (> /dev/null 2>&1)
* UNIX ile Linux arasındaki fark nedir ?
* Telnet ve SSH arasındaki fark nedir ?
* Üç yük ortamasını(three load averages) açıkla, neyi gösterirler ?


####[[⬆]](#toc) <a name='medium'>Orta seviye Linux Soruları:</a>

* Aşağıdaki komutlar ne işe yarar, nasıl kullanılır ?
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
* ```&``` karakteri komuttan sonra gelirse nasıl etki gösterir ?
* ```& disown``` karakteri komuttan sonra gelirse ne etki gösterir ?
* Paket filtreleme nedir, nasıl kullanılır ?
* Sanal bellek(virtual memory) nedir ?
* Swap nedir, ne için kullanılır ?
* A, NS, PTR, CNAME, MX kayıtları ne anlama gelir ?
* Bilinen başka RR(resource record) var mı, nasıl kullanılırlar ?
* Split-Horizon DNS nedir ?
* Sticky bit nedir ?
* Immutable bitin dosya üzerindeki etkisi nedir ?
* Hardlink ve sembolik lınkin arasındaki fark nedir ? Bunların kaynağını silinirse her iki durum içinde ne olur ?
* Inode nedir ve ne tür bilgiler tutar ?
* Dosya sistemi kontrolü sıradaki yeniden başlatma sürecinde nasıl zorlanır ?
* SNMP nedir ne için kullanılır ?
* runlevel nedir nasıl görülür ?
* SSH port yönlendirme(forwarding) nedir ?
* Yerel ve uzaktaki port yönlendirme arasındaki fark nedir ?
* useradd/adduser komutlarını kullanmadan sistemi kullanıcı eklemenin adımları nelerdir ?
* Özel dosyalardaki MAJOR ve MINOR numaraları ne anlama gelir ?
* "filesystem is full" hatası alındığında 'df' komutu kullanabilir alan gösteriyorsa sebebi ne olabilir ?
* Dosya silindikten sonra df komutunun boşalan alanı göstermemesinin sebebi ne olabilir ?
* 'ps' komutu nasıl çalışır ?
* Ölen yavru sürecin onu bekleyen ebeveyn süreci yoksa ne olur ? Bu neden kötüdür ?
* Bir sürecin tüm süreçlerini kısaca açıkla.
* Hangi sürecin hangi portu dinlediği nasıl öğrenilir ?
* Zombie süreç nedir ve ne sebep olur ?
* Bir bash scripti çalışırken aynı anda hem terminale çıktı versin hem de dosyaya yazılsın istiyorsan ne yapmalıyız ?
* echo "1" > /proc/sys/net/ipv4/ip_forward komutu ne yapar ?
* https://foo.example.com sitesi için geçerli sertifika oluşturup yüklemenin adımlarını kısaca açıkla.
* Birkaç HTTPS sanal host aynı IP'yi paylaşabilir mi ?
* Wildcard sertifika nedir ?
* Hangi Linux dosya tiplerini biliyorsun ?
* Süreç(process) ile thread arasındaki fark nedir ? Fork sistem çağrısından sonra ebeveyn ve yavru süreçler arasındaki fark nasıl olur ?
* Fork ve exec arasındaki fark nedir ?
* "nohup" ne için kullanılır ?
* Aşağıdaki iki komutun farkı nedir ?
* ```myvar=hello```
* ```export myvar=hello```
* Yerel ntp.conf dosyasında kaç tane NTP sunucusu bulundururdun ?
* ```ntpq -p``` komutunun çıktısında 'reach' şutunu ne anlama gelir ?
* 100-1000 sunucunu arasındaki bir sayıdaki sunucunun kernel güncellemesini nasıl yapardın ?
* SCSI dışkın, Host, Channel, ID, LUN değerlerini nasıl görürsün ?
* Bir sürecin bellek kullanımını nasıl kısıtlarsın ?


####[[⬆]](#toc) <a name='hard'>Zor linux soruları:</a>

* Tünel nedir, http proxy'i nasıl bypass edersin ?
* İDS ve İPS arasındaki fark nedir ?
* Ne tür kısayolları genelde kullanılırsın ?
* Linux Standard Base nedir ?
* Atomik operasyon nedir ?
* Yeni yapılandırdığın http sunucusu yeniden makina yeniden başlatıldıktan sonra çalışmıyorsa ne yaparsın ?
* ~/.ssh/authorized_keys dosyasında ne tür anahtarlar tutulur ve ne için kullanılır ?
* Public ssh anahtarımı authorized_keys dosyasına ekledim ama hala şifre girmem gerekiyor, sorun nerde olabilir ?
* RPM, DEB veya solaris paketi oluşturdun mu hiç ?
* ```:(){ :|:& };:``` komutu ne işe yarar ?
* Linux sinyalini script aracılığıyla nasıl yakalarsın ?
* SIGKILL sinyali yakalanabilir mi ?
* Linux çekirdiği OOM killer sürecini başlattığında ne olur, hangi süreci ilk durduracağını nasıl seçer ?
* Linux boot sürecini makinaya enerji vermekten promtu alana kadar olabildiğince detaylı anlat.
* Chroot jail nedir ?
* umount komutu dizinin meşgul olduğunu söylüyorsa dizini alıkoyan sürecin PID'sini nasıl buluruz ?
* LD_PRELOAD nedir, ne zaman kullanılır ?
* Bir ikili(binary) dosya çalıştırdın ama hiç birşey olmadı, nasıl debug edilir ?
* cgroup nedir ? Ne gibi bir durumda kullanılırlar ?


####[[⬆]](#toc) <a name='expert'>Uzman Linux Soruları:</a>


* Çalışan bir süreç soketi okurken ```EAGAIN: Resource temporarily unavaılable``` hatası alıyor. Süreci durdurmadan soket veya dosya descriptoru nasıl kapatırsın ?


####[[⬆]](#toc) <a name='network'>Ağ Soruları:</a>

* localhost nedir ? Neden ```ping localhost``` komutu hata verir ?
* "ping" & "traceroute" komutu arasında benzerlik nedir ? traceroute hopları nasıl bulur ?
* Bütün port ve soket bağlantılarını gösteren komut nedir ?
* 300.168.0.123 geçerli bir IPv4 adresi midir ?
* Hangi IP aralıkları/altağları "private" veya "non-routable" (RFC 1918) kategorisine girer ?
* VLAN nedir ?
* ARP nedir ve ne için kullanılır ?
* TCP ve UDP arasındaki fark nedir ?
* Varsayılan gateway ne için kullanılır ?
* Yönlendirme tablosunu gösteren komut nedir ?
* Bir TCP bağlantısı ağda 4 farklı eşsiz şey ile tanımlanır. Bunlar nedir ?
* İstemci web tarayıcısı ile web sunucusuna bağlandığında bağlantının kaynak ve hedef portu ne olur ?
* Özel bir arayüze İPv6 adres nasıl eklenir ?
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

* test.tar.gz dosyasını man sayfalarına ya da google'a bakmadan nasıl açarsın ?
* testdir dizininden bütün "*.pyc" dosyalarını nasıl silinir ?
* "my konfu is the best" içeriği bütün *.py dosyalarında nasıl aranır ?
* Bütün *.txt dosyalarındaki her "my konfu is the best" metinini "I'm a linux jedi master" ile değiştir.
* IP adresi X.X.X.X olan makinanın 443 portunun erişilir olduğu nasıl kontrol edilir ?
* Telnet ile http://myinternal.webserver.local/test.html sayfasını nasıl indirilir ? 
* Bir mail istemci olmadan komut satırı ile bir mail nasıl yollanılır ?
* python/perl/bash/pseudo dillerinde ```get_prim``` methodu nasıl yazılır ?
* Son 30 gün içerisinde erişilmiş bütün dosyalar nasıl bulunur ?
* ```(date ; ps -ef | awk ‘{print $1}’ | sort | uniq | wc -l ) >> Activity.log``` komutunu acikla.
* İki dizin arasındaki bütün farkları listeyen scripti yaz.
* ```<TIME> : [MESSAGE] : [ERROR_NO] - Human readable text``` formatındaki bir log dosyasındaki her saat veya belirli bir saatte oluşan belirli bir hatayı nasıl gösterirsin ?


####[[⬆]](#toc) <a name='todo'>Yapılacaklar:</a>

* Mülakat soruları diye açıldı ama soruların cevapları da fena olmaz gibi geldi
