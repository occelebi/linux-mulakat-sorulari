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


#### [[⬆]](#toc) <a name='general'>Genel Sorular:</a>

* Dün/geçen hafta ne öğrendin?
* Tercih ettiğin geliştirme/yönetim ortamından bahset.(OS, Editör, Browsers, Tools etc.)
* Son yaptığın Linux projesinden bahset.
* Son yaptığın en büyük hatadan bahset, bugün nasıl çözerdin? Neler öğrendin?
* Neden seni seçmeliyiz?
* Ağda DNS'in ne gibi bir rolü var?
1. DNS(Domain Name Server)'lar, domain adına karşılık gelen ip'leri tutar. client resolv.conf gibi bir program aracılığı ile bu indexden yazdığı domain'in ip sine gitmesi sağlanmış olur.
* HTTP nedir?
* HTTP proxy nedir, nasıl çalışır?
* Kısaca HTTPS'in nasıl çalıştığını açıkla.
* SMTP nedir? Mail nasıl SMTP aracılığıyla ulaştırılır?
* RAID nedir? RAID0, RAID1, RAID5, RAID10 nedir?
* Level 0 backup nedir? Incremental(artan) backup nedir?
* Linux sisteminin genel dosya sistemi hiyerarşisini açıkla.

#### [[⬆]](#toc) <a name='simple'>Basit Linux Soruları:</a>

