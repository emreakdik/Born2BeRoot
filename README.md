# Sanal Makineler

### Sanal Makineler Nasil Calisir?
- Sanal makine, fiziksel bir bilgisayar veya uzak sunucu üzerinde çalışan ve bir bilgisayar için tasarlanmış bir işletim sistemini çalıştıran yazılımdır.
- Sanal makine yazılımı, fiziksel bilgisayarın özelliklerini taklit eden bir sanal donanım oluşturur ve birincil sistemden donanim odunc alir.
- Bu sanal donanım, işletim sistemi ve uygulamaların çalışması için gerekli olan tüm bilgisayar donanımı fonksiyonlarını yerine getirir.
- Bir sanal makine, birincil sisteme asla etki edemez, soyutlanmistir.

### Sanal Makineler Ne Amacla Kullanilir?
- İşletim sistemi ve uygulamaları test etmek
-  Farklı işletim sistemlerini eşzamanlı olarak kullanmak
- Geliştirme ortamları oluşturmak
- Güvenlik
- Sanal makine üzerinde veri toplamak

### Sanal Makine Kullanmanin Avantajlari
- **Fiziksel donanım gereksinimlerinin azalması:** Sanal makine yazılımının kullanımı sayesinde, bir fiziksel bilgisayar üzerinde birden fazla işletim sistemi ve uygulama çalıştırılabilir. Bu, fiziksel donanım gereksinimlerinin azalmasına neden olur ve daha az maliyetli bir çözüm sağlar.
- **Mobilite:** Sanal makine dosyalarını taşımak, fiziksel bilgisayarı taşımaktan daha kolaydır. Bu, örneğin bir işletim sistemi ve uygulamalarının farklı bilgisayarlarda çalıştırılmasını kolaylaştırır.
- **İşletim sistemi ve uygulamaların çalıştırılması için eski bilgisayarların kullanılması:** Sanal makine yazılımının kullanımı sayesinde, eski bilgisayarlar üzerinde daha yeni işletim sistemleri ve uygulamalar çalıştırılabilir. Bu, bilgisayar atıklarını azaltmaya yardımcı olur ve maliyetleri düşürür.
- **Güvenlik:** Sanal makine üzerinde çalıştırılan işletim sistemi ve uygulamalar, host bilgisayarın gerçek donanımından ayrıdır. Bu, güvenlik açısından avantaj sağlar çünkü sanal makine üzerindeki bir güvenlik açığı, host bilgisayarın gerçek donanımına etki etmez.
- **Yüksek kullanım verimliliği:** Sanal makine yazılımı, fiziksel bilgisayarın tüm özelliklerini kullanarak birden fazla işletim sistemi ve uygulamayı aynı anda çalıştırabilir. Bu, yüksek kullanım verimliliği sağlar.

|CentOS                                    |Debian                                       |
|------------------------------------------|---------------------------------------------|
|Red Hat toplulugu tarafindan gelistirilir.|Debian kullanicilari tarafindan gelistirilir.|
|Coklu mimari destegi yoktur.			   |Coklu mimari destegi vardir. 				 |
|YUM paket yoneticisini kullanir.		   |APT paket yoneticisini kullanir.			 |
|Daha cok sunucular icin kullanilir.	   |Hem sunucular icin hem de gunluk kullanilir. |
|Varsayilan paketleri azdir.			   |Varsayilan paket cesitliligi fazladir.		 |
|Ikisi de cok kararli dagitimlardir. Fakat CentOS bir adim onde gorulur.				 |

# Paket Yoneticileri
### APT
- APT (Advanced Package Tool) Debian ve diğer Debian tabanlı Linux dağıtımlarında kullanılan bir paket yöneticisidir.
- APT, Linux sistemlerinde yüklü olan uygulamaların güncellemelerini ve yeni uygulamaları yüklemek için kullanılır. 
- APT, ayrıca uygulamaların yüklenip kaldırılmasını ve bağımlılıkların yönetimini de gerçekleştirir.

