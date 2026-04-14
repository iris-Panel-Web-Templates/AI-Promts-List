# AI-Promts-List
AI ile PHP/SQL ile hazırlanmış bir siteyi irisPanel Onyx Api sistemi dönüştürmeye yardımcı olur.
Cursor, Codex, CludeCode aracılığı ile yapabilirsiniz.

Gerekli alanları değiştirerek kullanbilirsiniz. (OyunAdı, SiteURL, irisAuthKey)
"iTemplate için dosya yolu" alanına isterseniz bilgisayarınızdaki konumu yazabilirsiniz.

```text
iTemplate = "iris Panel Onyx"
iTemplate nedir: 'irisPanel' altyapısı ile çalışır; tüm veri işlemleri SQL'e doğrudan bağlantı olmadan merkezi bir 'REST API' üzerinden yürütülür.
"Kayıt", "Şifremi unuttum", "Kullanıcı Paneli", "Kullanıcı Hesap Yönetimi", "Oyuncu Sıralaması", "Lonca Sıralaması", "Ban Listesi", "istatistikler", "Haberler", "İndirme Linkleri" vs. vs. birçok şeyi api ile yönetir.


myTemplate = "Benim Hazırladığım Site"
myTemplate nedir: Tüm işlemleri SQL'e bağlanarak yapar.


Bilmen gerekenler:
OyunAdı     = "TugraMt2 ONYX"
SiteURL     = "tugramt2.com"
irisAuthKey = "xxxxxxxxxx"
iTemplate için dosya yolu  = "https://github.com/iris-Panel-Web-Templates/Web-Clasic"
myTemplate için dosya yolu = "C:\Users\xxxx\Desktop\MyTemplate"


Kurallar:
iTemplate dosyalarında asla değişim yapma. (unutma)
Dosya okur yada yazar iken bana sormana gerek yok. (unutma, benden sürekli izin isteme)
iTemplate içindeki "iSystem" klasörünü myTemplate içerisine kopyala. (ilk bunu yap)
"iSystem" içindeki dosyalarda asla değişim yapma. Bunlar Api erişim için kullanacağımız dosyalar. (unutma)


Yapılacaklar: (sırası ile yap, sırayı bozma)
İlk adımda myTemplate projesi genelinde PHP 8.3 uyumluluk taraması yap; deprecation/fatal üreten yerleri (özellikle required/optional parametre sırası ve başlangıç akışındaki bağlantı/fallback hataları) düzeltmeden diğer adımlara geçme.
myTemplate de OPcache/Redis/Memcached kullanıldı ise bunları APCu'ya çevir, store mantığını iTemplate deki gibi yap.
myTemplate Temayı bozmamaya özen göster.
myTemplate SQL işlemlerini iTemplateden aldığımız Api Fonksiyonlarına göre uyarlarla.
Dosyalarda geçen "XXXXX" ismini benim verdiğim OyunAdı ile değiş.
Dosyalarda geçen tasarımcı/yapımcı bilgisini OyunAdı ile değiştir, URL'leri var ise onlarıda SiteURL ile değiştir.
Dosyalarda geçen tasarımcı/yapımcı bilgisini OyunAdı ile değiştir.
.htaccess yok ise oluştur. (iTemplate den örnek alabilirsin)
.htaccess içinde yer alan RewriteRule'leri yeni sisteme göre güncelle. (seo uyumlu olsun)
iTemplate .htaccess dosyası içinde olup myTemplate .htaccess içinde olmayan önemli satırlar var ise ekle.
myTemplate içinde error.php yok ise güzel birtane oluştur ve .htaccess'e bunu işle.
Sözleşme dosyasını silme, içindeki oyun adı ve url'leri verdiğim oyun adı ve site url'si ile değiştir. (dosya "imprint,agreement,contract,articles,sozlesme,kontrat" gibi isimlere sahip olabilir)
myTemplate dosyaları içinde kullanılan JavaScrip ve CSS'lerin eğer CDN'i var ise bu Javascrip'ler ve Css'ler için CDN kullan, sonra CDN e çevrilen dosyları sil.
Değişimler sonrası myTemplate'e ait klasör içinde kullanılmayan php dosyası var ise sil. (Üyelik sözleşmesi gibi sayfalarda linki olan dosyaları koru)
Değişimler sonrası myTemplate'e ait klasör içinde ihtiyaç olmayan php dosyası var ise sil. (Üyelik sözleşmesi gibi sayfalarda linki olan dosyaları koru)
Değişimler sonrası myTemplate'e ait klasör içinde  gereksiz/kullanılmayan resimleri bul ve sil. (CSS dosyalarını mutlaka kontrol et, CSS'lerde geçiyor ise silme)
Değişimler sonrası myTemplate içindeki ".htaccess" RewriteRule kurallarını değişimlere göre düzenle.
Gereksiz kodları ve açıklamaları sil.
Olası arka plan açıkları yada siteye zarar verecek JavaScript yada PHP kodu görürsen sil. (bana mutlaka bildir)
Yukarıdaki işlemler bitince myTemplate'de hatalar var mı kontrol et, varsa düzeltmesini yap.
```


Pro versiyon kullanıyor iseniz aşağıdakileride ekleye bilirsiniz.
```text
Boyutu çok büyük resimler var ise Optimize et. (görüntü bozmadan sıkıştır)
Resimleri sitede kullanıldığı ölçülerde boyutlandır. (örneğin CSS/PHP/JS içinde 64x64 kullanılan bir resim dosyasının ölçüsü 512x512 ise bu resim dosyasını 64x64 boyutlandır)
Hareketli gif dosyalarını webm formatına dönüştür, CSS/PHP/JS dosyalarında geçiyorsa güncelle.
```