* Admin kullanıcısının adı ve UID'si nedir?
1. admin`lik linux`da verilen erişimlerle değişsede sanırım root kullanıcısından bahsediyorsunuz. UID'si 0`dır. id komutu veya /etc/passwd' dan bakabilirsiniz.
* Bir dizin içindeki saklı dosyalar dahil bütün dosyaları nasıl listelersin?
1. ls -a ile gizli dosyaları listeleyebiliriz. Dosya yöneticisi kullanıyorsanız muhtemelen ctrl+h ile gösterecektir.
* Bir dizini ve içindekileri silen Linux komutu nedir?
1. rm -r dosyaismi
* Kullanılabilir/kullanılmış belleği nasıl görürüz? Kullanılmamış bellek Linux'te mevcut mudur?
1. free komutu ile görebiliriz. (ikinci soruyu anlamadım orjinalindede anlamadım.)
* "my konfi is the best" cümlesini dizindeki dosyalarda ve altındaki dizinlerde nasıl ararız?
1. for i in my konfi is the best ; do find . -name $i ; done 
* Uzaktaki makinaya nasıl bağlanırız veya SSH nedir?
1. Bağlantı derken komut gönderme ise SSH gayet güvenli bir yöntemdir public key`imizle bağlanabiliriz. Ama bir servise komut gönderme amacında isek API'ı varsa curl veya benzeri bir araçla yada browser ile işimize yarayan endpoint'i bularak istek atabilir bir soket programı yazabilir. Üzerinde çalıştırdığı yazılımın bir açığından faydalanarak komut gönderebiliriz.
* Bütün ortam değişkenleri nasıl görürüz ve nasıl kullanırız?
1. env komutu ile görebiliriz. $ ile yani normal tanımladığımız değişkeni çağırıyormuş gibi kullanabiliriz.
* ```ifconfig -a``` komutunu çalıştırdığımda "command not found" hatası alıyorsam problem ne olabilir?
1. komut satırı kullanırken bir komutu yazarız direk çalışır PATH env 'si hangi dizindeki dosyalar çalıştırılabilir dosyalar bunu tutar bu env'da muhtemelen /usr/sbin olmadığı için komut bulunamadı diyor. PATH env`ını günceller yada komutun path'ini girersen çalışır.
* İki kez TAB tuşuna basarsam ne olur?
1. hiç harf girmediysen birşey yapmaz harf girdiysen o harfdeki tüm komutları gösterir. eğer komutu yarım yazdıysan o hali tek bir komutu gösteriyorsa tamamlar aynı şeyi path girerkende yapar dosya ismini yarım yazarsan onu tamamlar.
* Linux sistemlerde kullanabilir disk alanını gösteren komut nedir?
1. df komutu, tanımlı alan, kullanılan alan gibi bilgileri byte cinsinden yazdığı için daha okunabilir olması bakımından -h paramentresi verilmesi uygun olur.
* DNS kayıtlarını kontrol etmek için hangi komutlar kullanılır?
1. host,dig,nslookup araçlarını kullanabilirsiniz.
* Hangi Linux komutları dosyanın aidiyetini ve izinleri değiştirir?
1. chown 
* ```chmod +x FILENAME``` komutu ne yapar?
1. user,group,other erişimlerinin hepsine çalıştırma yetkisi verir.
* 0750 izninin dosya üzerindeki etkisi nedir?
1. user okuma,yazma,çalıştırma. group okuma,çalıştırma. other yetki yok olarak yetki verir. yani dosyanın içeriğini okuyabilirsin, içinde birşeyler değiştirebilirsin ve çalıştırabilirsin user olarak.
* 0750 izninin dizin üzerindeki etkisi nedir?
1. user için dosyanın içine girme dosya dizin silme,taşıma,oluşturma gibi yetkileri vardır. group için ise dosya ismi değiştirme,silme,oluşturma gibi işlevleri yapamazsın. Bu yetkilerin dosyanın hemen altında geçerli olduğunu unutmayın.
* Erişim (login) izni vermeden nasıl kullanıcı oluşturulur?
* Bir kullanıcıya nasıl grup nasıl eklenir, silinir?
1. /etc/group dosyasından group'a karşılık gelen satıra user'ı ekle. Komutlada yapılabilir ama sistemde o komut olmayabilir veya o iş için farklı komutlar kullanılıyr olabilir bu daha garanti. 
* Bash alias ne demektir?
1. takma ad yani bir komut veya komut dizisine başka bir isim vermek istersen kullanabilirsin.
* root veya bir kullanıcının mail adresini nasıl ayarlarsın?
* CTRL-c ne yapar?
1. komuttan çıkar bir komut yürütülüyorsa buna basıp çıkabilirsin, aynı zamanda terminalde komut yazdıysan çalıştırmayacaksan silmeyede üşeniyorsan ctrl+c yap
* /etc/services dosyanın içinde ne saklanır?
* Standart çıkış ve hatayı Bash dilinde nasıl yeniden yönlendirirsin? (> /dev/null 2>&1)
* UNIX ile Linux arasındaki fark nedir?
1. unix dağıtımları ve linuxdağıtımları arasındaki farklılıklarmı kernel olarak unix ve linux`un farklılıklarındanmı bahsediyorsunuz işletim sistemi olarakmı linux dağıtımları ve linux kernel ilk unix`i örnek almıştır. Unix artık geliştirilmiyor ama unix`in açık kaynak kernel`ını bazı dağıtımların bünyesinde gelişmeye devam etmiştir. freebsd,openbsd gibi 
* Telnet ve SSH arasındaki fark nedir?
1. Birinin iletişimi şifresiz diğerinin şifrelidir. İkiside ağ üzerinden veri aktarımı içindir.
* Üç yük ortalamasını (three load averages) açıkla, neyi gösterirler?
1. belirli bir süre boyunca ortalama sistem yüküdür.

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
* ```&``` karakteri komuttan sonra gelirse nasıl etki gösterir?
1. çalıştırılan komutun o terminal`de değilde arkaplanda çalışmasını sağlar. Terminal kapatıldığında bile süreç sonlanmaz.
* ```& disown``` karakteri komuttan sonra gelirse ne etki gösterir?
1. yine arkaplanda çalışır ama terminal kapatıldığında süreç sonlanır.
* Paket filtreleme nedir, nasıl kullanılır?
* Sanal bellek (virtual memory) nedir?
* Swap nedir, ne için kullanılır?
1. belleğin yetersiz geldiği durumlarda ram olarak disk`de bir alanı kullanma olayıdır. Zorunlu değildir.
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
1. Linux dağıtımında hangi süreçlerin çalışıp çalışmayacağına karar veren kurallardır. bunlar değiştirilebilir. runlevel 0 tüm süreçleri sonlandır yani kapat demektir, runlevel 1 tek user(root) olarak sadece sistemin çalışmasına direk yardım eden süreçleri çalıştır demektir,runlevel 2 çoklu user kullanılabilir ama hâla elzem servislerin çalıştığı runlevel`dir. runlevel 3 ekstra network servislerinin çalışır, runlevel 4 normalde kullanılmaz kullanıcının ayarına bırakılmıştır. runlevel 5 ekstra kullanıcı arayüzü servisleri çalışmaktatır. Runlevel 6 yeniden başlatma modudur. runlevelde hangi servislerin çalışıp çalışmayacağı sabit değiştirilemez değildir. runlevel 3 ü runlevel 5 deki servisleri çalıştırması için düzenleyebilirim. 
* SSH port yönlendirme (forwarding) nedir?
* Yerel ve uzaktaki port yönlendirme arasındaki fark nedir?
* useradd/adduser komutlarını kullanmadan sistemi kullanıcı eklemenin adımları nelerdir?
* Özel dosyalardaki MAJOR ve MINOR numaraları ne anlama gelir?
* "filesystem is full" hatası alındığında 'df' komutu kullanabilir alan gösteriyorsa sebebi ne olabilir?
* Dosya silindikten sonra df komutunun boşalan alanı göstermemesinin sebebi ne olabilir?
1. dosyayı bir proccess kullanıyor ve bu process sonlanmamış olabilir lsof ile bakıp kill edilmesi gerekir. 
* 'ps' komutu nasıl çalışır?
1. process`leri listeler, parametre verilerek process`in bilgisi çoğaltılabilir parametre verilmezse açık olan terminal`de çalışan process`leri listeler.
* Ölen yavru sürecin onu bekleyen ebeveyn süreci yoksa ne olur? Bu neden kötüdür?
1. zombi process olur, aslında bir zararı yoktur çok az miktarda ram kullanır ama linux sisteminde PID numarası sınırsız değildir bir sebebden dolayı hızla biriken zombie process`ler varsa pid havuzunu bitirir veni bir process oluşamaz artık.
* Bir sürecin tüm süreçlerini kısaca açıkla.
* Hangi sürecin hangi portu dinlediği nasıl öğrenilir?
1. process`in bir port kullandığını biliyosak öğrenmek istiyorsak pid numarasını alıp netstat -tulpn | grep pid_numarası şeklinde arayıp portu öğrenebiliriz. tam tersi bir durum varsa port numarasını yazarak ara. lsof da kullanabiliri lsof -i :portNumber veya /proc/pid/net/nf_conntrack`dan bakın bu araçlar yoksa.
* Zombie süreç nedir ve ne sebep olur?
1. childprocess`in parentprocess`i ölürse childprocess zombie process olur.
* Bir bash scripti çalışırken aynı anda hem terminale çıktı versin hem de dosyaya yazılsın istiyorsan ne yapmalıyız?
* echo "1" > /proc/sys/net/ipv4/ip_forward komutu ne yapar?
* https://foo.example.com sitesi için geçerli sertifika oluşturup yüklemenin adımlarını kısaca açıkla.
1. certbot`un desteklediği bir sunucu yazılımı indir,certbot ile sertifika oluştur sunucu yazılımını konfügre et 443 portunu firewall`dan izin ver. sunucu yazılımını proxy olarak kullanıyosan çok birşey değişmiyor. 
* Birkaç HTTPS sanal host aynı IP'yi paylaşabilir mi?
1. Ne türde bir paylaşım DNS ile farklı hostlardaki servislere erişimden bahsediyorsanız sunucu yazılımını proxy olarak ayarlayıp DNS firmasındada proxied olarak servisin ip ve port`unu bir DNS`e atayabilirsiniz.
* Wildcard sertifika nedir?
* Hangi Linux dosya tiplerini biliyorsun?
1. binary,static link library,dynamic link library,shell dosyaları,
* Süreç (process) ile thread arasındaki fark nedir? Fork sistem çağrısından sonra ebeveyn ve yavru süreçler arasındaki fark nasıl olur?
* Fork ve exec arasındaki fark nedir?
* "nohup" ne için kullanılır?
1. ssh`ı kapattıktan sonrada komutun devam etmesi için kullanıyorum nohup komut &
* Aşağıdaki iki komutun farkı nedir?
1. 2 komutta env belirlemek için kullanılır ama 1. tanım sadece oluşturulduğu session`da geçerlidir. 2. tanım o session`ın alt session`larındada geçerlidir.
* ```myvar=hello```
* ```export myvar=hello```
* Yerel ntp.conf dosyasında kaç tane NTP sunucusu bulundururdun?
* ```ntpq -p``` komutunun çıktısında 'reach' şutunu ne anlama gelir?
* 100-1000 sunucunu arasındaki bir sayıdaki sunucunun kernel güncellemesini nasıl yapardın?
1. sunucular donanım olarak birbirerinin aynı ise en güncel kernel'ı donanıma uygun config ederek derlerim sunucuların birini cluster'ından güvenli biçimde ayırır güncellerim bir sorun oluşmadı ise kernel`ı sunucuların linux dağıtımına göre paketleyip sunucuları kademe kademe cluster'ından güvenli şekilde ayırarak güncellerim ve geri eklerim. Tabi altyapı mimarisine göre işler değişir storage kullanılmıyorsa çok büyük boyutlu veri kullanan servislerin sunucularını gücellemek sorun olabilir bu verilerin taşınması gerekir ama gerçek zamanlı veri yazılıyorsa db ise hiç hizmet kesintisi olmadan yapabilmek için epey düşünmek gerekir. altyapı mimarisine bağlı bu birazda
* SCSI dışkın, Host, Channel, ID, LUN değerlerini nasıl görürsün?
* Bir sürecin bellek kullanımını nasıl kısıtlarsın?
1. prlimit ile kısıtlayabilirim.
* Bash quick substitution/caret replace(^x^y) nedir?
* Farklı kabuk (shell) çeşitleri biliyor musun? Evetse, kullanma imkanın oldu mu?
1. zsh,csh,ksh,ash,sh,bash var olduğunu bildiğim shell`ler, ash,sh ve tabiki bash dışında kullanmadım.
* Tarpipe nedir? (ya da hard linkler ve özel dosyalar dahil olmak üzere birşeyi bir sunucudan diğerine komple olarak nasıl kopyalarsın?)