```properties
apt-get update: Sistemde mevcut olan uygulamaların listesini günceller.
apt-get upgrade: Sistemde mevcut olan uygulamaları günceller.
apt-get install [package]: Belirtilen paketi yükler.
apt-get remove [package]: Belirtilen paketi kaldırır.
apt-get purge [package]: Belirtilen paketi kaldırır ve ilişkili tüm dosyaları da siler.
```
### APTITUDE 
- Debian ve Debian tabanlı Linux dağıtımlarında kullanılan bir paket yöneticisidir. 
-  APT (Advanced Package Tool) gibi çalışır ve uygulamaları yüklemek, güncellemek, kaldırmak ve bağımlılıkları yönetmek gibi işlevleri vardır. 
- APT'ye göre daha gelişmiş bir arayüze sahiptir ve daha fazla özellik sunar.
```properties
aptitude update: Sistemde mevcut olan uygulamaların listesini günceller.
aptitude upgrade: Sistemde mevcut olan uygulamaları günceller.
aptitude install [package]: Belirtilen paketi yükler.
aptitude remove [package]: Belirtilen paketi kaldırır.
aptitude purge [package]: Belirtilen paketi kaldırır ve ilişkili tüm dosyaları da siler.
```

### APT Ve APTITUDE Farklari
- **Aptitude**  işlevselliği  apt'den daha geniştir ve apt-mark ,  apt-cache  gibi diğer varyantlarının işlevlerini bütünleştirir.
- Apt kullanıcı arayüzünden yoksun olsa da, Aptitude'un salt metin ve etkileşimli bir kullanıcı arayüzü vardır.
- Aptitude, apt-get'den daha iyi bir paket yönetimine sahiptir.
- Yüklü herhangi bir paketi kaldırırken, **Aptitude** kullanılmayan paketleri otomatik olarak silerken **apt** bunu yapmaz ve ek olarak komutlara ihtiyac duyar.

# Guvenlik

### DAC Ve MAC
İsteğe bağlı erişim denetimi (DAC) altında, bir kullanıcı veya sürecin dosyalara, socketlere ve diğer kaynaklara erişip erişemeyeceği kullanıcı sahipliğine veya izinlere bakarak belirlenir.

Zorunlu erişim denetimi ise (MAC) kullanıcıların (subjects) oluşturdukları nesnelern (objects) üzerindeki denetim düzeyini kısıtlayan bir güvenlik mekanizmasıdır. İsteğe bağlı erişim denetimi kontrolünde kullanıcılar kendi dosya, dizin, vb üzerinde tam denetime sahipken, zorunlu erişim denetimi tüm dosya sistemi nesneleri için, ek etiket ya da kategori ekler. Kullanıcılar ve süreçlerin bu nesnelerle erişebilmesi için bu kategorilere uygun erişim hakları olmalıdır.	
### SELinux
Bir subject (örneğin bir uygulama) bir objecte (örneğin bir dosya) erişmeye çalıştığında çekirdekteki politika uygulama sunucusu subject ve object izinleri için öncelikle erişim vektörü önbelleğini (Access Vector Cache) kontrol eder. Eğer önbelleğe bakılarak karar verilemezse sunucu güvenlik politikalarına göre erişimin gerçekleşip gerçekleşmeyeceğini belirler. Ayrıca söylemekte fayda var SELinux DAC’ta belirlenen erişim kurallarını ezmez.

SELinux’un 3 modu vardır. Bunlar:

-   enforcing: Kaynaklara erişimin SELinux politikasına göre belirlendiği moddur.
-   permissive: Bu modda erişimler SELinux politikası zorlanmaz. Ancak erişim politikasına uymayan durumlar bir günlük dosyasına yazılır. (Redhat’te /var/log/audit/audit.log dosyasına varsayılan olarak yazılır)
-   disabled: SELinux tamamen devre dışıdır. Sadece DAC kuralları geçerlidir.

SELinux’u  _/etc/selinux/config_  dosyasını kullanarak yapılandırabilirsiniz.

`# This file controls the state of SELinux on the system.`
`SELINUX=enforcing`
`SELINUXTYPE=targeted`

### APPArmor
AppArmor açıklanabilecek en kısa açıklaması ile sisteme verilebilecek zararı sınırlandırır veya yapılan bu işlemi tamamen durdururan bir uygulamadır. Örneğin, Ubuntu’nun varsayılan yapılandırmasında kısıtlanan bir uygulama Evince PDF görüntüleyicidir. Evince, kullanıcı hesabınız olarak çalışabilir ancak yalnızca belirli eylemleri gerçekleştirebilir. Evince, yalnızca PDF belgelerini çalıştırmak ve bunlarla çalışmak için gereken minimum izinlere sahiptir. Evince’nin PDF oluşturucusunda bir güvenlik açığı keşfedilirse ve Evince’yi ele geçiren kötü amaçlı bir PDF belgesi açarsanız, AppArmor, Evince’nin verebileceği zararı sınırlar. Geleneksel Linux güvenlik modelinde Evince, erişiminiz olan her şeye erişebilir. AppArmor ile, yalnızca bir PDF görüntüleyicinin erişmesi gereken şeylere erişebilir.

