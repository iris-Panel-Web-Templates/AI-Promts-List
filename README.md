# AI-Promts-List
AI ile PHP/SQL ile hazırlanmış bir siteyi irisPanel Onyx Api sistemi dönüştürmeye yardımcı olur.

```markdown
iTemplate = "iris Panel Onyx"
iTemplate SQL kullanmadan Api geliştirilmiş bir arabirim kullanır.
"Kayıt", "Şifremi unuttum", "Kullanıcı Paneli", "Kullanıcı Hesap Yönetimi", "Oyuncu Sıralaması", "Lonca Sıralaması", "Ban Listesi", "istatistikler", "Haberler", "İndirme Linkleri" vs. vs. birçok şeyi api ile yönetir.


myTemplate = "Benim Hazırladığım Site"
Tüm işlemleri SQL'e bağlanarak yapar.


Bilmen gerekenler:
OyunAdı    = "TugraMt2 ONYX"
SiteURL    = "tugramt2.com"
irisAuthKey = "8OTWUXU4HTDH75A2"
iTemplate için dosya yolu  = "https://github.com/iris-Panel-Web-Templates/Web-Clasic"
myTemplate için dosya yolu = "C:\Users\pc\Desktop\FTP_old"


Kurallar:
iTemplate dosyalarında asla değişim yapma. (unutma)
Dosya okur yada yazarken bana sormana gerek yok. (unutma)
iTemplate içindeki "iSystem" klasörünü myTemplate içerisine kopyala. (ilk bunu yap)
"iSystem" içindeki dosyalarda asla değişim yapma. Bunlar Api erişim için kullanacağımız dosyalar. (unutma)


Yapılacaklar: (sırası ile yap, sırayı bozma)
myTemplate PHP versiyonu 8.3'e yükselt.
myTemplate de OPcache/Redis/Memcached kullanıldı ise bunları APCu'ya çevir, store mantığını iTemplate deki gibi yap.
myTemplate Temayı bozmamaya özen göster.
myTemplate SQL işlemlerini iTemplateden aldığımız Api Fonksiyonlarına göre uyarlarla.
Dosyalarda geçen "Darkbey" ismini benim verdiğim OyunAdı ile değiş.
Dosyalarda geçen tasarımcı/yapımcı bilgisini OyunAdı ile değiştir, URL'leri var ise onlarıda SiteURL ile değiştir.
Dosyalarda geçen tasarımcı/yapımcı bilgisini OyunAdı ile değiştir.
Sözleşme dosyasını silme, içindeki oyun adı ve urlleri verdiğim oyun adı ve site urlsi ile güncelle. (dosya "imprint,agreement,contract,articles,sozlesme,kontrat" gibi isimlere sahip olabilir)
myTemplate dosyaları içinde kullanılan JavaScrip ve CSS'lerin eğer CDN'i var ise Javascrip'ler ve Css'ler için CDN kullan, sonra CND e çevrilen dosyları sil.
Değişimler sonrası myTemplate'e ait klasör içinde kullanılmayan php dosyası var ise sil. (Üyelik sözleşmesi gibi sayfalarda linki olan dosyaları koru.)
Değişimler sonrası myTemplate'e ait klasör içinde ihtiyaç olmayan php dosyası var ise sil. (Üyelik sözleşmesi gibi sayfalarda linki olan dosyaları koru.)
Değişimler sonrası myTemplate'e ait klasör içinde  gereksiz/kullanılmayan resimleri bul ve sil.
Değişimler sonrası myTemplate içindeki ".htaccess" RewriteRule kurallarını değişimlere düzenle.
Gereksiz kodları ve açıklamaları sil.
Olası arka plan açıkları yada siteye zarar verecek JavaScript yada PHP kodu görürsen sil. (bana mutlaka bildir)

yukarıdaki işlemler bitince myTemplate'de hatalar var mı kontrol et, varsa düzeltmesini yap.

Boyutu çok büyük resimler var ise Optimize et.
```