#### [[⬆]](#toc) <a name='hard'>Zor Linux soruları:</a>

* Tünel nedir, HTTP Proxy'i nasıl bypass edersin?
* IDS ve IPS arasındaki fark nedir?
* Genelde ne tür kısayolları kullanılırsın?
* Linux Standard Base nedir?
* Atomik operasyon nedir?
* Yeni yapılandırdığın HTTP sunucusu makina yeniden başlatıldıktan sonra çalışmıyorsa ne yaparsın?
* ~/.ssh/authorized_keys dosyasında ne tür anahtarlar tutulur ve ne için kullanılır?
1. ssh anahtarlı erişim için gereklidir ssh-keygen ile oluşturduğumuz public private key`lerden public olanını buraya koyarız bağlanacağımız makineye private key`i bağlanırken kullanırız.
* Public SSH anahtarımı authorized_keys dosyasına ekledim ama hala şifre girmem gerekiyor, sorun nerde olabilir?
1. dosya erişimlerinde sorun olabilir .ssh dosyası 700 authorized_keys dosyası 644 erişim verip tekrar dene dosya ismini kontrol et.
* RPM, DEB veya Solaris paketi oluşturdun mu hiç?
1. hayır 
* ```:(){ :|:& };:``` komutu ne işe yarar?
1. çatal bombası(fork bomb) sonsuz bir döngüde kendini çoğaltır. bir süre sonra sistem bunla başa çıkamaz ve çöker tavşan virüsüde denir.
* Linux sinyalini script aracılığıyla nasıl yakalarsın?
* SIGKILL sinyali yakalanabilir mi?
* Linux çekirdiği OOM killer sürecini başlattığında ne olur, hangi süreci ilk durduracağını nasıl seçer?
* Linux boot sürecini makinaya enerji vermekten promptu alana kadar olabildiğince detaylı anlat.
* Chroot jail nedir?
* Umount komutu dizinin meşgul olduğunu söylüyorsa dizini alıkoyan sürecin PID'sini nasıl buluruz?
* LD_PRELOAD nedir, ne zaman kullanılır?
* Bir ikili (binary) dosya çalıştırdın ama hiç birşey olmadı, nasıl debug edilir?
1. strace ile çalıştırırı
* Cgroup nedir? Ne gibi bir durumda kullanılırlar?