### APPArmor vs SELinux

|APPArmor|SELinux|
|--------|-------|
|Dosya yoluna gore erisim kontrolu        |Dosya etiketine gore erisim kontrolu      |
|Her dagitima uygun ama esas olarak SUSE ve Ubuntu'da kullanilir. | Her dagitima uygun ama esas olarak RHEL\Fedora'da kullanilir. 
| Kurulumu ve yonetimi daha kolay. | Daha karmasik. |
| Performansi etkilemez fakat daha uzun boot suresine sebep olur. | Performansi etkilemez. |
| Koruma politikalari asla esnemez. | Koruma politikalari esnetilebilirdir.|

### UFW Nedir?
Güvenlik duvarı (firewall), bir ağın içine gelen veya ağdan çıkan trafiği kontrol etmek amacıyla kullanılan bir araçtır. Güvenlik duvarı, belirli kurallara göre trafiği izin verir veya engeller. Bu sayede, ağınızın güvenliğini artırır ve istenmeyen trafiği engeller.

UFW (Uncomplicated Firewall), işletim sistemlerinde kullanılan bir güvenlik duvarı yönetim aracıdır. UFW, kullanımı kolay ve anlaşılır bir arayüze sahiptir ve kuralları koymak için komut satırı aracılığıyla kullanılır. Örneğin, UFW kullanarak, sadece belirli IP adreslerinden gelen trafiği izin verebilir veya sadece belirli portları açarak, sadece belirli servislerin kullanılmasına izin verebilirsiniz.

# Diskler ve Bellekler

### Mantiksal Birim Ve Fiziksel Birim Arasindaki Fark Nedir?
Mantıksal birim ve fiziksel birim, bir işletim sistemi üzerinde disk alanının iki farklı yönetim şeklidir.

- Fiziksel birim, bir işletim sistemi tarafından fiziksel olarak takılı olan bir disk bölümü olarak görülür. 
- Mantıksal birim ise, işletim sistemi tarafından bir fiziksel disk bölümü olarak değil, bir dosya gibi görülebilir.

Mantıksal birimler ve fiziksel birimler, işletim sistemi üzerinde disk alanını yönetmek için kullanılır. Ancak, mantıksal birimler daha esnek bir şekilde yönetilebilir ve birden fazla fiziksel disk arasında bölümler oluşturularak, büyütülebilir veya küçültülebilir.
### LVM Nedir?
LVM, Logical Volume Manager (Mantıksal Birim Yöneticisi) olarak adlandırılır. LVM, bir işletim sistemi üzerinde disk alanını yönetmek için kullanılan bir araçtır. LVM sayesinde, diskler arasında bölümler oluşturulabilir ve bu bölümler mantıksal birimler olarak adlandırılır.

LVM, birden fazla fiziksel disk arasında bölümler oluşturarak, bu bölümleri birleştirip büyütebilir veya küçültebilir. Bu özellik sayesinde, işletim sistemi üzerinde disk alanı daha esnek bir şekilde yönetilebilir.
### lsblk Nedir?
`lsblk` Linux sistemlerinde kullanılan bir komuttur ve sistemde bulunan blok cihazlarını listelemek için kullanılır. Blok cihazı, verileri sabit boyutlu bloklarda saklayan bir depolama cihazı türüdür. Blok cihazlarının örnekleri, sabit diskler, SSD'ler ve USB sürücülerdir.
### Disk Isimlendirmeleri Nasil Oluyor?
Linux sistemlerinde, diskler ve diğer depolama cihazları sıklıkla "sd" ile başlayan kısaltmalarla adlandırılır. Örneğin, ilk sabit disk "sda" olarak adlandırılır, ikinci sabit disk "sdb" olarak adlandırılır, ve benzer şekilde devam eder.
### Disk Isminin Sonunde Neden crypt Var?
Eğer bir disk üzerinde bir şifreleme katmanı (encryption layer) kuruluysa, `lsblk` komutunun çıktısında disk isminin yanında "crypt" gibi bir etiket gösterilebilir. Bu, disk üzerindeki verilerin şifrelenmiş olduğu anlamına gelir ve bu verilerin ancak şifre çözülerek okunabileceği anlamına gelir.

