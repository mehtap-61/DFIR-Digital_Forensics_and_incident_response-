**AMCACHE.HVE**

Windows işletim sistemleri, farklı dağıtımlar arasındaki program uyumluluğunu desteklemek için oluşturulmuştur. 
Bir örnekle açıklamak gerekirse bir program Windows’un tüm dağıtımı ile uyumlu olmamasıdır.
Windows sistem dosyası olan Amcache.hve dosyaları genel yapısı, registry.hive dosyasıdır.
Windows, sisteme yüklenen bir program hakkında, programın çalışma yolu, SHA1 hash değeri, program yükleme, silinme gibi zaman damgası bilgileri içerisine kaydetmektedir. 
Diğer bir özellik ise sistem içerisin de silinen dosyaların amcache.hve dosyasından silinmemesidir.

Amcache.hve dosyası “%SystemDrive%\Windows\AppCompat\Programs\Amcache.hve” dizininde bulunur.

AMCACHE.HVE ANALİZİ NASIL YAPILIR?

Amcache.hve dosyasını analiz etmeden önce bu dosyayı elde etmemiz gerekmektedir.
Amcache.hve dosyası sistem dosyası olduğundan Windows tarafından kopyalanmasına ve silinmesine izin verilmemektedir.
Dosyanın bir kopyasını alabilmek için Raw Copy, KAPE, FTK gibi toollar kullanarak elde edilebilir.