#### [[⬆]](#toc) <a name='expert'>Uzman Linux Soruları:</a>

* Çalışan bir süreç socketi okurken ```EAGAIN: Resource temporarily unavaılable``` hatası alıyor. Süreci durdurmadan socket veya file descriptoru nasıl kapatırsın?


#### [[⬆]](#toc) <a name='network'>Ağ Soruları:</a>

* Localhost nedir? Neden ```ping localhost``` komutu hata verir?
1. localhost ağda yine kendisini işaret eden bir adresdir. Eğer bilgisayarımızda bir port`a yayın yapan bir adres varsa localhost ile port üzerinde servisi kullanabiliriz. bu adres ile hem makine kendi servislerine kendi erişebilir hemde bazı servisler network üzerinden birbirleri ile iletişim kurarken kullanabilirler,varsayılan olarak hosts dosyasıda 127.0.0.1 adresini işaret ettiği için hata vermez aslında.
* "ping" & "traceroute" komutu arasında benzerlik nedir? Traceroute hopları nasıl bulur?
1. ikiside bir makine ağa bağlımı kontrol eder teknik olarak,ping sadece hedef makineye hedef bırakırken paketin ulaştığını doğrularken, traceroute hedef makineye ulaşana kadar her makineye paket bırakır ve listeler.
* Bütün port ve socket bağlantılarını gösteren komut nedir?
1. netstat -tulpa, bu komut net-tools paketindedir.
* 300.168.0.123 geçerli bir IPv4 adresi midir?
1. hayır max 255 olmalıdır 1 oktet`de 
* Hangi IP aralıkları/altağları "private" veya "non-routable" (RFC 1918) kategorisine girer?
* VLAN nedir?
* ARP nedir ve ne için kullanılır?
* TCP ve UDP arasındaki fark nedir?
* Varsayılan gateway ne için kullanılır?
* Yönlendirme tablosunu gösteren komut nedir?
* Bir TCP bağlantısı ağda 4 farklı eşsiz şey ile tanımlanır. Bunlar nedir?
* İstemci web tarayıcısı ile web sunucusuna bağlandığında bağlantının kaynak ve hedef portu ne olur?
* Özel bir arayüze IPv6 adres nasıl eklenir?
* Eth0 arayüzüne IPv4 ve IPv6 adresine ekledikten sonra v4 adresine gönderilen ping çalışıyor fakat v6 adresine gönderilen pingin sonucu ```sendmsg: operation not permitted``` hatası alınıyorsa problem ne olabilir?
* SNAT nedir ne için kullanılır? 
* SSH tünelinden gelen bütün bağlantı paketlerini DROP eden bir Linux sistemine SSH ile nasıl bağlanırsınız? 
* DDoS'u durdurmak için en yaparsın?
* IP paketinin içeriğini nasıl görürsün?
* IPoAC nedir? (RFC 1149)