Bu tür bir şifreleme katmanı, genellikle disk üzerinde verilerin güvenliğini artırmak amacıyla kurulur. Örneğin, bir kullanıcının diskini kaybettiğinde veya diski başka bir kişinin eline geçtiğinde, bu verilerin okunamamasını ve değiştirilememesiini sağlar.
### Linux Sistem Bolumleri
Linux sistemlerinde, diskler genellikle birkaç ayrı bölüme ayrılır. Bu bölümler, sistem dosyalarının depolandığı ve çalıştırıldığı yerlerdir ve her bir bölüm farklı bir amaç için kullanılır. Aşağıda bu bölümlerin genel olarak ne işe yaradıkları hakkında bilgi verilmiştir:

-   `/boot`: Bu bölüm, sistem açılışı sırasında kullanılan dosyaları saklar. Örneğin, sistem açılışı sırasında yüklenen işletim sistemi dosyaları bu bölümde bulunur.
    
-   `/root`: Bu bölüm, sistem yöneticisi (root) kullanıcısının ev dizinini (home directory) saklar. Bu dizin, root kullanıcısının dosyalarını ve ayarlarını saklar ve genellikle `/root` olarak adlandırılır.
    
-   `/swap`: Bu bölüm, sistem belleği (RAM) için ekstra depolama alanı olarak kullanılır. Eğer sistem belleği dolmuşsa ve sistemde fazla işlem yapılıyorsa, bu işlemlerin bir kısmı `/swap` bölümüne taşınır ve bu sayede sistem çalışmaya devam eder. `/swap` bölümü, genellikle disk üzerinde ayrılmış bir bölüm olarak kullanılır, ancak bazen RAM üzerinde de kullanılabilir.
    
-   `/home`: Bu bölüm, sistemdeki normal (non-root) kullanıcıların ev dizinlerini saklar. Her bir kullanıcının ev dizini, `/home/<kullanıcı adı>` şeklinde adlandırılır ve bu dizin, kullanıcının dosyalarını ve ayarlarını saklar.
    
-   `/var`: Bu bölüm, sistem çalışırken değişen (variable) dosyaları saklar. Örneğin, geçici dosyalar, günlük dosyaları ve sunucu dosyaları bu bölümde saklanır.
- `/var/log` dizini, sistemde çalışan uygulamalar ve servisler tarafından oluşturulan günlük dosyalarını saklar. Bu dosyalar, sistem çalışırken oluşan olayları, hataları ve diğer bilgileri saklar ve sistem yöneticileri tarafından incelenir. Örneğin, bir uygulamanın çalışma durumu hakkında bilgi veren `syslog` dosyası bu dizinde bulunabilir.
- `/srv` dizini, sistemde çalışan sunucu uygulamaları tarafından kullanılan dosyaları saklar. Bu dizin, genellikle sunucu uygulamalarının özel veri ve dosyalarını saklar ve bu dosyalar, genellikle sistem kullanıcıları tarafından değil, sadece sunucu uygulamaları tarafından kullanılır. Örneğin, bir web sunucusu tarafından kullanılan web sayfaları ve dosyaları `/srv/www` dizini altında saklanabilir.
- `/tmp` dizini, geçici dosyaları saklar. Bu dizin, genellikle sistemde çalışan uygulamalar tarafından oluşturulan ve kullanılan dosyaları saklar. Örneğin, bir uygulama çalışırken oluşturduğu geçici dosyalar `/tmp` dizini altında saklanabilir. Bu dosyalar, genellikle uygulamanın çalışması tamamlandıktan sonra silinir ve `/tmp` dizini temizlenir.

Bu bölümler, genellikle bir Linux sisteminde bulunur ve her bir bölüm farklı bir amaç için kullanılır. Ancak, bazı dağıtımlar veya özel kurulumlar bu bölümlerin yapısını ve kullanımını değiştirebilir. Ayrıca, bu bölümlerin tam listesi sistemden sisteme değişebilir ve ek bölümler de olabilir.
### ROM Nedir?
ROM, Read-Only Memory (Salt Okunur Bellek) anlamına gelir. ROM, bir bilgisayar veya diğer elektronik cihazda saklanan ve sadece okunabilen verileri saklar. ROM, genellikle sistem çalışırken gerekli olan önemli verileri (örneğin, BIOS veya bootloader) saklar ve bu veriler sistem açılışı sırasında yüklenir.

