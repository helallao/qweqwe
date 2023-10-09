# [Input](#input-1)
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
* [Object Info](#object-info)
* [Particle Info](#particle-info)
* [Point Info](#point-info)
* [RGB](#rgb)
* [Tangent](#tangent)
* [Texture Coordinate](#texture-coordinate)
* [UV Map](#uv-map)
* [Value](#value)
* [Volume Info](#volume-info)
* [Wireframe](#wireframe)

# [Output](#output-1)

# [Shader](#shader-1)
* [Add Shader](#add-shader)
* [Anisotropic BSDF](#anisotropic-bsdf)
* [Diffuse BSDF](#diffuse-bsdf)
* [Emission](#emission)
* [Glass BSDF](#glass-bsdf)
* [Glossy BSDF](#glossy-bsdf)
* [Hair BSDF](#hair-bsdf)
* [Holdout](#holdout)
* [Mix Shader](#mix-shader)


<br>
<br>


# Input
Bu kategorideki node'lar bu shader'ı kullanan objenin/mesh'in bilgilerini verirler. Bu bilgileri kullanarak shader'ı yapılandırırız. Bu yüzden kategorinin ismi "Input".


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



## [Object Info](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/object_info.html)
Obje hakkında bilgiler verir.


* #### Location (Output)
Objenin orijin noktasını verir. Geometry'deki ["Position"](#position-output) gibi her nokta için konum vermez, sadece objenin orijin noktasını verir.

* #### Color (Output)
Objenin ayarlardan ayarlanmış renk degerini verir.

* #### Alpha (Output)
Bilmiyorum.

* #### Object Index (Output)
Objenin ayarlardan ayarlanmış "pass index" degerini verir.

* #### Material Index (Output)
Objenin material ayarlarından ayarlanmış "pass index" degerini verir.

* #### Random (Output)
Bu shader'ı kullanan her obje için 0 ile 1 arası rastgele deger verir.



## [Particle Info](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/particle_info.html)
Bilmiyorum.



## [Point Info](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/point_info.html)
Bilmiyorum.



## [RGB](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/rgb.html)
Renk veri tipinde bir deger oluşturmanıza yarar, yani renk oluşturmanıza yarar. Oluşturduğunuz rengi renk input'u olan herhangi bir node'a bağlayabilirsiniz.



## [Tangent](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/tangent.html)
Bilmiyorum.



## [Texture Coordinate](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/texture_coordinate.html)
Texture'ları düzgün bir şekilde mesh'e yerleştirebilmemiz için gerekli olan mesh boyut degerlerini verir.


* #### Generated (Output)
Bilmiyorum.

* #### Normal (Output)
Mesh'in her bir yüzünün baktığı yön degerini verir.

* #### UV (Output)
Bilmiyorum.

* #### Object (Output)
Bilmiyorum.

* #### Camera (Output)
Kameranın bakış açısına göre texture'u yerleştirmeye yarar, nereden bakarsan bak aynı görünür.

* #### Window (Output)
"Camera" output'u ile aynıdır, tek farkı ekran büyüklüğüne göre boyutları x ve y eksenlerinde oranlar.

* #### Reflection (Output)
Bilmiyorum.

* #### Object (Node Input)
Bilmiyorum.

* #### From Instancer (Node Input)
Bilmiyorum.



## [UV Map](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/uv_map.html)
Bilmiyorum.


* #### UV (Output)
Bilmiyorum.

* #### From Instancer (Node Input)
Bilmiyorum.

* #### Text Input (Node Input)
Bilmiyorum.



## [Value](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/value.html)
Float veri tipinde bir deger oluşturmanıza yarar, yani sayı degeri oluşturmanıza yarar. Oluşturduğunuz degeri sayı input'u (gri) olan herhangi bir node'a bağlayabilirsiniz.



## [Volume Info](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/volume_info.html)
Bilmiyorum.



## [Wireframe](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/wireframe.html)
Bilmiyorum.


<br>
<br>


# Output


<br>
<br>


# Shader
Bu kategorideki node'lar ana shader türlerini barındırır. Bu shader node'ları ile farklı shader türlerini kullanarak istedigimiz shader'ı yapabiliriz. En fazla kullanılan shader türü [Principled BSDF'dir](a) çünkü birçok shader türünü kendi içerisinde barındırır. Principled BSDF bu kategorideki birçok shader türü node'larının yerine kullanılabilir, dolayısıyla birçok node zaten gereksiz gibi düşünebilirsiniz ama öyle degil. Bazı node'larda Principled BSDF node'unda olmayan özellikler de var, dolayısıyla bu özellikleri kullanmak için o node'lara da ihtiyacımız var.


## [Add Shader](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/add.html)
Verilen iki shader'ı toplar, birbirlerine ekler. Sonuç daha parlak olur.


* #### Shader (Output)
Sonuç.

* #### Shader (Socket Input)
Bilmiyorum.

* #### Shader 2 (Socket Input)
Bilmiyorum.



## [Anisotropic BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/anisotropic.html)
Bilmiyorum.



## [Diffuse BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/diffuse.html)
Bilmiyorum.



## [Emission](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/emission.html)
Bilmiyorum.


* #### Emission (Output)
Sonuç shader'ı.

* #### Color (Socket Input)
Renk.

* #### Strength (Socket Input)
Emission şiddeti.



## [Glass BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/glass.html)
Cam shader'ı oluşturmaya yarar.


* #### BSDF (Output)
Shader.

* #### Mode Input (Node Input)
Buradan farklı modlar kullanarak cam shader'ı oluşturabilirsiniz.

* #### Color (Socket Input)
Cam rengi.

* #### Roughness (Socket Input)
Camın arkasını ne kadar keskin gösterecegini etkiler. 0'da iken arkayı tam gösterir, yükselttikçe arkayı bulanık gösterir.

* #### IOR (Socket Input)
[Index of Refraction](https://en.wikipedia.org/wiki/Refractive_index) degerini ayarlar, yani ışığın yönünün camın içinden geçerken kırılma derecesini.

* #### Normal (Socket Input)
Bilmiyorum.



## [Glossy BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/glossy.html)
Ayna shader'ı oluşturmaya yarar. Yani yüzeyi ayna gibi gelen ışıgı yansıtan shader oluşturur.


* #### BSDF (Output)
Shader.

* #### Mode Input (Node Input)
Buradan farklı modlar kullanarak ayna shader'ı oluşturabilirsiniz.

* #### Color (Socket Input)
Ayna rengi.

* #### Roughness (Socket Input)
Aynanın ne kadar gösterecegini etkiler. 0'da iken pürüzsüz gösterir, yükselttikçe bulanık gösterir.

* #### Normal (Socket Input)
Bilmiyorum.



## [Hair BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/hair.html)
Bilmiyorum.



## [Holdout](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/holdout.html)
Bu shader boşluk oluşturmaya yarar. Ekranda bu shader'ın oldugu yer silinir, arkayı da göstermez.


* #### Holdout (Output)
Shader.



## [Mix Shader](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/mix.html)
Verilen iki shader'ı birleştirir.


* #### Shader (Output)
Sonuç shader'ı.

* #### Fac (Socket Input)
Faktör degeri, bu deger 0'a kaydıkça 1. shader, 1'e kaydıkça 2. shader kullanılır. 0.5 yaparsanız iki shader'ın ortası olur. Bu şekilde istediginiz gibi oranlama yapabilirsiniz.

* #### Shader (Socket Input)
Karıştırılacak 1. shader.

* #### Shader 2 (Socket Input)
Karıştırılacak 2. shader.



## [Principled BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/principled.html)
Birçok shader türünün birleşimi olan tek bir shader'dır. En çok kullanılan shader budur.


* #### BSDF (Output)
Sonuç shader'ı.

* #### Distribution Mode (Node Input)
GGX | Multiscatter GGX
:---: | :---:
‎GGX | Multiscatter GGX'e göre daha hızlı ama dogruluk bakımından onun kadar dogru degil. Bunu seçerseniz "Transmission Roughness" ayarı açılır. Multiscatter GGX'e göre shader daha koyu olur.
‎Multiscatter GGX | Bu mod GGX'e göre enerjiyi daha fazla muhafaza eder. Yani ışık ışınları enerjisi bitene kadar sekmeye devam eder. Bu da daha parlak ve gerçekçi bir görünüm ile sonuçlanır. Roughness degeri düşük olan shader'larda ışınların sekmesi zor olacağı için etkisini de kaybeder, yani roughness degeri yüksek olan shader'larda etkisi daha belli olur. Hesaplama bakımından GGX'e göre 2.5% daha yavaştır.

* #### Subsurface Method Mode (Node Input)
asd

* #### Base Color (Socket Input)
Shader'ın ana rengi.

* #### Subsurface (Socket Input)
Bu deger arttıkça Subsurface Scattering etkisi de artar. Subsurface etkisi şudur, arkadan ışık vurunca objenin iç renginin yüzeye vurması ve yüzeyin biraz bu renge kaymasıdır. Mesela insan derisi örnek verilebilir, parmağınızı herhangi bir ışığın üstüne koydugunuzda parmagınız kırmızı şekilde ışıgı yansıtır. İşte buna Subsurface Scattering (SSS) deniyor.

* #### Subsurface Radius (Socket Input)
İnput olarak 3 boyutlu vektör alır. Her bir kanal kırmızı, yeşil ve mavi ışığın Subsurface etkisi derecesini belirler. Yani mesela default olarak verilen deger (1.0, 0.2, 0.1) dir. Bu da kırmızı ışığın daha fazla Subsurface Scattering etkisi yapacağını gösterir.

* #### Subsurface Color (Socket Input)
Subsurface Scattering etkisi için kullanılacak renk.

* #### Subsurface IOR (Socket Input)
[Index of Refraction](https://en.wikipedia.org/wiki/Refractive_index) degerini ayarlar, yani ışığın yönünün obje içinden geçerken kırılma derecesini.

* #### Subsurface Anisotropy (Socket Input)
asd

* #### Metallic (Socket Input)
Objeyi metalik hale getirir.

* #### Specular (Socket Input)
Işığı yansıtma derecesi. 0 iken hiç yansıtmaz, arttıkça daha fazla yansıtır.

* #### Specular Tint (Socket Input)
Yansıyan ışıga yüzeyin rengini verme derecesi. 0 iken yansıyan ışığın rengini degiştirmez. 1 iken yansıyan ışığa yüzeyin de rengini ekler. Yani yansıtırken kendi rengini de ekler.

* #### Roughness (Socket Input)
Objenin yüzeyinin ne kadar pürüzlü olduğunu ayarlar. 0 iken pürüzsüzdür ve yansıtma özelligi artar. 1 iken çok pürüzlüdür ve yansıtma özelligi azalır.

* #### Anisotropic (Socket Input)
Anisotropic ve Anisotropic Rotation ayarları ışığın yansıtma yönünü değiştirmek ile ilgilidir. Anisotropic Rotation ayarı yönü degiştirir. Anisotropic ayarı ise bu yön degiştirmenin ne kadar etkili olacağını belirler.

* #### Anisotropic Rotation (Socket Input)
Anisotropic ve Anisotropic Rotation ayarları ışığın yansıtma yönünü değiştirmek ile ilgilidir. Anisotropic Rotation ayarı yönü degiştirir. Anisotropic ayarı ise bu yön degiştirmenin ne kadar etkili olacağını belirler.

* #### Sheen (Socket Input)
Bu ayar genellikle giyisi tarzı shader'larda kullanılıyor. Kenarlara ışığın yansımasından dolayı parlaklık efekti ekler.

* #### Sheen Tint (Socket Input)
Aynı Specular Tint gibi, Sheen etkisinin verdigi parlaklığa yüzeyin de rengini eklemesine sebep olur.

* #### Clearcoat (Socket Input)
Clearcoat sanki yüzey bir şey ile kaplanmış gibi görünmesine sebep olur. İkincil bir yüzey oluşturur. Araba boyası gibi.

* #### Clearcoat Roughness (Socket Input)
Clearcoat için Roughness degeri.

* #### IOR (Socket Input)
[Index of Refraction](https://en.wikipedia.org/wiki/Refractive_index) degerini ayarlar, yani ışığın yönünün obje içinden geçerken kırılma derecesini.

* #### Transmission (Socket Input)
Objeyi saydam yapar.

* #### Transmission Roughness (Socket Input)
Transmission için Roughness degeri.

* #### Emission (Socket Input)
Emission ayarı Base Color gibidir. Yüzey rengini ayarlar. Emission Strength ayarı ile yüzey renginin şiddetini arttırabiliriz. Şiddet arttıkça renk neon gibi parlamaya başlar ve ışık saçar.

* #### Emission Strength (Socket Input)
Emission şiddeti.

* #### Alpha (Socket Input)
asd

* #### Normal (Socket Input)
asd

* #### Clearcoat Normal (Socket Input)
asd

* #### Tangent (Socket Input)
asd


https://pixelandpoly.com/ior.html