#### [[⬆]](#toc) <a name='mysql'>MySQL Soruları:</a>

* Kullanıcı nasıl oluşturulur?
* Kullanıcıya nasıl yetki verilir?
* "left" ve "right" join arasındaki fark nedir?
* InnoDB ve MyISAM arasındaki farkı kısaca açıklar mısın?
* Basit bir master/slave cluster kurmak için hangi adımlar gereklidir?
* MySQL'i kurduktan sonra neden "mysql_secure_installation" çalıstırılmalıdır? 
* Hangi işlerin çalıştığını nasıl görülür?
* 19 Ocak 2038 tarihinde ne olacak?
1. 1970'den beri bilgisayarlarda bulunan saatler saniyeyide tutar ve tek tek artar,2038'de 32 bit integer bir değerin tutabileceği max unsigned integer değerine ulaşacak ve artamayacak olay bu 32 bir bilgisayarlar artık saat'i gösteremeyecek, şuanki programlama pratikleriyle aşılabilecek bir sorun ama zaten 2038 yılında 32 bit bilgisayar kalmaz muhtemelen kalsa bile üreticiler yazılım güncellemesi vermez :). Ama o tarihte bunu düzelten kişilerin youtube videolarını görebiliriz. Neden saniyeyi tutuyor kısmında çok bir bilgim yok sadece secure bağlantılarda ve ssl-tls'de kullanıldığını biliyorum. Aklıma birşey geldi, ntp kullanabiliriz sistemde bios için zaman ayarı her zaman için çok önemli değil zaten. :p