ROM, genellikle hafıza modülü olarak kullanılır ve bu modül, genellikle cihazın içinde bulunur. ROM, verilerin yazılmasına izin vermez ve sadece okunabilir. Bu nedenle, ROM genellikle sistem açılışı ve önemli verilerin saklanması için kullanılır.

### sr0 Nedir?
`sr0` genellikle bir CD-ROM sürücüsünün veya diğer bir optik sürücünün sistemde tanımlanmış bir adıdır. Bu ad, genellikle sistem açılışı sırasında otomatik olarak atanır ve sistemde bulunan optik sürücüleri tanımlamak için kullanılır.
`sr0` adı, genellikle `/dev` dizini altında bulunur ve bu ad altında saklanan dosyalar, sistemde bulunan optik sürücülerin verilerine erişmek için kullanılır.
### MAJ:MIN Nedir?
MAJ:MIN, bir disk bölümünün Major (Ana) ve Minor (Yardımcı) numaralarını gösterir. Bu numaralar, sistemde bulunan diskleri ve bölümlerini tanımlamak için kullanılır ve genellikle `lsblk` veya `fdisk` gibi komutlarla görüntülenir.

Major numara, bir disk sürücüsünü veya bölümünün türünü tanımlar. Örneğin, Major numarası `8` olan bir bölüm, genellikle bir disk sürücüsünün bölümüdür ve bu bölüm, genellikle sistem açılışı sırasında kullanılır. Major numarası `3` olan bir bölüm ise, genellikle bir seri port sürücüsünün bölümüdür ve bu bölüm, genellikle seri port cihazlarının verilerine erişmek için kullanılır.

Minor numara ise, bir disk sürücüsünün veya bölümünün daha ayrıntılı tanımlamasını yapar. Örneğin, Minor numarası `0` olan bir bölüm, genellikle bir disk sürücüsünün ilk bölümüdür ve Minor numarası `1` olan bir bölüm ise, genellikle ikinci bölümüdür. Bu numaralar, sistemde bulunan diskleri ve bölümlerini daha ayrıntılı olarak tanımlamak için kullanılır.

## SSH
SSH (Secure Shell), bir bilgisayar ağı üzerinde güvenli bir bağlantı oluşturmak için kullanılan bir protokoldür. SSH, genellikle bir bilgisayardan başka bir bilgisayara veya sunucuya bağlanmak için kullanılır ve bu bağlantının güvenliğini sağlar.

SSH, genellikle bir komut satırı arabirimi (CLI) kullanılarak kullanılır ve bu arabirim üzerinden bir bilgisayara veya sunucuya bağlanılır ve bu cihazlarda komutlar çalıştırılır. SSH, bir bilgisayardan başka bir bilgisayara veya sunucuya bağlanırken güvenliğini sağlar ve bu bağlantı esnasında gönderilen verilerin şifrelenmesini sağlar.
## Sudo
`sudo` (SuperUser DO) Unix benzeri işletim sistemlerinde kullanılan bir komuttur. Bu komut, kullanıcıların sistem yöneticisi yetkilerine sahip olmadıkları halde, bu yetkilere sahip olan bir kullanıcı adı ve parolası kullanarak sistemde çalıştırılmasına izin verilen komutları çalıştırmak için kullanılır.

`sudo` komutu, genellikle sistem yöneticisi tarafından yapılandırılır ve kullanıcıların hangi komutları çalıştırmalarına izin verileceği ve hangi komutları çalıştırmalarına izin verilmeyeceği belirlenir. Bu yapılandırma, genellikle `/etc/sudoers` dosyasında yapılır ve bu dosya, sistem yöneticisi tarafından düzenlenebilir.
### Hostname Nedir?
`hostname` bir bilgisayar veya sunucunun ağda tanımlanmış bir adıdır. Bu ad, genellikle bilgisayarın veya sunucunun ağa bağlandığı anda atanır ve bu ad, genellikle bilgisayarın veya sunucunun ağ üzerinde tanımlanmasını sağlar.

