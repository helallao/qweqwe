Aşağıdaki döküman Cycles render motoru kullanıldığı varsayılarak hazırlanmıştır. Eger farklı bir render motoru kullanıyorsanız birçok özellik farklılık gösterecek veya çalışmayacaktır.

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
* [AOV Output](#aov-output)
* [Light Output](#light-output)
* [Material Output](#material-output)
* [World Output](#world-output)

# [Shader](#shader-1)
* [Add Shader](#add-shader)
* [Anisotropic BSDF](#anisotropic-bsdf)
* [Background](#background)
* [Diffuse BSDF](#diffuse-bsdf)
* [Emission](#emission)
* [Glass BSDF](#glass-bsdf)
* [Glossy BSDF](#glossy-bsdf)
* [Hair BSDF](#hair-bsdf)
* [Holdout](#holdout)
* [Mix Shader](#mix-shader)
* [Principled BSDF](#principled-bsdf)
* [Principled Hair BSDF](#principled-hair-bsdf)
* [Principled Volume](#principled-volume)
* [Refraction BSDF](#refraction-bsdf)
* [Subsurface Scattering](#subsurface-scattering)
* [Toon BSDF](#toon-bsdf)
* [Translucent BSDF](#translucent-bsdf)
* [Transparent BSDF](#transparent-bsdf)
* [Velvet BSDF](#velvet-bsdf)
* [Volume Absorption](#volume-absorption)
* [Volume Scatter](#volume-scatter)


<br>
<br>


# Input
Bu kategorideki node'lar bu shader'ı kullanan objenin/mesh'in bilgilerini verirler. Bu bilgileri kullanarak shader'ı yapılandırırız. Bu yüzden kategorinin ismi "Input" dur.


## [Ambient Occlusion](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/ao.html)
Mesh'in üzerindeki gölgeleri veya gölgede kalan kısımlarını hesaplayıp renkli ve grayscale map'lerini verir. Bu hesaplama aslında ışıktan bağımsızdır yani gerçekten ışığın nereye vurduğunu nereye vurmadığını kontrol etmez. Gölgeleme işlemi çoğunlukla mesh'in kenarlarında ve çevresi bloklanan kısımlarında olur.


* #### Color (Output)
"Color" inputuna verdiginiz renk map'inin gölge vuran kısımlarının siyaha kaymış halini verir. Yani verdiginiz renkli map'e sanki gölge vurmuş gibi siyah renk efekti eklenmiş halini verir.

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
Gölgelerin maksimum yayılabileceği mesafe. Normalde gölgeler köşelerden mesh'in etrafına doğru biraz yayılır. Bu ayar ile yayılım mesafesini ayarlayabilirsiniz. Eger bu ayarı azaltırsanız gölgelerin köşeye doğru kısıtlandığını görebilirsiniz, arttırırsanız da gölgeler daha fazla yayılır.

* #### Normal (Socket Input)
Bilmiyorum.



## [Attribute](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/attribute.html)
Obje üzerinden gelen değerleri alıp kullanmamıza yarar ama artık neredeyse hiç kullanılmıyor. Henüz diğer node'lardan birinde kullanılmamış (dolayısıyla kullanıma açılmamış, test aşamasındaki) attribute'leri (bilgi, deger) almamıza yarar. Listeye [buradan](https://blender.stackexchange.com/questions/14262/what-can-you-call-from-the-attribute-node#14267) ulaşabilirsiniz.


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
Objenin ayarlarından "Color Attributes" bölümüne eklenmiş renk degerlerini almamıza yarar.


* #### Color (Output)
Renk.

* #### Alpha (Output)
Alpha degeri.

* #### Color Attribute (Node Input)
Attribute'un ismi. İsimleri bilmenize gerek yok zaten bu bölüme tıkladığınızda otomatikmen şu anki attribute'leri listeleyecektir. Ayrıca şu an seçili olan attribute silinmişse bu bölüm kırmızıya döner (deneyip görebilirsiniz).



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
Objenin yüzeyinden ne kadar ışığın yansıdığını hesaplar, yansıma miktarı fazla ise beyaza (yani 1'e) düşük ise siyaha (yani 0'a) kayan bir grayscale map verir. Yaptıgı işlemler şöyle gerçekleşir, kameranın bakış açısı ile yüzeyin bakış açısını baz alarak, aralarındaki paralellik yüksekse siyaha (yani 0'a) kayan, aralarındaki paralellik düşükse (en fazla 90 dereceye kadar) beyaza kayan (yani 1'e) grayscale map verir. Yani kameranın bakış açısı ile yüzeyin bakış açısının paralelligini kontrol eder. Bu işlem genellikle obje'nin kenarlarından ortasına doğru beyazdan siyaha kayan bir renk map'i oluşturur.


* #### Fac (Output)
Grayscale map.

* #### IOR (Socket Input)
Bu deger arttıkça output map'indeki beyaz renkler köşelerden ortaya doğru yaklaşır. Azalttıkça köşelere yaklaşır. Aslında bu deger yüzeyin [Index of Refraction](https://en.wikipedia.org/wiki/Refractive_index) degerini ayarlar, yani ışığın yönünün obje içinden geçerken kırılma derecesini.

* #### Normal (Socket Input)
Bilmiyorum.



## [Geometry](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/geometry.html)
Mesh hakkında geometrik bilgiler verir.


* #### Position (Output)
Shader render edilirken mesh üzerindeki her bir nokta için dünya üzerindeki pozisyon vektörü. Yani shader ekrana çizilirken her bir nokta için bu bilgi farklı olabilir, her bir noktaya göre bu bilgiyi verir.

* #### Normal (Output)
Shader render edilirken mesh üzerindeki her bir nokta için noktanın baktığı yön vektörü. Yani shader ekrana çizilirken her bir nokta için bu bilgi farklı olabilir, her bir noktaya göre bu bilgiyi verir.

* #### Tangent (Output)
[Tangent](#tangent) node'u ile aynı şeyi verir dolayısıyla Tangent node'una bakın. Default olarak Z eksenindeki tangent degerini verir, istediğiniz ekseni seçemezsiniz o yüzden Tangent node'unu kullanın.

* #### True Normal (Output)
"Normal" output'u ile aynıdır ama mesh'in her bir yüzü için yüzün baktığı yönü verir. Yani her bir yüz için yüze göre bu bilgiyi verir.

* #### Incoming (Output)
Shader render edilirken mesh üzerindeki her bir nokta için noktanın kameraya doğru baktığı yön vektörü. Yani shader ekrana çizilirken her bir nokta için bu bilgi farklı olabilir, her bir noktaya göre bu bilgiyi verir.

* #### Parametric (Output)
Mesh'in her bir üçgeni için (dörtgenleri de üçgene çevirir) UV degerini verir. Bu UV degeri ile bütün üçgenler üzerinde işlemler yapabilirsiniz.

* #### Backfacing (Output)
Mesh'in ön ve arka yüzünü ayırt etmek içindir. İç olan taraf için 1, dış olan taraf için 0 degeri döndürür.

* #### Pointiness (Output)
Mesh'in keskin açıları için 1'e kayan deger, düz olan kısımları için 0'a kayan deger verir.

* #### Random Per Island (Output)
Bu shader'ı kullanan her obje için birbirinden farklı olmak üzere 0 ile 1 arasında rastgele deger verir.



## [Layer Weight](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/layer_weight.html)
[Fresnel](#fresnel) gibidir. Ek olarak keskinlik ayarı da vardır. "IOR" input'u yerine "Blend" input'unu kullanır.


* #### Fresnel (Output)
[Fresnel](#fresnel) ile aynı mantıkta çalışır, Fresnel'in [Fac](#fac-output-1) output'u ile aynıdır.

* #### Facing (Output)
[Fresnel](#fresnel) ile aynı mantıkta çalışır ama daha keskindir. Fresnel yüzeyleri bir bütün gibi etkilerken bu özellik her bir noktayı etkilermiş gibi output verir. Yani noktanın baktığı yön ile kameranın baktığı yönün paralelligi birazcık azalsa hemen fark edilir. Bu da hesaplanan efektin dairesel olarak dağıldığını bile görebilmemizi sağlar (test ederek kendiniz de görebilirsiniz).

* #### Blend (Socket Input)
Fresnel efekti için keskinlik derecesini ayarlar. Degeri düştükçe fresnel efekti şiddetlenir, arttıkça fresnel efekti azalır.

* #### Normal (Socket Input)
Bilmiyorum.



## [Light Path](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/light_path.html)
Kameranın yolladığı ışık ışınları (ray) ile ilgili bilgiler verir. Evet ışınlar kameraya gelmiyor, kamera ışıklara doğru ışınlar yolluyor. Gerçek hayattaki ışığın yazılımsal olarak çalışma şekli bu (Path Tracing). Bu node'u anlatırken ışık ışınlarının (ray) farklı farklı yüzeylerden sektiğini ve kameraya ulaştığını göreceksiniz. "Path Tracing" özelliği ışık ışınının başına gelen bütün olayları kaydeder. Bu sayede ışık ışınlarının hangi yüzeylerden sektiğini bile bilebileceksiniz. Yani ışık ışınlarının sektiği yüzeylerin hangi shader türüne ait olduğu çok önemli. Aşağıdaki resime bakın.

<img src="Dosyalar/LightPath_Ray.png">


* #### Is Camera Ray (Output)
Işığın geldiği noktanın tam olarak objeye ait olup olmadığını kontrol eder. Yani eger ışık kameraya mesh üzerinden geliyorsa yani yansıma yoksa ve orijinal konum dışında bir yerden gelmiyorsa 1 döndürür, eger yansıma ile geliyorsa yani orijinal konumdan gelmiyorsa 0 döndürür. Mesela bunu kullanıp iki shader'ı birleştirirken mix faktörü olarak kullanırsanız, objeyi yeşil renk yapabilir ve obje dışındaki her şeye objeyi kırmızı olarak yansıtabilirsiniz (örnek veriyorum).

<img src="Dosyalar/IsCameraRay.png">

* #### Is Shadow Ray (Output)
Işığın geldiği noktanın gölge olan kısma ait olup olmadığını kontrol eder (hem objenin üzerindeki hem gölgenin vurduğu yerdeki). Eger ışık kameraya gölge olan kısımdan geliyorsa 1'e kayan, gölge olmayan kısımdan geliyorsa 0'a kayan deger döndürür.

* #### Is Diffuse Ray (Output)
Bunu "Is Camera Ray" ile karıştırabilirsiniz çünkü çalışma şekli ona çok benziyor, "Is Camera Ray" ışığın geldiği noktanın objeye ait olup olmadığını kontrol ederken, "Is Diffuse Ray" ışığın [Diffuse shader](#diffuse-bsdf) özelliği taşıyan bir shader'dan gelip gelmediğini (direktmen) kontrol eder.

* #### Is Glossy Ray (Output)
Işığın [Glossy shader](#glossy-bsdf) özelliği taşıyan bir shader'dan gelip gelmediğini (direktmen) kontrol eder.

* #### Is Singular Ray (Output)
Işık ışını eger tek bir yol izleyerek kameraya geliyorsa 1 degeri döndürür. Eger ışık ışını tek bir doğru yol izlemeden kameraya geliyorsa 0 degeri döndürür. Bu şu anlama geliyor, ışık ışını bir yüzeye çarptığında yüzeyin pürüzlülüğüne yani yansıtmasına göre birden fazla ışık ışını şeklinde etrafa saçılabilir veya tek bir ışık ışını şeklinde yansıyabilir. Eger yüzey çok pürüzlü ise ışık ışını çok fazla parçacığa ayrılacak ve yansıma çok bulanık olacaktır. Eger yüzey pürüzsüz ise ışık ışını tek bir parça olarak yansıyacak ve görüntü hiç bozulmamış, keskin bir halde olacaktır. İşte bu keskin yansıma yapan yüzeyler görüntüyü bozmadan yansıtırlar, yani tek bir ışık ışını şeklinde. "Is Singular Ray" özelliği de bize ışığın kameraya tek bir ışık ışını şeklinde geldiği noktaları verir. Ayna buna en iyi örneklerden biridir.

* #### Is Reflection Ray (Output)
Eger ışık ışını bir yerden sekip de kameraya geldiyse yani yansıma ise 1, degilse 0 döndürür.

* #### Is Transmission Ray (Output)
Bilmiyorum.

* #### Ray Length (Output)
Işık ışınının (ray) gittiği mesafe degeri. 0'dan başlayıp sonsuza kadar artabilir.

* #### Ray Depth (Output)
Işık ışınının (ray) toplamda kaç defa sektiğini veya kaç şeyin içinden geçtiğini gösterir. Mesela direktmen kameraya geldiyse 1 döndürür, kameranın önünde cam varsa ve camdan geldiyse 2 döndürür. Bu sayı sonsuza kadar artabilir.

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
Objenin ayarlarından ayarlanmış renk degerini verir.

* #### Alpha (Output)
Bilmiyorum.

* #### Object Index (Output)
Objenin ayarlarından ayarlanmış "pass index" degerini verir.

* #### Material Index (Output)
Objenin material ayarlarından ayarlanmış "pass index" degerini verir.

* #### Random (Output)
Bu shader'ı kullanan her obje için birbirinden farklı olmak üzere 0 ile 1 arası rastgele deger verir.



## [Particle Info](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/particle_info.html)
Bilmiyorum.



## [Point Info](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/point_info.html)
Bilmiyorum.



## [RGB](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/rgb.html)
Renk veri tipinde bir deger oluşturmanıza yarar, yani renk oluşturmanıza yarar. Oluşturduğunuz rengi renk input'u olan herhangi bir node'a bağlayabilirsiniz.



## [Tangent](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/tangent.html)
[Anisotropic BSDF](#anisotropic-bsdf) için tangent yönünü değiştirmenize yarar, isterseniz XYZ eksenlerinden birini seçebilir veya full kontrol için UV Map kullanabilirsiniz.


* #### Tangent (Output)
Tangent degeri.

* #### Direction Type (Node Input)
Mod | Açıklama
:---: | :---:
‎Radial | Normalde kullanılan dairesel tangent. İstediğiniz ekseni seçebilirsiniz.
‎UV Map | Verilen UV Map'e göre tangent şekillenir. UV Map üzerinde değişiklik yaptığınızda tangent'in de değiştiğini görebilirsiniz.



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
Kameranın bakış açısına göre texture'u yerleştirmeye yarar, nereden bakarsak bakalım aynı görünür.

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

* #### UV Map (Node Input)
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
Bu kategorideki node'lar oluşturulan shader'ın bağlandığı output node'larının olduğu kategoridir.


## [AOV Output](https://docs.blender.org/manual/en/latest/render/shader_nodes/output/aov.html)
Bilmiyorum.



## [Light Output](https://docs.blender.org/manual/en/latest/render/shader_nodes/output/light.html)
Bilmiyorum.



## [Material Output](https://docs.blender.org/manual/en/latest/render/shader_nodes/output/material.html)
Bilmiyorum.



## [World Output](https://docs.blender.org/manual/en/latest/render/shader_nodes/output/world.html)
(World moduna özeldir) Bilmiyorum.


<br>
<br>


# Shader
Bu kategorideki node'lar ana shader türlerini barındırır. Bu shader node'ları ile farklı shader türlerini kullanarak istedigimiz shader'ı yapabiliriz. En fazla kullanılan shader türü [Principled BSDF'dir](#principled-bsdf) çünkü birçok shader türünü kendi içerisinde barındırır. Principled BSDF bu kategorideki birçok shader türü node'larının yerine kullanılabilir, dolayısıyla birçok node zaten gereksiz gibi düşünebilirsiniz ama öyle degil. Bazı node'larda Principled BSDF node'unda olmayan özellikler de var, dolayısıyla bu özellikleri kullanmak için o node'lara da ihtiyacımız var.


## [Add Shader](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/add.html)
Verilen iki shader'ı toplar, birbirlerine ekler. Sonuç daha parlak olur.


* #### Shader (Output)
Sonuç shader'ı.

* #### Shader (Socket Input)
Toplanacak shader.

* #### Shader 2 (Socket Input)
Toplanacak shader.



## [Anisotropic BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/anisotropic.html)
Bilmiyorum.



## [Background](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/background.html)
(World moduna özeldir) Bilmiyorum.



## [Diffuse BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/diffuse.html)
Bilmiyorum.



## [Emission](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/emission.html)
Emission [Diffuse BSDF](#diffuse-bsdf) gibidir ama neona benzer. Emission yüzey rengini ayarlar, buna ek olarak "Strength" ayarı ile yüzey renginin şiddetini arttırabiliriz. Şiddet arttıkça renk neon gibi parlamaya başlar ve ışık saçar.


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
Camın arkasını ne kadar keskin göstereceğini etkiler. 0'da iken arkayı tam gösterir, yükselttikçe arkayı bulanık gösterir.

* #### IOR (Socket Input)
[Index of Refraction](https://en.wikipedia.org/wiki/Refractive_index) degerini ayarlar, yani ışığın yönünün camın içinden geçerken kırılma derecesini.

* #### Normal (Socket Input)
Bilmiyorum.



## [Glossy BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/glossy.html)
Ayna shader'ı oluşturmaya yarar. Yani yüzeyi ayna gibi gelen ışığı yansıtan shader oluşturur.


* #### BSDF (Output)
Shader.

* #### Mode Input (Node Input)
Buradan farklı modlar kullanarak ayna shader'ı oluşturabilirsiniz.

* #### Color (Socket Input)
Ayna rengi.

* #### Roughness (Socket Input)
Aynanın ne kadar keskin gösterecegini etkiler. 0'da iken pürüzsüz gösterir, yükselttikçe bulanık gösterir.

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
Faktör degeri, bu deger 0'a kaydıkça 1. shader, 1'e kaydıkça 2. shader kullanılır. 0.5 yaparsanız iki shader'ın ortası olur. Bu şekilde istediğiniz gibi oranlama yapabilirsiniz.

* #### Shader (Socket Input)
Karıştırılacak 1. shader.

* #### Shader 2 (Socket Input)
Karıştırılacak 2. shader.



## [Principled BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/principled.html)
Birçok shader türünün birleşimi olan tek bir shader'dır. En çok kullanılan shader budur.


* #### BSDF (Output)
Sonuç shader'ı.

* #### Distribution Mode (Node Input)
Mod | Açıklama
:---: | :---:
‎GGX | Multiscatter GGX'e göre daha hızlı ama dogruluk bakımından onun kadar dogru degil. Bunu seçerseniz "Transmission Roughness" ayarı açılır. Multiscatter GGX'e göre shader daha koyu olur.
‎Multiscatter GGX | Bu mod GGX'e göre enerjiyi daha fazla muhafaza eder. Yani ışık ışınları enerjisi bitene kadar sekmeye devam eder. Bu da daha parlak ve gerçekçi bir görünüm ile sonuçlanır. "Roughness" degeri düşük olan shader'larda ışınların sekmesi zor olacağı için etkisini de kaybeder, yani "Roughness" degeri yüksek olan shader'larda etkisi daha belli olur. Hesaplama bakımından GGX'e göre 2.5% daha yavaştır.

<img src="Dosyalar/DistributionTypes.png">

* #### Subsurface Method Mode (Node Input)
Bilmiyorum.

* #### Base Color (Socket Input)
Shader'ın ana rengi.

* #### Subsurface (Socket Input)
Bu deger arttıkça "Subsurface Scattering" etkisi de artar. "Subsurface Scattering" etkisi şudur, arkadan ışık vurunca objenin iç renginin yüzeye vurması ve yüzeyin biraz bu renge kaymasıdır. Mesela insan derisi örnek verilebilir, parmağınızı herhangi bir ışığın üstüne koyduğunuzda parmağınız kırmızı şekilde ışığı yansıtır. İşte buna "Subsurface Scattering" (SSS) deniyor.

* #### Subsurface Radius (Socket Input)
İnput olarak 3 boyutlu vektör alır. Her bir kanal kırmızı, yeşil ve mavi ışığın "Subsurface Scattering" etkisi derecesini belirler. Yani mesela default olarak verilen deger (1.0, 0.2, 0.1) dir. Bu da kırmızı ışığın daha fazla "Subsurface Scattering" etkisi yapacağını gösterir.

* #### Subsurface Color (Socket Input)
"Subsurface Scattering" etkisi için kullanılacak renk.

* #### Subsurface IOR (Socket Input)
[Index of Refraction](https://en.wikipedia.org/wiki/Refractive_index) degerini ayarlar, yani ışığın yönünün obje içinden geçerken kırılma derecesini.

* #### Subsurface Anisotropy (Socket Input)
"Subsurface Scattering" etkisi için ışığın yansıma yönünü değiştirme derecesi.

* #### Metallic (Socket Input)
Objeyi metalik hale getirir.

* #### Specular (Socket Input)
Işığı yansıtma derecesi. 0 iken hiç yansıtmaz, arttıkça daha fazla yansıtır.

* #### Specular Tint (Socket Input)
Yansıyan ışığa yüzeyin rengini verme derecesi. 0 iken yansıyan ışığın rengini degiştirmez. 1 iken yansıyan ışığa yüzeyin de rengini ekler. Yani yansıtırken kendi rengini de ekler.

* #### Roughness (Socket Input)
Objenin yüzeyinin ne kadar pürüzlü olduğunu ayarlar. 0 iken pürüzsüzdür ve yansıtma özelligi artar. 1 iken çok pürüzlüdür ve yansıtma özelligi azalır.

* #### Anisotropic (Socket Input)
"Anisotropic" ve "Anisotropic Rotation" ayarları ışığın yansıtma yönünü değiştirmek ile ilgilidir. "Anisotropic Rotation" ayarı yönü degiştirir. "Anisotropic" ayarı ise bu yön degiştirmenin ne kadar etkili olacağını belirler.

* #### Anisotropic Rotation (Socket Input)
"Anisotropic" ve "Anisotropic Rotation" ayarları ışığın yansıtma yönünü değiştirmek ile ilgilidir. "Anisotropic Rotation" ayarı yönü degiştirir. "Anisotropic" ayarı ise bu yön degiştirmenin ne kadar etkili olacağını belirler.

* #### Sheen (Socket Input)
Bu ayar genellikle giysi tarzı shader'larda kullanılıyor. Kenarlara ışığın yansımasından dolayı parlaklık efekti ekler.

* #### Sheen Tint (Socket Input)
Aynı "Specular Tint" gibi, "Sheen" etkisinin verdigi parlaklığa yüzeyin de rengini eklemesine sebep olur.

* #### Clearcoat (Socket Input)
Clearcoat sanki yüzey bir şey ile kaplanmış gibi görünmesine sebep olur. İkincil bir yüzey oluşturur. Araba boyası gibi.

* #### Clearcoat Roughness (Socket Input)
"Clearcoat" için Roughness degeri.

* #### IOR (Socket Input)
[Index of Refraction](https://en.wikipedia.org/wiki/Refractive_index) degerini ayarlar, yani ışığın yönünün obje içinden geçerken kırılma derecesini. [Buradan](https://pixelandpoly.com/ior.html) gerçek hayattaki birçok materyalin IOR degerine ulaşabilirsiniz.

* #### Transmission (Socket Input)
Objeyi saydam yapar.

* #### Transmission Roughness (Socket Input)
Transmission için Roughness degeri.

* #### Emission (Socket Input)
Emission ayarı Base Color gibidir. Yüzey rengini ayarlar. "Emission Strength" ayarı ile yüzey renginin şiddetini arttırabiliriz. Şiddet arttıkça renk neon gibi parlamaya başlar ve ışık saçar.

* #### Emission Strength (Socket Input)
Emission şiddeti.

* #### Alpha (Socket Input)
asd

* #### Normal (Socket Input)
Bu ayar sayesinde yüzeydeki noktalar için sahte yükseklik verebilirsiniz. Yani aslında yüksekligi olmayan yüzeyleri sanki yükseklikleri varmış gibi gösterebilirsiniz.

* #### Clearcoat Normal (Socket Input)
"Clearcoat" için Normal verebilmemize yarar.

* #### Tangent (Socket Input)
asd



## [Principled Hair BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/hair_principled.html)
Bilmiyorum.


* #### BSDF (Output)
Sonuç shader'ı.



## [Principled Volume](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/volume_principled.html)
Bilmiyorum.


* #### BSDF (Output)
Sonuç shader'ı.



## [Refraction BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/refraction.html)
Cam shader'ı oluşturmamıza yarar.


* #### BSDF (Output)
Sonuç shader'ı.

* #### Distribution Mode (Node Input)
Mod | Açıklama
:---: | :---:
‎Sharp | Beckmann ve GGX'in aksine "Roughness" input'undan bağımsız olarak arkayı keskin gösterir.
Beckmann | GGX'e göre koyu kısımları daha dogru gösterir. Test edip kendiniz görmelisiniz.
GGX | Beckmann'e göre koyu kısımları daha az gösterir. Test edip kendiniz görmelisiniz.

* #### Color (Socket Input)
Cam rengi.

* #### Roughness (Socket Input)
Camın arkasını ne kadar keskin gösterecegini etkiler. 0'da iken arkayı tam gösterir, yükselttikçe arkayı bulanık gösterir.

* #### IOR (Socket Input)
[Index of Refraction](https://en.wikipedia.org/wiki/Refractive_index) degerini ayarlar, yani ışığın yönünün camın içinden geçerken kırılma derecesini.

* #### Normal (Socket Input)
Bilmiyorum.



## [Subsurface Scattering](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/sss.html)
"Subsurface Scattering" etkisi oluşturmanıza yarar. "Subsurface Scattering" etkisi şudur, arkadan ışık vurunca objenin iç renginin yüzeye vurması ve yüzeyin biraz bu renge kaymasıdır. Mesela insan derisi örnek verilebilir, parmağınızı herhangi bir ışığın üstüne koyduğunuzda parmağınız kırmızı şekilde ışığı yansıtır. İşte buna "Subsurface Scattering" (SSS) deniyor.


* #### BSSRDF (Output)
Sonuç shader'ı.

* #### Subsurface Method (Node Input)
Mod | Açıklama
:---: | :---:
‎a | a

* #### Color (Socket Input)
"Subsurface Scattering" etkisi için kullanılacak renk.

* #### Scale (Socket Input)
"Subsurface Scattering" etkisi derecesi.

* #### Radius (Socket Input)
İnput olarak 3 boyutlu vektör alır. Her bir kanal kırmızı, yeşil ve mavi ışığın "Subsurface Scattering" etkisi derecesini belirler. Yani mesela default olarak verilen deger (1.0, 0.2, 0.1) dir. Bu da kırmızı ışığın daha fazla "Subsurface Scattering" etkisi yapacağını gösterir.

* #### IOR (Socket Input)
[Index of Refraction](https://en.wikipedia.org/wiki/Refractive_index) degerini ayarlar, yani ışığın yönünün obje içinden geçerken kırılma derecesini.

* #### Anisotropy (Socket Input)
"Subsurface Scattering" etkisi için ışığın yansıma yönünü değiştirme derecesi.

* #### Normal (Socket Input)
Bilmiyorum.



## [Toon BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/toon.html)
Yansımaları keskin bir şekilde hesaplayan bir shader türüdür. Çizgi film tarzı, çok detaya kaçmadan olabildiğince sade bir şekilde görünüm verir. Keskinligini Smooth input'u ile ayarlayabilirsiniz.


* #### BSDF (Output)
Sonuç shader'ı.

* #### Component Mode (Node Input)
Mod | Açıklama
:---: | :---:
‎Diffuse | [Diffuse BSDF](#diffuse-bsdf) türünde shader kullanır. Yani tek renk.
Glossy | [Glossy BSDF](#glossy-bsdf) türünde shader kullanır. Yani ayna gibi.

* #### Color (Socket Input)
Ana renk.

* #### Size (Socket Input)
Yansımaların boyutu.

* #### Smooth (Socket Input)
Keskinliği azaltır, yumuşaklık ekler. 0'da iken yansımalar keskin, arttıkça daha yumuşak olur.



## [Translucent BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/translucent.html)
Objeye saydamlık ekler. Saydam obje ışığı geçirebilir. Işık vurdugu zaman objenin yüzeyinde ışığın etkisini görebilirsiniz.


* #### BSDF (Output)
Sonuç shader'ı.

* #### Color (Socket Input)
Ana renk.

* #### Normal (Socket Input)
Bilmiyorum.



## [Transparent BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/transparent.html)
Objeyi görünmez yapar.


* #### BSDF (Output)
Sonuç shader'ı.

* #### Color (Socket Input)
Ana renk. Eger renk beyaz olursa yani (1, 1, 1) tamamen görünmez olur. Eger herhangi bir renk verirseniz o renkte görünür.



## [Velvet BSDF](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/velvet.html)
Objeye yansımalar ekler, sanki giysi tarzı maddelerin shader'ı gibi.


* #### BSDF (Output)
Sonuç shader'ı.

* #### Color (Socket Input)
Ana renk.

* #### Sigma (Socket Input)
Yansıma ekleme derecesi, arttırdıkça daha fazla yansıma ekler.

* #### Normal (Socket Input)
Bilmiyorum.



## [Volume Absorption](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/volume_absorption.html)
[Volume Absorption](#volume-absorption) ile [Volume Scatter](#volume-scatter) birbirlerine benzerlerdir, dolayısıyla bu ikisinin açıklamalarını dikkatli okuyup aralarındaki farkları anlamak gerekli. Volume Absorption içinden geçen ışığı emer. Bu da sanki renkli gözlük takmış ve gözlükten bakıyormuşsunuz gibi veya ışık renkli bir camdan geçiyormuş gibi efekt verir ve bu camın emme gücü ile rengini ayarlayabilirsiniz.


* #### Volume (Output)
Sonuç shader'ı.

* #### Color (Socket Input)
Ana renk.

* #### Density (Socket Input)
Alanının yoğunluğu.



## [Volume Scatter](https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/volume_scatter.html)
[Volume Absorption](#volume-absorption) ile [Volume Scatter](#volume-scatter) birbirlerine benzerlerdir, dolayısıyla bu ikisinin açıklamalarını dikkatli okuyup aralarındaki farkları anlamak gerekli. Volume Scatter içinden geçen ışığı farklı yönlere dağıtır. Bu da sanki orada bir alan varmış gibi efekt verir, mesela duman efekti gibi veya toz efekti gibi. Bu alanın rengini ve yoğunluğunu ayarlayabilirsiniz.


* #### Volume (Output)
Sonuç shader'ı.

* #### Color (Socket Input)
Ana renk.

* #### Density (Socket Input)
Alanının yoğunluğu.

* #### Anisotropy (Socket Input)
Bu ayar alanın içinden geçen ışığın dağılacağı yönü ayarlar. 0 iken eşit şekilde etrafa dağılır, artılara gittikçe öne doğru, eksilere gittikçe arkaya doğru dağılır.