#### [[⬆]](#toc) <a name='devop'>DevOps Soruları:</a>

* Bir script oluştururkenki çalışma akışını (workflow) açıklar mısın?
1. soruyu yanlış anlamış olabirim ama, bir dosya oluştur script dili neyse uzantısını yaz yazmayadabilirsin sadece ismini yaz. içine git yazılan kodun nerede yorumlanacağını seçmek için #!/path/to/interpreter yaz. alt satırlara geç script`i yazmaya devam et.
* GIT nedir?
1. versiyon kontrol sistemi yani kodundaki gelişmeleri eklemeleri görebildiğin sürümlere, kodundaki geliştirmeleri kayıt altına alabildiğin hatta geliştirmelere ne yaptığını yazabildiğin birşey.
* Dinamik ya da statik olarak bağlı dosya ne anlam ifade eder?
* "configure && make && make install" komutu ne işe yarar?
1. makefile oluşturur && derler && sisteme kurar.
* puppet/chef/ansible neden kullanılır?
* nagios/zenoss/newrelic ne içindir?
* Konteyner ile VM (sanal makina) arasındaki fark nedir?
1. Temel fark konteyner'da kernel`a ihtiyaç duymaması, vm'de ihtiyaç duyulması
* Yeni bir postgres kullanıcısı nasıl oluşturulur?
* Sanal IP nedir? Cluster nedir?
* Bir dosyadaki tüm yazdırılabilir karakterler nasıl yazdırılır?
* Paylaşılan kütüphane bağımlılıkları (shared library dependicies) nasıl bulunur
1. ldd dosyaadı.so
* Automake ve Autoconf nedir?
* ./configure komutu ```libfoobar is missing on your system``` hatası veriyorsa, problem ne olabilir nasıl çözülür?
1. configure dosyasının çalıştırılması için libfoobar bağımlılığında yüklenmesi gerekir onu yüklerim.
* Script veya derlenmiş programların avantajları ve dezavantajları nelerdir?
1. derlenmiş dosyanın boyutu daha az,daha hızlı çalışır ve bağımlılığı azdır. Script`ler kolay yazılır, kodları okuyabilirsiniz.
* Devamlı teslim (continuous delivery) ve DevOps arasındaki bağlantı nedir?
* Sistemin devamlı integrasyon (continous integration) ve devamlı canlıya alma (continous deployment) süreçlerinde önemli noktalar nelerdir?


#### [[⬆]](#toc) <a name='fun'>Eğlenceli Sorular:</a>

* Dikkatsiz bir sistem yöneticisi şu komutu çalıştırdıysa: ```chmod 444 /bin/chmod ``` - nasıl düzeltirdin?
1. chmod`u yeniden derler taşrdım veya derlenmiş paketten yeniden kurardım
* root şifresini kaybettin, bu durumda ne yapılabilir?
1. sunucuda root şifresini kaybetme gibi bir olay yaşamam muhtemelen ama kişisel bilgisayarımda unutabilirim. Eğer grub`u beklemeden geç şeklinde ayarladıysam mecburen live bir linux ile sisteme chroot ile girerek değiştirim. grub gözüküyorsa kernel parametresi olarak init=/bin/bash girerim ve boot ederim root kullanıcısına disklere ro olarak bağlanmış düşerim / dizinin rw olarak bağlarım root şifrsini yenilerim. (mount -o remount,rw /)
* Uzaktaki bir sunucuyu yeniden başlattım ama 10 dakika geçmesine rağmen hala SSH ile sisteme bağlanılmıyorsa problem ne olabilir?
1. yapılan bir network ayarı(ip,netmask) yanlış olabilir ping atmayı denerim cevap veriyorsa firewall kapalı ise önceden boot sırasında açılmış olabilir firewall yüzündenmi açılırken bişey mount edilememiş olabilir. bir servis patlamış olabilir ama o 10 dakika bekletmez. eğer ilo,idrac,ipmi gibi birşey kullanıyosa monitöre bakardım duruma göre ne yapacağıma karar verirdim. En önemlisi böyle durumlar yaşamamak için sistem açıkken herşeyi kontrol ederdim. 
* Issız bir adaya düşsen yanına alacağın 5 Linux komutu nedir?
1. bash,vim,nc,gcc,man
* Rastgele bir makinaya denk geldin, ilk olarak çalıştıracağın komut ne olurdu?
1. ls
* SSH protokolü farklı şekillerde nasıl kullanılabilir?
1. dosya aktarımı için
* Çalışan bir script yanlışlıkla sildin, nasıl geri getirirsin?
1. cat /proc/script_pid/fd/255 > ~/$(cat /proc/script_pid/comm) 

#### [[⬆]](#toc) <a name='demo'>Demo Zamanı:</a>

* test.tar.gz dosyasını man sayfalarına ya da Google'a bakmadan nasıl açarsın?
* testdir dizininden bütün "*.pyc" dosyalarını nasıl silinir?
1. rm testdir/*.pyc
* "my konfu is the best" içeriği bütün *.py dosyalarında nasıl aranır?
1. bunların hepsi aynı dosyanın içinde ise find . -name "*.py"
* Bütün *.txt dosyalarındaki her "my konfu is the best" metinini "I'm a Linux jedi master" ile değiştir.
1. find . -name "*.txt" -exec echo "I'm a Linux jedi master" > {} \;
* IP adresi X.X.X.X olan makinanın 443 portunun erişilir olduğu nasıl kontrol edilir?
1. curl X.X.X.X:443
* Telnet ile http://myinternal.webserver.local/test.html sayfasını nasıl indirilir? 
* Bir mail istemci olmadan komut satırı ile bir mail nasıl yollanılır?
* python/perl/bash/pseudo dillerinde ```get_prim``` methodu nasıl yazılır?
* Son 30 gün içerisinde erişilmiş bütün dosyalar nasıl bulunur?
* ```(date ; ps -ef | awk '{print $1}' | sort | uniq | wc -l ) >> Activity.log``` komutunun işlevi nedir?
* İki dizin arasındaki bütün farkları listeyen scripti yaz.
1. diff dizin1 dizin2
* ```<TIME> : [MESSAGE] : [ERROR_NO] - Human readable text``` formatındaki bir log dosyasındaki her saat veya belirli bir saatte oluşan belirli bir hata nasıl gösterilir?


#### [[⬆]](#toc) <a name='todo'>Yapılacaklar:</a>

* Mülakat soruları diye açıldı ama soruların cevapları da fena olmaz gibi geldi
* Gözden kaçan yazım hatalarına da açığım tabii :)
* Ara ara gelen güncellemeleri pek takip edemedim. Orjinal siteden çevirmek isteyen varsa hoş olur.
