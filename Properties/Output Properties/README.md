# Ek Bilgiler

<details>
<summary>Kullanılan Güzel Kaynaklar</summary>
<br>

* [Export animation renders the RIGHT way in Blender!](https://www.youtube.com/watch?v=UH-zqJ2Jx64) - Brandon's Drawings'in videosu. Kendisi blender hakkında en iyi [kaynaklardan birisidir](https://brandonsdrawings.com).

</details>



# [Format](#format-1)
* [Resolution X](#resolution-x)
* [Resolution Y](#resolution-y)
* [Resolution Percentage (%)](#resolution-percentage-)
* [Aspect X](#aspect-x)
* [Aspect Y](#aspect-y)
* [Render Region](#render-region)
* [Crop to Render Region](#crop-to-render-region)
* [Frame Rate](#frame-rate)

# [Frame Range](#frame-range-1)
* [Frame Start](#frame-start)
* [Frame End](#frame-end)
* [Frame Step](#frame-step)
* [Old (Time Stretching)](#old)
* [New (Time Stretching)](#new)

# [Stereoscopy](#stereoscopy-1)

# [Output](#output-1)
* [Output Path](#output-path)
* [File Extensions](#file-extensions)
* [Cache Results](#cache-results)
* [File Format](#file-format)
* [Color](#color)
* [Overwrite](#overwrite)
* [Placeholders](#placeholders)

# [Metadata](#metadata-1)
* [Metadata Input](#metadata-input)
* [Include](#include)
* [Note](#note)
* [Burn Into Image](#burn-into-image)

# [Post Processing](#post-processing-1)
* [Compositing](#compositing)
* [Sequencer](#sequencer)
* [Dither](#dither)


<br>
<br>


# [Format](https://docs.blender.org/manual/en/3.6/render/output/properties/format.html)
Bu kategori render çıktısı için ekran boyutunun (çözünürlük) ve frame rate'inin (fps) ayarlarının olduğu bölümdür.


* #### Resolution X
X ekseninde (Width) render çıktısının boyutunu temsil eder.

* #### Resolution Y
Y ekseninde (Height) render çıktısının boyutunu temsil eder.

* #### Resolution Percentage (%)
Render çıktısının boyutunun yani çözünürlüğünün "Resolution X" ve "Resolution Y" değerlerine dayanarak yüzdelik değeri. Yani bu değer %100 iken çıktının boyutu "Resolution X" ve "Resolution Y" değerlerine eşit olur. Eğer bu ayarı düşürürseniz, mesela %50 yaparsanız çıktının boyutu da yarıya düşer.

* #### Aspect X
Aspect ratio yani en boy oranı için X ekseni değeri. Bu değeri attırırsanız X ekseni sündürülür. En boy oranı standart orandan farklı olan ekranlar içindir.

* #### Aspect Y
Aspect ratio yani en boy oranı için Y ekseni değeri. Bu değeri attırırsanız Y ekseni sündürülür. En boy oranı standart orandan farklı olan ekranlar içindir.

* #### Render Region
Bu ayar açıkken sadece ["Render Region"](https://docs.blender.org/manual/en/3.6/editors/3dview/navigate/regions.html#render-region) olarak seçilen yer render edilir. Çıktının geriye kalan yerleri görünmez olarak ayarlanır.

* #### Crop to Render Region
Sadece "Render Region" ayarı açıkken vardır. Bu ayar açık değilken "Render Region" ayarı seçilen kısmı render eder, geriye kalan kısımlar ise görünmez olarak ayarlanır. Yani çıktı hala aynı boyuttadır ve sadece "Render Region" olarak seçilen kısım render edilir. Eğer bu ayarı açarsanız çıktıda arka plan da gösterilmez. Sadece "Render Region" olarak seçilen kısım render edilir ve bu kısım çıktının kendisidir.

* #### Frame Rate
Animasyonun frame rate'i (fps, kare hızı).


<br>
<br>


# [Frame Range](https://docs.blender.org/manual/en/3.6/render/output/properties/frame_range.html)
Bu kategori yaptığınız animasyonun frame (fps, kare hızı) sayısını ve hızını ayarladığınız bölümdür.


* #### Frame Start
Başlangıç frame'i.

* #### Frame End
Bitiş frame'i.

* #### Frame Step
Frame başına atlanacak frame sayısı, adım sayısı. Mesela bunu 2 yaparsanız her 2 frame'in biri animasyonda oynatılır.


## Time Stretching

* #### Old
"Time Stretching" frame ile oynatma hızının birbirlerinden farklı olarak ilerlemesini sağlar. Verdiğimiz orana göre animasyonu daha hızlı veya yavaş ilerlemeye alabiliriz. Blender'da default olarak bu ayar 100 olarak geliyor, aslında bu sayının kaç olduğunun önemi yok, önemli olan "Old" ile "New" sayılarının arasındaki oran. Mesela "Old" ve "New" 1 olarak ayarlanırsa oranlar eşit olacağı için 100'e ayarlandıklarında çıkacak animasyonunun aynısı olacaktır. Eğer oranlar farklı olursa, mesela "Old" 2, "New" 1 olursa oynatma hızı 2 kat daha hızlı oynatılacaktır. Oynatma hızının hızlı oynatılması ile frame hızı farklı şeylerdir, eğer animasyonu oynatırsanız bunu görebilirsiniz. Frame sayısı henüz yarıdayken animasyonun tamamının oynatıldığını görebilirsiniz. Yani oynatma hızını 2 katına çıkarmış olursunuz. Bu şekilde oynatma hızını hızlandırabilir/yavaşlatabilirsiniz. Ayrıca oranı manuel olarak hesaplamaktansa, eski ve yeni animasyonların frame sayısını girerek animasyonunuzun oynatma hızını başka bir animasyonun hızına ayarlayabilirsiniz.

* #### New
"Time Stretching" frame ile oynatma hızının birbirlerinden farklı olarak ilerlemesini sağlar. Verdiğimiz orana göre animasyonu daha hızlı veya yavaş ilerlemeye alabiliriz. Blender'da default olarak bu ayar 100 olarak geliyor, aslında bu sayının kaç olduğunun önemi yok, önemli olan "Old" ile "New" sayılarının arasındaki oran. Mesela "Old" ve "New" 1 olarak ayarlanırsa oranlar eşit olacağı için 100'e ayarlandıklarında çıkacak animasyonunun aynısı olacaktır. Eğer oranlar farklı olursa, mesela "Old" 2, "New" 1 olursa oynatma hızı 2 kat daha hızlı oynatılacaktır. Oynatma hızının hızlı oynatılması ile frame hızı farklı şeylerdir, eğer animasyonu oynatırsanız bunu görebilirsiniz. Frame sayısı henüz yarıdayken animasyonun tamamının oynatıldığını görebilirsiniz. Yani oynatma hızını 2 katına çıkarmış olursunuz. Bu şekilde oynatma hızını hızlandırabilir/yavaşlatabilirsiniz. Ayrıca oranı manuel olarak hesaplamaktansa, eski ve yeni animasyonların frame sayısını girerek animasyonunuzun oynatma hızını başka bir animasyonun hızına ayarlayabilirsiniz.


<br>
<br>


# [Stereoscopy](https://docs.blender.org/manual/en/3.6/render/output/properties/stereoscopy/index.html)
a.


<br>
<br>


# [Output](https://docs.blender.org/manual/en/3.6/render/output/properties/output.html)
Render çıktısının dosyası ile ilgili ayarların olduğu bölümdür.


* #### Output Path
Çıktıların kaydedileceği klasör/dosya yolu.

* #### File Extensions
Dosyaların sonuna dosya uzantısı ekler.

* #### Cache Results
Çıktıyı önbelleğe alır, bilgileri önbelleğe almak sonraki frame'leri render ederken hız kazandırabilir.

* #### File Format
Buradan çıktının hangi dosya formatında kaydedileceğini ayarlayabilirsiniz. Eğer resim ise sizin için en iyi seçenek "PNG" olacaktır. Eğer video ise yine en iyi seçenek "PNG" olacaktır çünkü render işlemi esnasında bir hata oluşursa videoyu tekrar baştan render etmek vakit kaybı olur. Eğer "PNG" olarak kaydederseniz, olası bir render hatası durumunda sadece kalan frame'leri render etmeniz gerekir. Render işlemi bittikten sonra da "PNG" dosyaları ile video oluşturabilirsiniz.

* #### Color
Buradan renkleri seçebilirsiniz. "BW" (Black & White) seçeneği siyah beyaz, "RGB" seçeneği alpha kanalı olmadan renkli, "RGBA" seçeneği alpha kanalı ile birlikte renklidir.

* #### Overwrite
Eski dosyaları siler ve yeni oluşturur.

* #### Placeholders
Render işlemi başlayınca oluşturulacak bütün dosyalar için aynı isimde boş dosyalar oluşturur. Render ilerledikçe bu dosyaların içerisine bilgileri yazar. Yani render başlar başlamaz dosyaları oluşturur.


<br>
<br>


# [Metadata](https://docs.blender.org/manual/en/3.6/render/output/properties/metadata.html)
Çıktı dosyasına yazılacak bilgileri belirlediğiniz kategoridir. Metadata eklemeyi destekleyen formatlara [buradan](https://docs.blender.org/manual/en/3.6/files/media/image_formats.html) ulaşabilirsiniz.


* #### Metadata Input
Metadata'nın alınacağı yer.

* #### Include
Eklenecek bilgiler.

Seçenek | Açıklama
:---: | :---:
‎Date | Dosyanın içerisine tarihi ekler.
‎Time | Resmin içerisine saat/dakika ekler.
‎Render Time | Resmin içerisine render edildiği saat/dakika ekler.
Frame | Resmin içerisine frame numarasını ekler.
Frame Range | Dosyanın içerisine toplam frame sayısını ekler.
Memory | Dosyanın içerisine kullanılan maksimum ram derecesini ekler.
Hostname | Dosyanın içerisine bilgisayarın [Hostname'ini](https://en.wikipedia.org/wiki/Hostname) ekler.
Camera | Resmin içerisine aktif kameranın adını ekler.
Lens | Resmin içerisine aktif kameranın lens değerlerini ekler.
Scene | Dosyanın içerisine sahnenin adını ekler.
Marker | Resmin içerisine son marker'ın ismini (animasyon çizelgelerinde kullanılan) ekler.
Filename | Dosyanın içerisine ".blend" uzantılı dosyanızın ismini ekler, yani proje dosyanızın ismini.
Strip Name | Bilmiyorum.

* #### Note
Dosyanın içerisine not eklemenize yarar.

* #### Burn Into Image
Resmin içerisinde görünecek yazı eklemenize yarar.


<br>
<br>


# [Post Processing](https://docs.blender.org/manual/en/3.6/render/output/properties/post_processing.html)
Render sonrası efektler/işlemler ile ilgili ayarların olduğu kategoridir.


* #### Compositing
Bu ayar açıkken composite node'ları kullanılır.

* #### Sequencer
Video Sequence editörünün output'unu render eder.

* #### Dither
Keskin çizgilerden kurtulmak için [Dither](https://en.wikipedia.org/wiki/Dither) uygular. Yani blur efekti uygular da denebilir.