### DHCP Sunucusu Nedir?
DHCP sunucusu, bir ağda IP adreslerini otomatik olarak yapılandırmak için kullanılır ve bu sayede, ağda bulunan cihazlar otomatik olarak bir IP adresi alır ve bu sayede ağ üzerinde tanımlanır. DHCP sunucusu, ağ üzerinde bulunan cihazların IP adreslerini yönetir ve bu sayede, cihazlar ağ üzerinde tanımlanır ve ağ üzerinde çalışabilir.

## Crontab Nedir?
`cron` Unix benzeri işletim sistemlerinde kullanılan bir servistir. Bu servis, belirli zaman aralıklarında otomatik olarak çalıştırılmasına izin verilen komutları ve görevleri çalıştırmak için kullanılır. `cron` servisi, genellikle sistem yöneticisi tarafından yapılandırılır ve bu yapılandırma, genellikle `/etc/crontab` veya `/etc/cron.d` gibi dizinlerde bulunan dosyalarda yapılır.

`cron` servisi, genellikle sistem yöneticisi tarafından yapılandırılan zaman aralıklarında çalıştırılmasına izin verilen komutları ve görevleri çalıştırır. Bu komutlar ve görevler, genellikle sistem bakımı ve yönetimi için kullanılır ve bu komutlar ve görevler, genellikle sistem açılışı sırasında çalıştırılır. Örneğin, bir sistem yöneticisi tarafından ayarlanan bir zaman aralığında otomatik olarak bir sunucunun yedeklemesinin alınması gibi bir görev için `cron` servisi kullanılabilir.

- **crontab -u root -e:** makro ayari yapilmasini saglar. (-u user, -e edit)
- **sudo /etc/init.d/cron stop:** komutu durdurmak icin.
- **sudo /etc/init.d/cron start:** komutu baslatmak icin.
- **sudo /etc/init.d/cron start:** durumu baslatmak icin.
- **sudo /etc/init.d/cron . :** hangi komutlar kullanilabilir onu gosterir.
## TCP Nedir?
TCP, Transmission Control Protocol (İletişim Kontrol Protokolü) olarak adlandırılır. Bu protokol, internet üzerinde veri gönderimini gerçekleştirmek için kullanılır. TCP, verileri parçalara böler (bunlar "paketler" olarak adlandırılır) ve her bir paketi ayrı ayrı gönderir. Bu sayede, herhangi bir paketin kaybı durumunda sadece o paket yeniden gönderilir, diğer paketler etkilenmez. TCP ayrıca verilerin aynı sırayla ve doğru şekilde alıcıya ulaşmasını sağlar.

TCP, IP (Internet Protocol) protokolü ile birlikte kullanılır. IP, paketleri doğru yere göndermek için kullanılır, ancak gönderilen verilerin doğru şekilde alıcıya ulaşmasını ve verilerin parçalara ayrılmasını sağlamaz. Bu nedenle, TCP ve IP protokolleri birlikte kullanılır. Baglanti bilgileri (kac baglanti oldugu vb.) /proc/net/sockstat adresinde tutulur.
# Komutlar ve Aciklamalari
-   `id`: Kullanıcının kimlik bilgilerini gösterir.
-   `whoami`: Kullanıcının kim olduğunu gösterir.
-   `finger`: Kullanıcı hakkında detaylı bilgi verir.
-   `w`: Sistemde çalışan kullanıcıları ve ne yaptıklarını gösterir.
-   `last`: Kullanıcıların sisteme son giriş bilgilerini gösterir.
-   `users`: Sistemde çalışan kullanıcıların listesini gösterir.
- `getent` komutu, sistemdeki kullanıcı ve gruplar hakkında bilgi toplamak için kullanılabilir. Bu komut, `/etc/passwd`, `/etc/group` ve benzeri dosyalarda bulunan bilgileri kullanarak kullanıcı ve gruplar hakkında bilgi verir.
-------------------------
Aşağıdaki `ufw` komutlarını kullanarak güvenlik duvarını yönetebilirsiniz:

-   `ufw enable`: Güvenlik duvarını etkinleştirir.
-   `ufw disable`: Güvenlik duvarını devre dışı bırakır.
-   `ufw default deny`: Varsayılan olarak tüm bağlantıları reddeder.
-   `ufw default allow`: Varsayılan olarak tüm bağlantıları kabul eder.
-   `ufw allow [port/service]`: Belirtilen port veya hizmete izin verir.
-   `ufw deny [port/service]`: Belirtilen port veya hizmete izin vermez.
-   `ufw show`: Güvenlik duvarı kurallarını gösterir.
-----------------------------
Linux terminali üzerinde kullanıcı yönetimi için aşağıdaki komutlar kullanılabilir:

