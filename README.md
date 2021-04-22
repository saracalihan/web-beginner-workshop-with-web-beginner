# web-beginner-workshop-with-web-beginner
<img width="600" src="images/background.png">

***MavDurak-IO*** bünyesinde yapılan "***Web Beginner Workshop with Web Beginner***" adlı etkinliğin sunum ve kodları

## İçindekiler
+ [İnternetin Tarihi](#i̇nternetin-tarihi)
+ [Temel kavramlar ve Web'in Çalışma Mantığı](#temel-kavramlar-ve-webin-çalışma-mantığı)
  + [IP](#ipinternet-protocol)
  + [MAC](#mac-adresimedia-access-control)
  + [TCP](#tcptransmission-control-protocol)
  + [DNS](#dnsdomain-name-system)
  + [Server](#server)
  + [ISP](#ispinternet-service-provider-i̇ss--i̇nternet-servis-sağlayıcısı)
  + [IAN](#ianinternet-area-network)
  + [Hyper Text](#hypertexthiper-metin)
  + [HTTP](#httphypertext-transfer-protocol)
  + [Temel Çalışma Mantığı](#temel-çalışma-mantığı)
+ [Lisans](#lisans) 
  

## İnternetin Tarihi

<img width="400" src="https://i.pinimg.com/originals/7c/0a/e3/7c0ae333fa4c4428bf67fa14382924d3.png">

İnternetin tarihi,  1950'lerde bilgisayarların gelişmesi ile başlar. Paket ağlarının ilk tasarımları ABD, İngiltere ve Fransa'daki çeşitli laboratuvarlarda şekillenmiştir. 

60'ların başında ABD Savunma Bakanlığı tarafından desteklenen ağ çalışmalarından birisi, İnternet Protokolü'nü (**IP**) kullanan ilk ağ olan **ARPANET**'tir.

ARPANET çerçevesinde ilk bağlantı 1969 yılında yapıldı. Ana bilgisayarlar arası bağlantılar ile internetin ilk adımı atılmış oldu. ARPANET ilk başlarda 4 merkezle yapıldı yani 4 merkezdeki bilgisayarlar arasında ilk bağlantı kuruldu. Bu merkezler University of California at LA, Stanford Research Institute, University of Utah ve University at Santa Barbara oldu

<img width="400" src="https://portswigger.net/cms/images/e0/91/1afc66d7078e-article-arpanet-infographic-map.png">

İlerleyen birkaç yıl içerisine yapılan çalışmalar doğrultusuna bu sistem e-posta atılabilir, **TCP/IP** ile dosya gönderme ve uzak bağlantı kurulabilir hale geldi.

1980’li yıllarda internetin Avrupa’da yükselişiyle beraber, domain name sistemleri ortaya çıkmaya başladı. Amerika ile Avrupa arasında bir IP bağlantısı oluşturulmasının ardından, **WWW** bulucusu olarak bilinen Tim Berners Lee, internet üzerinde bir bilgi dünyası oluşturulabileceğinin kararını vermişti. 1990’lı yıllarda yine Tim Berners Lee tarafından ortaya çıkarılan **HTML**, başka bir icat olarak ortaya çıkmıştır. WWW ve HTML’nin ardından tek eksik olan şey bir internet tarayıcısıydı. Tim Berners Lee’nin kurduğu tarayıcıyla beraber, World Wide Web’in ilk kullanımını CERN’de gerçekleştirmiştir. Ardından, World Wide Web tüm kullanıcılara açık hale geldi.

<img width="400" src="https://blog.thedigitalgroup.com/assets/uploads/web3.0-1024x601.png">

Web dünyası WWW'dan günümüze kadar 3+1 dönemden geçti.Bunlar sırasıyla Web 1.0, Web 2.0, Web 3.0 + Web 4.0 olarak kabul edilir. 
**Web 1.0**(The HyperText Web) döneminde statik(kullanıcıya göre değişken olmayan) siteler yapılı.**Web 2.0**(The Social Web) döneminde dinamik sistemlere geçiş yapıldı ve bu süreçte Youtube, Facebook gibi sosyal medya, blog, wiki temalı sistemler geliştirilmeye başlandı.**Web 3.0**(The Semantic Web) döneminde **SEO**(arama motoru optimizasyonu) bazlı geliştirmeler yapıldı bu sayede arama motorları site içeriklerini çok daha iyi bir şekilde anlamaya ve kullanıcılara göre tepkı vermeye başladı.**Web 4.0**(The Intelligent Web) ile birlikte **IoT**(Internet of Things) ve giyilebilir cihazlar git gide hayatımızın bir parçası olmaya başladı.  

Artık temel anlama internetin tarihini öğrendik.Artık Web dünyasına kullanılan temel protokoller ve Web'in çalışma mantığına anlayabiliriz.

## Temel kavramlar ve Web'in Çalışma Mantığı
### IP(Internet Protocol)
Ağ sınırları boyunca datagramların geçişi için internet protokolü takımında temel iletişim protokolüdür. Yönlendirme işlevi sayesinde internetin çalışmasını sağlamaktadır. IP, paket teslim görevini paket başlıklarındaki IP adreslerine dayalı olarak kaynak adresten hedef adrese doğru gerçekleştirir.  
  + IPV4: 32 bit'ten oluşan adrestir.Örnek: `192.149.252.47`
  + IPV6: 128 bit'ten oluşan adrestir.Örnek: `21DA:00D3:0000:2F3B:02AA:00FF:FE28:9C5A`

### MAC adresi(Media Access Control)
MAC adresi, ağ donanımlarını kimliklemeye yarayan bir numaradır.Modemler veya bilgisayardaki ağ kartlarında(ethernet, wifi, bluetooth, ...) 48 bitlik doğrudan donanıma işlenmiş olarak gelmektedir.Donanım üreticilerine bu adresler için kullanılabilecek belli aralıklar verilir  böylece mac adresini bildiğiniz bir cihazın ağ kart üreticisini de bilebilirsiniz.

 Örnek: `01:23:45:67:89:AB`

### TCP(Transmission Control Protocol)
Vint Cerf ve Bob Khan bir ağ üzerinde yer alan uçlar (nodes) arasında kaynak paylaşımını sağlamak amacıyla "packet-switching" yöntemini kullanan bir ağ protokolü tanımladılar. Bu protokol modelini paket anahtarlamalı olarak nitelendirdiler ve TCP‘nin temelleri atılmış oldu.

TCP'nin çalışma esası üç faz altında incelenebilir.Öncelikle hedefle bir bağlantı gerçekleşir, bağlantı gerçekleştikten sonra veri transferi yapılır, veri transferi yapıldıktan sonra da bağlantı sona erdirilir.

### DNS(Domain Name System)
Alan adı sistemi IP adreslerini alan adları ile haritalar.Tarayıcıda arama çubuğuna [mavidurak.github.io](mavidurak.github.io) size bu adrese karşılık olarak bir IP adresi döndürür.

<img width="400" src="https://www.andronova.net/images/upload/screenshot.1886912829.jpg">

### Server
Sunucu temel olarak bir bilgisayardır, içerisinde oyun oynamak veya günlük kullanım yerine belirli programsal işlerin yapılması sağlanır.Bu işler dışında kullanılacak donanıma(ekran, klavye, fare vb.) sahip olması gerekmez.**SSH** gibi protokoller kullanılarak başka bir bilgisayardan erişim kurulabilir.

<img width="400" src="https://www.intel.com.tr/content/dam/products/hero/foreground/server-boards-products-hero-foreground-16x9.png.rendition.intel.web.480.270.png">
<img width="400" src="https://www.servetr.com/wp-content/uploads/2015/02/disk-ekleme-750x422.jpg">

### ISP(Internet Service Provider, İSS- İnternet Servis Sağlayıcısı)
Şirketlere yada kişilere internet bağlantısı, altyapısı ve teknik desteği sağlayan kurumlar.

### IAN(Internet Area Network)
İnternet altyapısı, yönetimi ve ağ oluşturmada kullanılan, cihaz sayısı, erişim menzili gibi etmenler göz ününde bulundurularak hazırlanan model.

<img width="400" src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6e/Data_Networks_classification_by_spatial_scope.svg/688px-Data_Networks_classification_by_spatial_scope.svg.png">

+ **WAN**(Wide Area Network):
Ülke gibi geniş bir coğrafyaları ve yüksek kullanıcı sayısını kaplayan ağ türüdür.

+ **RAN**(Region Area Network):
Ülkelerin coğrafi bölgelerini kapsayan ağ türüdür.

+ **MAN**(Metropolitan Area Network):
Büyükşehir alanını kapsayan ağ türüdür.LAN'ların genel ağa bu bağlantı sayesinde bağlanır.

+ **CAN**(Campus Area Network):
Üniversite kampusleri gibi yüksek sayıda kullanıcıyı kapsayan ağ türüdür.

+ **LAN**(Local Area Network):
Ev, iş yeri gibi birden fazla kullanıcının bulunduğu en küçük ağdır.

+ **PAN**(Personal Area Network):
İnsan vücudunu kapsayan ağ türüdür.Gelişen teknoloji ile kullanım yoğunluğu gittikçe artmaktadır.Dış internete bağlanmadan vücutta bulunan cihazlar(giyilebilir) ile haberleşmek için kullanılır.

+ **BAN**(Body Area Network):
Vücutta bulunan akıllı implant ve benzeri vücuda gömülü olan sistemlerde haberleşmeyi geciktirmemek için doğrudan vücut içerisinden yapılması modellenen ağdır.BAN giyilebilir bir gateway sayesinde dışarıya açılabilir.

+ **Nanoscale Network**:
Nano ağ veya nano ölçekli ağ, hesaplama, veri depolama, algılama ve çalıştırma gibi yalnızca çok basit görevleri yerine getirebilen nanomakinelerin (birkaç yüz nanometre veya en fazla birkaç mikrometre boyutunda cihazlar) bilgiyi koordine etmelerine, paylaşmalarına ve birleştirmelerine olanak sağlayan ağ modelidir.

### HyperText(Hiper Metin)
Düz yazının aksine video, resim, tablo, referans gibi içerikler içeren belge türüdür.

### HTTP(HyperText Transfer Protocol)
HTTP, 1989'da CERN'de Tim Berners-Lee tarafından geliştirilmeye başlandı. Yorumlara yönelik erken HTTP taleplerinin (RFC'ler) geliştirilmesi, İnternet Mühendisliği Görev Gücü (IETF) ve World Wide Web Consortium (W3C) tarafından koordine edilmiş bir çalışmadır. Daha sonra IETF'e taşınmıştır.

HTTP, istemci-sunucu bilgi işlem modelinde bir istek-yanıt protokolü olarak işlev görür. Örneğin, bir web tarayıcısı istemci olabilir, veya bir web sitesini barındıran bir barındırma hizmetinde çalışan bir uygulama sunucu olabilir.İstemci, sunucuya bir HTTP istek mesajı gönderir.HTML dosyaları ve diğer içerik gibi kaynakları sağlayan veya istemci adına diğer işlevleri gerçekleştiren sunucu, istemciye bir yanıt mesajı verir.Yanıt, istekle ilgili tamamlanma durumu bilgilerini içerir, ayrıca mesaj gövdesinde istenen içeriği gösterebilir.

### Temel Çalışma Mantığı

# Lisans
[GPL-3.0 License](LICENSE)