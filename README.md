# [Input](#input)
* [Ambient Occlusion](#ambient-occlusion)
* [Attribute](#attribute)
* [Bevel](#bevel)
* [Camera Data](#camera-data)
* [Color Attribute](#color-attribute)
* [Curves Info](#curves-info)
* [Fresnel](#fresnel)
* [Geometry](#geometry)


<br>
<br>


# Input



## [Ambient Occlusion](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/ao.html)
Mesh'in üzerindeki gölgeleri veya gölgede kalan kısımlarını hesaplıp renkli ve grayscale map'lerini verir. Bu hesaplama aslında ışıktan bağımsızdır yani gerçekten ışığın nereye vurduğunu nereye vurmadığını kontrol etmez. Gölgeleme işlemi çoğunlukla mesh'in kenarlarında ve çevresi bloklanan kısımlarında olur.


* #### Color (Output)
"Color" inputuna verdiginiz renk map'inin gölge vuran kısımlarının siyaha kaymış halini verir. Yani renkli map'e sanki gölge vurmuş gibi siyah renk eklenmiş halini verir.

* #### AO (Output)
Gölge vuran kısımların siyaha kaydığı (yani 0'a), diğer kısımların da beyaza kaydığı (yani 1'e) grayscale map. Gölge map'i.

* #### Samples (Node Input)
Gölge vuran kısımlar hesaplanırken kullanılacak hesaplama kalitesi.

* #### Inside (Node Input)
Bu ayar açıldığında gölge vuran kısımlar mesh'in dışına göre değilde içine göre hesaplanır.

* #### Only Local (Node Input)
Bu ayar açıkken gölgeler sadece mesh'in kendisinden gelebilir yani gölgeler mesh'in kendi kendini bloklayan kısımlarına göre hesaplanır. Bu ayar kapalıyken başka objelerin de bloklaması ile mesh gölgelenebilir.

* #### Color (Socket Input)
Mesh'in shader'ı. Bu inputa mesh'in rengi yani texture'u baglanabilir. Renk inputu yani.

* #### Distance (Socket Input)
Gölgelerin maksimum yayılabileceği mesafe. Normalde gölgeler köşelerden mesh'in etrafına doğru biraz yayılır. Bu ayar ile yayılım mesafesini ayarlayabilirsiniz. Eger bu ayarı azaltırsanız gölgelerin köşeye doğru kısıtlandıgını görebilirsiniz, arttırırsanız da gölgeler daha fazla yayılır.

* #### Normal (Socket Input)
Bilmiyorum.



## [Attribute](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/attribute.html)
Obje üzerinden gelen değerleri alıp kullanmana yarar ama artık neredeyse hiç kullanılmıyor.


* #### Color (Output)
Bilmiyorum.

* #### Vector (Output)
Bilmiyorum.

* #### Fac (Output)
Bilmiyorum.

* #### Alpha (Output)
Bilmiyorum.

* #### Type (Node Input)
Bilmiyorum.

* #### Name (Node Input)
Bilmiyorum.



## [Bevel](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/bevel.html)
Mesh'in kenar olan kısımlarını açısal farklara dayanarak bulur ve bu kenarlara bevel uygulanmış normal map'i output olarak verir.


* #### Normal (Output)
Bevel uygulanmış normal map.

* #### Samples (Node Input)
Normal map ve bevel kalitesi.

* #### Radius (Socket Input)
Bevel miktarı/derecesi/şiddeti.

* #### Normal (Socket Input)
Bilmiyorum.



## [Camera Data](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/camera_data.html)
Kamera yani bakış açısı ile ilgili bilgileri verir.


* #### View Vector (Output)
Kameranın baktığı yön vektörü.

* #### View Z Depth (Output)
Kameraya olan uzaklık değeri, yani "View Distance" output'u gibidir ama daha farklı bir çalışma şekli vardır. Sanal bir plane (düz plaka/levha yani düzlem) oluşturulur ve bu plane'in normal'i (yani baktığı yön) kameranın baktığı yöndür. Bu output da bu plane'e olan uzaklık değerini döndürür (obje üzerindeki her bir nokta için).

<img src="Dosyalar/View_Z_Depth.png">

* #### View Distance (Output)
Kameraya olan uzaklık değeri (obje üzerindeki her bir nokta için).



## [Color Attribute](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/vertex_color.html)
Bilmiyorum.


* #### Color (Output)
Bilmiyorum.

* #### Alpha (Output)
Bilmiyorum.

* #### Text Input (Node Input)
Bilmiyorum.



## [Curves Info](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/hair_info.html)
Bilmiyorum.


* #### Is Strand (Output)
Bilmiyorum.

* #### Intercept (Output)
Bilmiyorum.

* #### Length (Output)
Bilmiyorum.

* #### Thickness (Output)
Bilmiyorum.

* #### Tangent Normal (Output)
Bilmiyorum.

* #### Random (Output)
Bilmiyorum.



## [Fresnel](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/fresnel.html)
Objenin yüzeyinden ne kadar ışıgın yansıdıgını hesaplar, yansıma miktarı fazla ise beyaza (yani 1'e) düşük ise siyaha (yani 0'a) kayan bir grayscale map verir. Yaptıgı işlemler şöyle gerçekleşir, kameranın bakış açısı ile yüzeyin bakış açısını baz alarak, aralarındaki paralellik yüksekse siyaha (yani 0'a) kayan, aralarındaki paralellik düşükse (en fazla 90 dereceye kadar) beyaza kayan (yani 1'e) grayscale map verir. Yani kameranın bakış açısı ile yüzeyin bakış açısının paralelligini kontrol eder. Bu işlem genellikle obje'nin kenarlarından ortasına doğru beyazdan siyaha kayan bir renk map'i oluşturur.


* #### Fac (Output)
Grayscale map.

* #### IOR (Socket Input)
Bu deger arttıkça output map'indeki beyaz renkler köşelerden ortaya doğru yaklaşır. Azalttıkça köşelere yaklaşır. Aslında bu deger yüzeyin [Index of Refraction](https://en.wikipedia.org/wiki/Refractive_index) degerini ayarlar, yani ışığın yönünün obje içinden geçerken kırılma derecesini.

* #### Normal (Socket Input)
Bilmiyorum.



## [Geometry](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/geometry.html)
Mesh hakkında geometrik bilgiler verir.


* #### Position (Output)
Shader render edilirken mesh üzerindeki her bir nokta için dünya üzerindeki pozisyon vektörü. Yani shader ekrana çizilirken her bir nokta için bu bilgi farklı olabilir, her bir noktanın sahip olduğu bu bilgiyi verir.

* #### Normal (Output)
Shader render edilirken mesh üzerindeki her bir nokta için noktanın baktığı yön vektörü. Yani shader ekrana çizilirken her bir nokta için bu bilgi farklı olabilir, her bir noktanın sahip olduğu bu bilgiyi verir.

* #### Tangent (Output)
Bilmiyorum.

* #### True Normal (Output)
"Normal" output'u ile aynıdır ama mesh'in her bir yüzü için yüzün baktığı yönü verir. Yani her bir yüz için yüzün sahip olduğu bu bilgiyi verir.

* #### Incoming (Output)
Shader render edilirken mesh üzerindeki her bir nokta için noktanın kameraya doğru baktığı yön vektörü. Yani shader ekrana çizilirken her bir nokta için bu bilgi farklı olabilir, her bir noktanın sahip olduğu bu bilgiyi verir.

* #### Parametric (Output)
Mesh'in her bir üçgeni için (dörtgenleri de üçgene çevirir) UV degerini verir. Bu UV degeri ile bütün üçgenler üzerinde işlemler yapabilirsin.

* #### Backfacing (Output)
Mesh'in ön ve arka yüzünü ayırt etmek içindir. İç olan taraf için 1, dış olan taraf için 0 degeri döndürür.

* #### Pointiness (Output)
Mesh'in keskin açıları için 1'e kayan deger, düz olan kısımları için 0'a kayan deger verir.

* #### Random Per Island (Output)
Bu shader'ı kullanan her obje için 0 ile 1 arasında rastgele deger verir.



## [Layer Weight](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/layer_weight.html)
[Fresnel](#fresnel) gibidir. Ek olarak açıya göre deger döndürme modu da vardır.


* #### Fresnel (Output)
[Fresnel](#fresnel) ile aynı mantıkta çalışır, [Fresnel'in](#fresnel) [Fac](#fac) output'u ile aynıdır.