-   `useradd`: Yeni bir kullanıcı oluşturur.
-   `userdel`: Bir kullanıcıyı siler.
-   `usermod`: Bir kullanıcının bilgilerini değiştirir.
-   `passwd`: Bir kullanıcının parolasını değiştirir.
-   `chage`: Bir kullanıcının parola ömrünü değiştirir.
-   `groupadd`: Yeni bir grup oluşturur.
-   `groupdel`: Bir grubu siler.
-   `groupmod`: Bir grubun bilgilerini değiştirir.

------------------------------------------
Linux terminali üzerinden hizmetleri yönetmek için aşağıdaki komutlar kullanılabilir:

-   `systemctl`: Systemd hizmetlerini yönetir.
-   `service`: Sistemin eski hizmetlerini yönetir.
-   `chkconfig`: Sistemin eski hizmetlerini yönetir.
- -   `systemctl start [hizmet]`: Belirtilen hizmeti başlatır.
-   `systemctl stop [hizmet]`: Belirtilen hizmeti durdurur.
-   `systemctl restart [hizmet]`: Belirtilen hizmeti yeniden başlatır.
-   `systemctl status [hizmet]`: Belirtilen hizmetin durumunu gösterir.
- ---------------------------------
- **dpkg -l:** Bu komut, sistemde yüklü olan paketlerin listesini gösterir.
- **Hostnamectl:** Ana bilgisayarin adini kontrol eder.
- **hostnamectl set-hostname sunucu1:** Ana bilgisayar adını sunucu1 olarak ayarlar.
- **head -n 2 /etc/os-release:** Isletim sisteminin ismini gosteriyor.
- **/usr/sbin/aa-status:** APPArmor'un yuklu olup olmadigini gosteriyor.
- **ss -tunlp:** sanal makinenin portlarini gosterir.
- uname:	
	- **-s:** isletim sisteminin adi
	- **-n:** hostname
	- **-r:** cekirden surumu
	- **-v:** kernel versiyonu
	- **-m:** makine donanim adi
	- **-o:** isletim sisteminin yazilim adi
	- **-a:** all
- **grep:** belirli bir karakter kalibi icin bir dosya arar ve bu kalibi iceren tum satirlari goruntuler.
- **uniq:** tekrar eden satirlari gostermez.
- **sort:** dosyalarin icerigini siralar.
- **wc:** bir dosyadaki karakter sayisini sayar.
- ^ isareti bir karakter dizisinde basta eslesen karakterleri bulmak icin kullanilir.
- **free:** sistemde bulunan ram ve swap degerleri gosterilir.
	- **-m:** ciktiyi megabayt turunce gosterir.
- **awk:** tarar ve isler. (ornegin ciktiyi tarar ve sutun sutun ayirir.)
- **df:** kullanilabilir ve kullanilan disk alani kullaniminin tam bir ozetini verir.
	- **-B:** dizinlerin boyutunu gosterir fakat tek basina yeterli degildir.
		- **-Bg:** dizinin boyutunu gb cinsinde gosterir.
		- **-Bm:** dizinin boyutunu mb cinsinde gosterir.
- **top:** Calisan islemlerin gercek zamanli bir gorunumunu gosterir.
	- **-b:** toplu modda top baslatir.
	- **-n1:** yenileme sayisini belirler. Ornegin komut calistiktan sonra 1 kere yenilenir.
- **who:** Isletim sisteminde oturum acmis kullanicilari gosterir.
	- **-b:** sistemin son yeniden baslatma tarihi alinir.
- **lsblk:** tum veya belirtilen blok aygitlariyla ilgili bilgileri listeler.
- **if blok:** if[some test] then <commands> else <other commands> fi
	- -**eq:** sayisal karsilastirma yapar.
- **-echo:** karsisinda bulunan degerin ciktisini almamizi saglar.
- **ss -s:** Baglanti sayisini gosterir.
- **hostname -I:** ip adresini gosterir.
- **ip link show:** mac adresini verir.
- **journalctl:** bilgisayar gunluklerini sorgular ve goruntuler.
