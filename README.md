# [Input](#input)
* [Ambient Occlusion](#ambient-occlusion)
* [Attribute](#attribute)
* [Bevel](#bevel)
* [Camera Data](#camera-data)
* [Color Attribute](#color-attribute)
* [Curves Info](#curves-info)
* [Fresnel](#fresnel)
* [Geometry](#geometry)
* [Layer Weight](#layer-weight)
* [Light Path](#light-path)


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
Objenin yüzeyinden ne kadar ışığın yansıdıgını hesaplar, yansıma miktarı fazla ise beyaza (yani 1'e) düşük ise siyaha (yani 0'a) kayan bir grayscale map verir. Yaptıgı işlemler şöyle gerçekleşir, kameranın bakış açısı ile yüzeyin bakış açısını baz alarak, aralarındaki paralellik yüksekse siyaha (yani 0'a) kayan, aralarındaki paralellik düşükse (en fazla 90 dereceye kadar) beyaza kayan (yani 1'e) grayscale map verir. Yani kameranın bakış açısı ile yüzeyin bakış açısının paralelligini kontrol eder. Bu işlem genellikle obje'nin kenarlarından ortasına doğru beyazdan siyaha kayan bir renk map'i oluşturur.


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
[Fresnel](#fresnel) gibidir. Ek olarak keskinlik ayarı da vardır. "IOR" input'u yerine "Blend" input'unu kullanır.


* #### Fresnel (Output)
[Fresnel](#fresnel) ile aynı mantıkta çalışır, Fresnel'in [Fac](#fac-output-1) output'u ile aynıdır.

* #### Facing (Output)
[Fresnel](#fresnel) ile aynı mantıkta çalışır ama daha keskindir. Normal Fresnel yüzeyleri bir bütün gibi etkilerken bu özellik her bir noktayı etkilermiş gibi output verir. Yani noktanın baktığı yön ile kameranın baktığı yönün paralelligi birazcık azalsa hemen fark eder. Bu da fresnel efektinin dairesel olarak dağıldığını bile görebilmemizi sağlar.

* #### Blend (Socket Input)
Fresnel efekti için keskinlik derecesini ayarlar. Degeri düştükçe fresnel efekti şiddetlenir, arttıkça fresnel efekti azalır.

* #### Normal (Socket Input)
Bilmiyorum.



## [Light Path](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/light_path.html)
Kameranın yolladığı ışık ışınları (ray) ile ilgili bilgiler verir.


* #### Is Camera Ray (Output)
Işıgın geldiği noktanın tam olarak mesh'e ait olup olmadığını kontrol eder. Yani eger ışık kameraya mesh üzerinden geliyorsa yani yansıma yoksa ve orijinal konum dışında bir yerden gelmiyorsa 1 döndürür, eger yansıma ile geliyorsa yani orijinal konumdan gelmiyorsa 0 döndürür.

* #### Is Shadow Ray (Output)
Işığın geldiği noktanın gölge olan kısma ait olup olmadığını kontrol eder (hem mesh'in üzerindeki hem yerdeki). Eger ışık kameraya gölge olan kısımdan geliyorsa 1, gölge olmayan kısımdan geliyorsa 0 döndürür.

* #### Is Diffuse Ray (Output)
Işığın geldiği noktanın direktmen mesh'e mi ait yoksa başka bir yerden sekerek gelen bir ışıga mı ait olup olmadığını kontrol eder. Yani eger ışık ışını (ray) direktmen mesh'e değiyorsa 0 döndürür, eger başka bir yerden sekip değiyorsa 1 döndürür. Mesela bunu kullanıp iki shader'ı birleştirirken mix faktörü olarak kullanırsan, mesh'e yeşil renk ve mesh dışındaki her şeye mesh'i kırmızı olarak yansıtabilirsin.

* #### Is Glossy Ray (Output)
Bilmiyorum.

* #### Is Singular Ray (Output)
Bilmiyorum.

* #### Is Reflection Ray (Output)
Bilmiyorum.

* #### Is Transmission Ray (Output)
Bilmiyorum.

* #### Ray Length (Output)
Işık ışınının (ray) gittiği mesafe degeri. 0'dan başlayıp sonsuza kadar artabilir.

* #### Ray Depth (Output)
Işık ışınının (ray) toplamda kaç defa sektigini veya kaç şeyin içinden geçtigini gösterir. Mesela direktmen kameraya geldiyse 1 döndürür, kameranın önünde cam varsa ve camdan geldiyse 2 döndürür. Bu sayı sonsuza kadar artabilir.

* #### Diffuse Depth (Output)
Bilmiyorum.

* #### Glossy Depth (Output)
Bilmiyorum.

* #### Transparent Depth (Output)
Işık ışınının (ray) toplamda kaç saydam şeyin içinden geçtiğini gösterir.

* #### Transmission Depth (Output)
Bilmiyorum.



