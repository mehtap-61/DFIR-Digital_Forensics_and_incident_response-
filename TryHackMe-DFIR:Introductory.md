**DFIR: An Introduction**
**Görev1-Giriş**

![Giriş](https://github.com/user-attachments/assets/59390f1b-d91e-454a-9240-e0337cc6f517)

*Öğrenme Hedefleri*

Güvenlik ihlalleri ve olayları, güvenlik ekiplerinin tüm dünyada bunlardan kaçınmak için ellerinden geleni yapmalarına rağmen meydana gelmektedir.
Böyle bir senaryoda ihtiyatlı yaklaşım, hazırlıksız yakalanmamak için bir olayın gerçekleşeceği zamana hazırlanmaktır.
Bu nedenle, Dijital Adli Tıp ve Olay Müdahalesi (DFIR), Savunmacı Güvenlikte önemli bir konu haline gelmiştir. 
Bu odada, DFIR'ın bazı temel kavramlarını ele alındı ve DFIR bilgimizi genişleten tanıtıldı. 

Oda aşağıdaki konuları kapsamaktadır:
•	DFIR'a Giriş
•	DFIR alanında kullanılan bazı temel kavramlar
•	Sektörde kullanılan Olay Müdahale süreçleri
•	DFIR için kullanılan araçlardan bazıları
![1 soru_cevap](https://github.com/user-attachments/assets/5bff2303-ee4e-4157-a228-b55309950321)
 
*DFIR nedir?*
Daha önce de belirtildiği gibi DFIR, Dijital Adli Tıp ve Olay Müdahalesi anlamına gelmektedir. 
Bu alan, bir olayı araştırmak için bilgisayarlar, medya cihazları ve akıllı telefonlar gibi dijital cihazlardan adli belgelerin toplanmasını kapsar.
Bu alan, güvenlik uzmanlarının bir güvenlik olayı meydana geldiğinde bir hacker tarafından bırakılan ayak izlerini belirlemelerine, bunları bir ortamdaki tehlikenin boyutunu belirlemek için kullanmalarına ve ortamı olay meydana gelmeden önceki durumuna geri getirmelerine yardımcı olur.
*DFIR'a duyulan ihtiyaç*

DFIR güvenlik uzmanlarına çeşitli şekillerde yardımcı olur, bunlardan bazıları aşağıda özetlenmiştir:

Ağdaki hackerin faaliyetlerinin kanıtlarını bulmak ve yanlış alarmları gerçek olaylardan ayırmak.
Hackerin sağlam bir şekilde ortadan kaldırılması, böylece ağdaki dayanaklarının artık kalmaması.
Bir ihlalin kapsamını ve zaman dilimini belirleme. 
Bu, ilgili paydaşlarla iletişim kurmaya yardımcı olur.
İhlale yol açan boşlukları bulmak.
Gelecekte ihlali önlemek için nelerin değiştirilmesi gerekiyor?
Hackerin daha fazla izinsiz giriş girişimini önceden engellemek için saldırgan davranışının anlaşılması.
Hacker hakkındaki bilgilerin toplulukla paylaşılması.

*DFIR'ı kim gerçekleştirir?*

![dfır_kim](https://github.com/user-attachments/assets/cfef3981-5cdc-4c72-a4db-544fc01ec54b)

Adından da anlaşılacağı üzere, DFIR hem Dijital Adli Tıp hem de Olay Yanıtı alanlarında uzmanlık gerektirir.
Bu iki alanı bu şekilde ayırırsak, bir DFIR uzmanı olmak için aşağıdaki beceri setine ihtiyaç vardır:

*Dijital Adli Tıp*: Bu profesyoneller, dijital cihazlardaki adli eserleri veya insan faaliyeti kanıtlarını tanımlama konusunda uzmandır. 

*Olay Yanıtı*: Olay yanıtı uzmanları siber güvenlik konusunda uzmandır ve güvenlik perspektifinden ilgilenilen faaliyeti belirlemek için adli tıp bilgilerinden yararlanırlar.

*DFIR uzmanları*:  Dijital Adli Tıp ve siber güvenlik hakkında bilgi sahibidir ve hedeflerine ulaşmak için bu alanları birleştirirler. 
Dijital Adli Tıp ve Olay Müdahalesi alanları birbirlerine oldukça bağımlı oldukları için genellikle birleştirilirler. 
Olay Müdahalesi, Dijital Adli Tıptan elde edilen bilgilerden yararlanır.
Benzer şekilde, Dijital Adli Tıp hedeflerini ve kapsamını Olay Yanıtı sürecinden alır ve IR süreci adli soruşturmanın kapsamını tanımlar.

*DFIR ne anlama gelmektedir?*

**Cevap:** Digital Forensics and Incident Response(Dijital Adli Tıp ve Olay Yanıtı)

*DFIR iki alanda uzmanlık gerektirmektedir. Alanlardan biri Dijital Adli Tıp. Diğer alan nedir?*

**Cevap:** Incident Response (Olay Yanıtı)

Şimdi DFIR'ı ve neden gerekli olduğunu tanıttığımıza göre, bu görevde DFIR ile ilgili bazı temel kavramları öğrenelim.

**Görev 3:DFIR’ın temel kavramları**

**Artefaktlar:**
Artefaktlar, bir sistem üzerinde gerçekleştirilen bir faaliyete işaret eden kanıt parçalarıdır.
DFIR gerçekleştirilirken, artifaktlar saldırgan faaliyeti hakkındaki bir hipotezi veya iddiayı desteklemek için toplanır. 
Örneğin, hackerin bir sistemde kalıcılığı sağlamak için Windows kayıt defteri anahtarlarını kullandığını iddia edeceksek, iddiamızı desteklemek için söz konusu kayıt defteri anahtarını kullanabiliriz.
Bu durumda, söz konusu kayıt defteri anahtarı bir obje olarak kabul edilecektir. 
Artefakt toplama bu nedenle DFIR sürecinin önemli bir parçasıdır. 
Artefaktlar Uç Nokta veya Sunucunun dosya sisteminden, belleğinden veya ağ etkinliğinden toplanabilir.
Çoğu zaman, kurumsal ortamlar çoğunlukla Windows ve Linux İşletim Sistemlerinden oluşur.
Bu İşletim Sistemlerindeki adli eserler hakkında daha fazla bilgi edinmek için Windows Forensics 1, Windows Forensics 2 veya Linux Forensics odasına gidebilirsiniz. 
Windows sistemleri öncelikle Active Directory Etki Alanı Denetleyicileri veya MS Exchange e-posta sunucuları gibi uç noktalar ve sunucu kullanım durumları için kullanılır. 
Şirketler Linux sistemlerini öncelikle web sunucuları veya veritabanı sunucuları gibi bazı hizmetleri barındıran sunucular olarak kullanmaktadır.

*Evidence Preservation (Kanıtların Korunması):*

DFIR gerçekleştirirken, topladığımız kanıtların bütünlüğünü korumalıyız. 
Bu nedenle sektörde bazı en iyi uygulamalar belirlenmiştir. Herhangi bir adli analizin delilleri kirlettiğini unutmamalıyız.
Bu nedenle, kanıtlar önce toplanır ve yazmaya karşı korunur. Ardından, yazmaya karşı korumalı kanıtın bir kopyası analiz için kullanılır. 
Bu süreç, orijinal kanıtımızın kirlenmemesini ve analiz sırasında güvende kalmasını sağlar. 
İnceleme altındaki kopyamız bozulursa, her zaman geri dönebilir ve koruduğumuz kanıtlardan yeni bir kopya oluşturabiliriz.

*Chain of custody (Gözetim zinciri):*

Kanıtların bütünlüğünü korumanın bir diğer kritik yönü de gözetim zinciridir. 
Kanıt toplandığında, güvenli bir şekilde muhafaza edildiğinden emin olunmalıdır. 
Soruşturmayla ilgisi olmayan herhangi bir kişi delile sahip olmamalıdır, aksi takdirde delilin gözetim zinciri kirlenecektir. 
Kirlenmiş bir gözetim zinciri, verilerin bütünlüğü hakkında soru işaretleri doğurur ve çözülemeyecek bilinmeyen değişkenler ekleyerek oluşturulmakta olan davayı zayıflatır. 
Örneğin, bir sabit disk imajının, imajı alan kişiden analizi gerçekleştirecek kişiye aktarılırken, bu tür bir kanıtı kullanma yetkisi olmayan bir kişinin eline geçtiğini varsayalım.
Bu durumda, bu kişinin delili doğru bir şekilde ele alıp almadığından ve dolayısıyla kendi faaliyetleriyle delili kirletip kirletmediğinden emin olamayız.

*Order of volatility (Uçuculuk sırası):*

Dijital kanıtlar genellikle uçucudur, yani zamanında yakalanmazsa sonsuza kadar kaybolabilir.
Örneğin, bir bilgisayar sisteminin belleğindeki (RAM) veriler bilgisayar kapatıldığında kaybolacaktır.
Çünkü RAM verileri yalnızca açık kaldığı sürece saklar. 
Bazı kaynaklar diğerlerine kıyasla daha uçucudur.
Örneğin, bir sabit disk kalıcı bir depolama alanıdır ve güç kesilse bile verileri korur. Bu nedenle sabit disk RAM'den daha az uçucudur.
DFIR gerçekleştirirken, farklı kanıt kaynaklarının uçuculuk sırasını anlamak ve buna göre yakalamak ve muhafaza etmek hayati önem taşır. 
Yukarıdaki örnekte, öncelik vermediğimiz takdirde RAM'deki verileri kaybedebileceğimiz için sabit sürücüyü korumadan önce RAM'i korumamız gerekecektir.

*Timeline creation (Zaman çizelgesi oluşturma):*

Eserleri topladıktan ve bütünlüklerini koruduktan sonra, içerdikleri bilgileri tam olarak kullanabilmek için bunları anlaşılır bir şekilde sunmamız gerekir.
Etkili ve doğru analiz için bir olaylar zaman çizelgesi oluşturulmalıdır.
Bu olaylar zaman çizelgesi tüm faaliyetleri kronolojik sıraya koyar.
Bu faaliyete zaman çizelgesi oluşturma adı verilir.
Zaman çizelgesi oluşturma, soruşturmaya bir perspektif kazandırır ve olayların nasıl gerçekleştiğine dair bir hikaye oluşturmak için çeşitli kaynaklardan gelen bilgilerin harmanlanmasına yardımcı olur. 
Şimdi, zaman çizelgesi oluşturma pratiği yapmak ve ilk soruyu yanıtlamak için ekteki statik siteyi görüntüleyelim.
Bunu yapmak için, bu görevin sağ üst köşesindeki Siteyi Görüntüle düğmesine tıklayın.

![link](https://github.com/user-attachments/assets/3b6cf976-59bc-430e-861b-58c499f31183)

**RAM ve sabit disk arasından hangi depolama birimi daha uçucudur?**
**Cevap:** RAM

**Ekteki statik sitede zaman çizelgesi oluşturma alıştırmasını tamamlayın. Tamamladıktan sonra aldığınız bayrak nedir?**
**Cevap:** THM{DFIR_REPORT_DONE}

**Görev 4: DFIR Tools**
Güvenlik sektörü, DFIR sürecine yardımcı olmak için çeşitli heyecan verici araçlar geliştirmiştir. 
Bu araçlar değerli zamandan tasarruf edilmesine ve güvenlik uzmanlarının yeteneklerinin geliştirilmesine yardımcı olur. 
Şimdi bu araçlardan bazıları hakkında bilgi edinelim. 
Bu araçlar hakkında daha fazla bilgi edinmek için TryHackMe'deki bu araçların odalarına göz atabilirsiniz.

![Eric_Zimmerman_tool](https://github.com/user-attachments/assets/866491c6-a0b8-4bf9-ba62-a9d336280939)

Eric Zimmerman, Windows platformunda adli analiz gerçekleştirmeye yardımcı olmak için birkaç araç yazmış bir güvenlik araştırmacısıdır.
Bu araçlar kayıt defteri, dosya sistemi, zaman çizelgesi ve diğer birçok analize yardımcı olur. 
Bu araçlar hakkında daha fazla bilgi edinmek için, bu araçların Windows İşletim Sisteminde bulunan farklı eserlerle ilgili olarak tartışıldığı Windows Forensics 1 ve Windows Forensics 2 odalarına göz atabilirsiniz.

![KAPE](https://github.com/user-attachments/assets/b06ab482-90b2-44a9-b3e0-d1d4fbd3cbce)

Kroll Artifact Parser and Extractor (KAPE), Eric Zimmerman tarafından geliştirilen bir başka faydalı araçtır.
Bu araç, adli eserlerin toplanmasını ve ayrıştırılmasını otomatikleştirir ve olayların bir zaman çizelgesini oluşturmaya yardımcı olabilir. 
KAPE hakkında daha fazla bilgi edinmek için KAPE odasına göz atabilirsiniz.

![Autospy](https://github.com/user-attachments/assets/b466ec45-f271-4a10-95ca-4117dcaac247)

Autopsy, mobil cihazlar, sabit sürücüler ve çıkarılabilir sürücüler gibi dijital ortamlardan gelen verileri analiz etmeye yardımcı olan açık kaynaklı bir adli tıp platformudur. 
Otopsi için çeşitli eklentiler adli süreci hızlandırır ve ham veri kaynaklarından değerli bilgileri çıkarır ve sunar. 
Bu konuda daha fazla bilgi edinmek isterseniz TryHackMe'nin Otopsi odası size yardımcı olabilir.

![volality](https://github.com/user-attachments/assets/d63c66d3-6bc7-4b15-8032-d220d1877db4)

Volatility, hem Windows hem de Linux İşletim Sistemlerinden bellek yakalamaları için bellek analizi yapmaya yardımcı olan bir araçtır. 
İncelenmekte olan bir makinenin belleğinden değerli bilgilerin çıkarılmasına yardımcı olabilecek güçlü bir araçtır.
Volatility hakkında daha fazla bilgiyi Volatility odasında bulabilirsiniz.

![Redline](https://github.com/user-attachments/assets/d25f13e1-f33b-44db-acbd-91dfb6e1b75e)

Redline, FireEye tarafından geliştirilen ve ücretsiz olarak dağıtılan bir olay müdahale aracıdır. 
Bu araç bir sistemden adli veri toplayabilir ve toplanan adli bilgilere yardımcı olabilir. 
Redline hakkında daha fazla bilgiyi Redline odasında bulabilirsiniz.

![Velociprator](https://github.com/user-attachments/assets/3ca8cd2f-3caf-4fd8-93ad-de8ea5ae8079)

Velociraptor gelişmiş bir uç nokta izleme, adli tıp ve müdahale platformudur. 
Açık kaynaklıdır ancak çok güçlüdür. 
TryHackMe, hakkında daha fazla bilgi edinmeniz için bir Velociraptor odası oluşturdu.
Tüm bu araçlar DFIR gerçekleştirirken yardımcı olsa da, hedeflerimize ulaşmak için izlenen süreci anlamak çok önemlidir. 
Bir sonraki görev, Olay Müdahale sürecine ve bu süreçte Dijital Adli Bilişimden nasıl yararlanabileceğimize odaklanacaktır.

![Görev_4](https://github.com/user-attachments/assets/9d4654ac-c4cd-4995-86ae-fff82391c154)

Görev 5: Olay Müdahale süreci
Güvenlik Operasyonlarında, Dijital Adli Bilişimin öne çıkan kullanımı Olay Müdahalesi gerçekleştirmektir. 
Olay Müdahale sürecini öğreneceğiz ve Dijital Adli Bilişim'in bu görevde IR sürecine nasıl yardımcı olduğunu gözlemleyeceğiz.
Farklı kuruluşlar Olay Müdahalesi gerçekleştirmek için standartlaştırılmış yöntemler yayınlamıştır. 

NIST, SP-800-61 Incident Handling kılavuzunda aşağıdaki adımları içeren bir süreç tanımlamıştır:

•	Hazırlık
•	Tespit ve Analiz
•	Kontrol Altına Alma, Yok Etme ve Kurtarma
•	Olay Sonrası Faaliyet

Benzer şekilde SANS da bir Olay Yöneticisi el kitabı yayınlamıştır.

El kitabı adımları aşağıdaki gibi tanımlamaktadır:

•	Hazırlık
•	Tanımlama
•	Sınırlama
•	Eradikasyon
•	Kurtarma
•	Çıkarılan Dersler

SANS tarafından tanımlanan adımlar genellikle PICERL kısaltması ile özetlenerek hatırlanmaları kolaylaştırılmıştır. 
SANS ve NIST tarafından belirtilen adımların aynı olduğunu görebiliriz. 
NIST Sınırlama, Yok Etme ve Kurtarma adımlarını bir araya getirirken SANS bunları farklı adımlara ayırmaktadır. 
Olay sonrası faaliyet ve alınan dersler karşılaştırılabilirken, Tanımlama ve Tespit ve Analiz aynı etkilere sahiptir.
Şimdi iki sürecin benzer olduğunu anladığımıza göre farklı adımların ne anlama geldiğini kısaca öğrenelim.
PICERL adımlarını, kısaltma ile hatırlanması daha kolay olduğu için açıklıyoruz, ancak yukarıda açıklandığı gibi, NIST tarafından tanımlanan adımlarla aynıdır.

![NIST_adimlari](https://github.com/user-attachments/assets/23d5712d-585b-4d79-b1c5-f0168b6127c5)

**Preparation (Hazırlık):** Bir olay meydana gelmeden önce, bir olay durumunda herkesin hazır olması için hazırlık yapılması gerekir.
Hazırlık, olayları önlemek ve olaylara müdahale etmek için gerekli kişilere, süreçlere ve teknolojiye sahip olmayı içerir.
**Identification(Tanımlama):** Tanımlama aşamasında bazı göstergeler aracılığıyla bir olay tespit edilir.
Bu göstergeler daha sonra Yanlış Pozitifler için analiz edilir, belgelenir ve ilgili paydaşlara iletilir.
**Containment (Muhafaza altına alma):** Bu aşamada olay kontrol altına alınır ve etkilerinin sınırlandırılması için çaba gösterilir. 
Bu aşamanın bir parçası olacak olayın adli analizine dayalı olarak tehdidi kontrol altına almak için kısa ve uzun vadeli düzeltmeler olabilir.
**Eradication(Yok etme):** 
Ardından, tehdit ağdan ortadan kaldırılır.
Ortadan kaldırmadan önce uygun bir adli analiz yapıldığından ve tehdidin etkili bir şekilde kontrol altına alındığından emin olunmalıdır.
Örneğin, tehdit aktörünün ağa giriş noktası tıkanmazsa, tehdit etkili bir şekilde ortadan kaldırılamaz ve aktör yeniden bir yer edinebilir.
**Recovery(Geri kazanım):**
Tehdit ağdan kaldırıldıktan sonra, kesintiye uğrayan hizmetler olay meydana gelmeden önceki haline geri getirilir.
**Lessons Learned(Çıkarılan Dersler):**
Son olarak, olayın bir incelemesi yapılır, olay belgelenir ve ekibin bir dahaki sefere daha iyi hazırlanmasını sağlamak için olaydan elde edilen bulgulara dayalı adımlar atılır.

**IR sürecinin hangi aşamasında kesintiye uğrayan hizmetler olaydan önceki haliyle tekrar çevrimiçi hale getirilir?**
**Cevap:** Recovery (Geri kazanım)

**Adli analiz gerçekleştirildikten sonra tehdit, IR sürecinin hangi aşamasında ağdan çıkarılır?**
**Cevap:** Eradication (Yok etme)

**SANS sürecinde “Alınan Dersler” olarak adlandırılan adımın NIST'teki karşılığı nedir?**
**Cevap:** Post-incident Activity

**Görev 6-Conclusion(Sonuç)**
Bu oda için hepsi bu kadardı. 
Burada öğrendiklerimizi tekrarlayalım.
DFIR'ın ne olduğunu ve nerede kullanıldığını öğrendik.
Neden DFIR yapmamız gerektiğini öğrendik.
Gözetim zinciri, kanıtların korunması ve uçuculuk sırası gibi temel kavramları öğrendik.
EZ araçları, KAPE, Otopsi gibi sektörde kullanılan bazı araçlar hakkında bilgi edindik.
Olay müdahalesi için PICERL süreci
Şimdi DFIR hakkında daha fazla bilgi edinmek için bu modüldeki sonraki odalara geçebiliriz.

![görev_6](https://github.com/user-attachments/assets/2d116426-f906-4d5b-9165-d9b86490a0a8)
