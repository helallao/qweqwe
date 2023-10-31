# Ek Bilgiler

<details>
<summary>Kullanılan Güzel Kaynaklar</summary>
<br>

* [The Blender 2.8 Encyclopedia](https://www.udemy.com/course/the-blender-encyclopedia/) - Udemy'deki sayısı bir elin parmaklarını geçmeyecek kadar az olan, gerçekten uğraşılmış kurslardan birisi. Bizim için önemli olan 9. bölüm "Modifiers", modifier'ların açıklamalarının olduğu bölüm, tabi isterseniz diğer kısımlara da bakabilirsiniz. [Buradan](https://btdig.com/search?q=The+Blender+2.8+Encyclopedia) torrent'ini bulabilirsiniz (vpn gerekebilir).
* [All Modifiers in Blender](https://brandonsdrawings.com/modifiers/) - Brandon's Drawings'in sitesi. Kendisi blender hakkında en iyi kaynaklardan birisidir.

</details>



# [Modify](#modify-1)
* [Data Transfer](#data-transfer)
* [Mesh Cache](#mesh-cache)
* [Mesh Sequence Cache](#mesh-sequence-cache)
* [Normal Edit](#normal-edit)
* [Weighted Normal](#weighted-normal)
* [UV Project](#uv-project)
* [UV Warp](#uv-warp)
* [Vertex Weight Edit](#vertex-weight-edit)
* [Vertex Weight Mix](#vertex-weight-mix)
* [Vertex Weight Proximity](#vertex-weight-proximity)

# [Generate](#generate-1)
* [Array](#array)
* [Bevel](#bevel)
* [Boolean](#boolean)
* [Build](#build)
* [Decimate](#decimate)
* [Edge Split](#edge-split)
* [Geometry Nodes](#geometry-nodes)
* [Mask](#mask)
* [Mirror](#mirror)
* [Multiresolution](#multiresolution)
* [Remesh](#remesh)
* [Screw](#screw)
* [Skin](#skin)
* [Solidify](#solidify)
* [Subdivision Surface](#subdivision-surface)
* [Triangulate](#triangulate-1)
* [Volume to Mesh](#volume-to-mesh)
* [Weld](#weld)


<br>
<br>


# [Modify]()
Bu kategorideki modfier'lar objenin geometrisini direktmen değiştirmeyen, daha çok objelerin verisini değiştiren modifier'lardır.


## [Data Transfer](https://docs.blender.org/manual/en/3.6/modeling/modifiers/modify/data_transfer.html)
Bilmiyorum.


## [Mesh Cache](https://docs.blender.org/manual/en/3.6/modeling/modifiers/modify/mesh_cache.html)
Bilmiyorum.


## [Mesh Sequence Cache](https://docs.blender.org/manual/en/3.6/modeling/modifiers/modify/mesh_sequence_cache.html)
Bilmiyorum.


## [Normal Edit](https://docs.blender.org/manual/en/3.6/modeling/modifiers/modify/normal_edit.html)
Bilmiyorum.


## [Weighted Normal](https://docs.blender.org/manual/en/3.6/modeling/modifiers/modify/weighted_normal.html)
Bilmiyorum.


## [UV Project](https://docs.blender.org/manual/en/3.6/modeling/modifiers/modify/uv_project.html)
Bilmiyorum.


## [UV Warp](https://docs.blender.org/manual/en/3.6/modeling/modifiers/modify/uv_warp.html)
Bilmiyorum.


## [Vertex Weight Edit](https://docs.blender.org/manual/en/3.6/modeling/modifiers/modify/weight_edit.html)
Bilmiyorum.


## [Vertex Weight Mix](https://docs.blender.org/manual/en/3.6/modeling/modifiers/modify/weight_mix.html)
Bilmiyorum.


## [Vertex Weight Proximity](https://docs.blender.org/manual/en/3.6/modeling/modifiers/modify/weight_proximity.html)
Bilmiyorum.


<br>
<br>


# [Generate]()
Bu kategorideki modfier'lar objenin geometrisini direktmen değiştirmeyen, daha çok objelerin verisini değiştiren modifier'lardır.


## [Array](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/array.html)
Objeyi istediğiniz sayıda ve yönde kopyalar (aynı veriyi paylaşan kopyalar oluşturur).


* #### Fit Type
Yerleştirme türü.

Mod | Açıklama
:---: | :---:
‎Fixed Count | "Count" input'una verdiğiniz sayı kadar kopya oluşturulur.
Fit Length | "Length" input'unda belirttiğiniz mesafe değerine göre, verdiğiniz offset ile kaç tane kopya sığıyorsa o kadar kopya oluşturur. Bu modda offset kullanmak zorundasınız.
Fit Curve | "Curve" input'unda belirttiğiniz curve'ün uzunluk değerine göre, verdiğiniz offset ile kaç tane kopya sığıyorsa o kadar kopya oluşturur. Bu modda offset kullanmak zorundasınız.


## Relative Offset
Objenin kendi boyut değerlerine göre offset verir.

* #### Factor X/Y/Z
Her bir kopyanın bir önceki kopyaya olan offset'i yani uzaklığı, "Relative Offset" yani objenin kendi boyut değerlerine göre offset olduğu için, mesela herhangi bir ekseni 2 ayarlamak o eksende her kopyanın arasına objenin kendisi kadar boşluk konulmasına sebep olur.


## Constant Offset
Belirttiğiniz değere göre offset verir.

* #### Distance X/Y/Z
Her bir kopyanın bir önceki kopyaya olan offset'i yani uzaklığı, "Constant Offset" yani belirttiğiniz offset değeri objenin büyüklüğünden bağımsız olarak kullanılır.


## Object Offset
Belirttiğiniz objeye göre offset verir. Bu modu sürekli küçülen kopyalar oluşturmak için veya belirli bir nokta etrafında kopyalar oluşturmak için kullanabilirsiniz.

* #### Object
Referans objesi, offset bu objenin transform değerlerine göre (location, rotation, scale) hesaplanır.


## Merge
Belirtilen mesafe değerinden küçük offset'e sahip olan kopyaları birleştirmeye yarar.

* #### Distance
Mesafe değeri, eğer bir önceki ve sonraki kopyalar arasındaki mesafe bu değerden küçükse vertice'leri birleştirilir.

* #### First and Last Copies
Bu ayarı açarak ilk ve son kopyaları birleştirebilirsiniz (tabi eğer aralarındaki mesafe "Distance" input'undan küçükse). Bu ayarı daire oluşturup tekrar başlangıç noktasına gelen kopyalarda kullanabilirsiniz.


## UVs
Offset U/V ayarları ile UV kaydırmanıza yarar.

* #### Offset U/V
X ve Y daha doğru U ve V eksenlerinde yeni oluşturulan kopyalar için UV'yi kaydırır. Eğer her kopyada farklı UV kullanılsın istiyorsanız bunu kullanabilirsiniz.


## Caps
Eğer kopyalar başlarken veya bitince koymak istediğiniz bir obje varsa bu ayarı kullanabilirsiniz.

* #### Cap Start/End
Bu ayarlar ile başlangıca ve sona (her kopya için değil, hepsinden önce ve sonra) koymak istediğiniz objeleri seçebilirsiniz. Mesela tren rayı yaptınız ve başlangıç ile bitişe duvar koymak istiyorsunuz, o zaman bu ayarı kullanabilirsiniz.



## [Bevel](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/bevel.html)
Bildiğimiz bevel tool'unun modifier halidir. Daha gelişmiş özellik sunar. Eğer bevel tool'unu bilmiyorsanız internetten ilk baş onu ögrenin. Zaten ayarların çoğu bevel tool'undaki ayarlar ile aynı.


* #### Width Type
Bevel derecesini belirleyen modlardır.

Mod | Açıklama
:---: | :---:
‎Offset | Kenarın face'ler üzerinde kenardan uzaklaşması olarak hesaplanır (resme bakın).
‎Width | Bevel kenarlarının birbirlerinden uzaklaşması olarak hesaplanır, yani aralarındaki mesafe (resme bakın).
Depth | Derinlik yani kenarların içe doğru uzaklaşması olarak hesaplanır (resme bakın).
Percent | Face'lerin uzunluğuna göre yüzdelik olarak bevel hesaplanır. Eğer objenin yüzlerinin boyutu farklı ise, bevel derecesinin de farklı olduğunu görebilirsiniz. Mesela bir dikdörtgen üzerinde bevel modifier uygularsanız kenar'ın uzun olan face'ine daha geniş bevel uygulanmışken kısa olan face'ine daha dar bevel uygulandığını görebilirsiniz.
Absolute | Tam olarak verdiğiniz değere göre bevel hesaplanır.

<img src="../../Dosyalar/Modifiers_Bevel_WidthTypes.png" width="300">

* #### Amount
Bevel miktarı, "Width Type" ayarına göre bu ayarın çalışma mantığı değişebilir.

* #### Segments
Segment sayısı. Bu ayar zaten bevel tool'unda da var.

* #### Limit Method
Bevel işlemini limitlememize yarayan modlardır.

Mod | Açıklama
:---: | :---:
‎None | Limit yok.
Angle | Kenarın face'ler arasındaki açısına göre limit kullanır. "Angle" input'una veridiğiniz açıdan az açıya sahip olan kenarlara bevel uygulanmaz.
Weight | Kenarların "Bevel Weight" bilgisini kullanır.
Vertex Group | Eğer kenarı oluşturan vertex'lerin hepsi "Vertex Group" input'una verilen vertex group'ta ise bevel uygulanır.


## Profile
Buradan bevel şeklini belirleyebilirsiniz.

Mod | Açıklama
:---: | :---:
‎Superellipse | Default mod. "Shape" input'unun değerini arttırıp azaltarak bevel derecesini belirleyebilirsiniz.
Custom | Bevel şeklini curve aracılığı ile belirleyebilirsiniz.

* #### Sample Straight Edges
Sadece "Profile" ayarı "Custom" modundayken vardır. Curve üzerindeki bütün noktaların handling type'ını yani önceki ve sonraki noktalara bağlanma modlarını vector'e çevirir. Yani noktalar birbirine direktmen bağlanır, ama bu curve üzerinde görünmez. Eğer bevel edilen kenarlara bakarsanız görebilirsiniz.

* #### Sample Even Lengths
Sadece "Profile" ayarı "Custom" modundayken vardır. Curve üzerindeki bütün noktaları eşit dağıtır. Aralarındaki mesafe eşit olur.


## Geometry
Bevel ile ilgili şekil ayarları.

* #### Miter Inner/Outer
Bu ayarlar bevel şekli ile ilgili. [Buradan](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/bevel.html#id8) modların yaptığı değişiklikleri görebilirsiniz.

* #### Spread
Sadece "Miter Inner" ayarı "Arc" modundayken vardır. Ekstra vertice'leri yayma derecesini belirler.

* #### Intersections
"Grid Fill" modu default moddur. "Cutoff" modu bevel edilmiş kenarların birbiriyle birleştikleri kısmı siler.

* #### Clamp Overlap
Kenarların bevel edilen kısımlarının birbirleriyle çakışmasını engeller. Çakışmanın başladığı noktada bevel genişliğini durdurur.

* #### Loop Slide
Bevel edilen kenarlardan bazılarının bağlı olduğu face'lerin boyutu farklı olduğu için sünme oluyorsa bu ayarı açarak bütün kenarlardaki bevel'ları eşitleyebilirsiniz. Güzel video bulamadım ama [buna](https://youtu.be/vLzY4ApZZcE?t=907) bakabilirsiniz.


## Shading
Bevel ile ilgili shading ayarları.

* #### Harden Normals
Oluşturulan bevel face'lerinin normal'larını yani baktıkları yönleri düzenler. Shading sorunlarını çözer.

* #### Mark Seam
Bilmiyorum.

* #### Mark Sharp
Bilmiyorum.

* #### Material Index
Bevel ile oluşturulan kenarlar için Materials bölümündeki (Properties > Material) materyallerden hangisinin kullanılacağını belirler. -1 yaparsanız otomatik olarak materyal atanır yani bevel ile oluşturulan kenarlara objenin bevel olmadan önceki halinde en yakın olan face'in rengi verilir. Bu sayıyı 0 veya daha büyük bir sayı yaparsanız index belitmiş olursunuz, yani Materials bölümündeki (Properties > Material) materyallerden birini seçmiş olursunuz. 0 yaparsanız ilk, 1 yaparsanız 2. materyal kullanılır ve bu şekilde verdiğiniz index'teki materyal kullanılır. Index sayıları yazılım dillerinde 0'dan başlar.

* #### Face Strength
Bilmiyorum.



## [Boolean](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/booleans.html)
Başka bir objeyi kullanarak seçilen obje ile üst üste gelen kısımlar üzerinde işlemler yapabilirsiniz. Mesela kesiştikleri kısmı silebilirsiniz. Bu modifier'ı kullanırsanız mesh'iniz üzerinde n-gon'lar oluşabilir, mesh'inizin topolojisini bozabilir. Sadece basit mesh'ler için kullanın, kompleks mesh'lerinizde bu modifier'ı kullanmak kolaylık değil zorluk getirebilir.


* #### Operation
İşlem.

Mod | Açıklama
:---: | :---:
‎Intersect | Modifier uygulanan objenin, diğer obje ile kesişen kısmı kalır, geriye kalan her yeri silinir.
Union | İki obje birleştirilir.
Difference | Modifier uygulanan objenin, diğer obje ile kesişen kısmı silinir. Yani diğer obje silici olarak kullanılır.

* #### Operand Type
Kullanılacak objenin türü. "Object" modunda tek bir obje belirtebilirsiniz. "Collection" modunda koleksiyon belirtebilirsiniz ve bu koleksiyondaki bütün objeler kullanılır.

* #### Object/Collection
Hedef obje/koleksiyon.

* #### Solver
Hesaplama algoritması.

Mod | Açıklama
:---: | :---:
‎Fast | Hızlı ama tam doğru hesaplama sunmaz.
Exact | "Fast" moduna göre daha yavaş ama hesaplamalar doğru.

* #### Overlap Threshold
Sadece "Solver" ayarı "Fast" modundayken vardır. İki face'in üst üste gelmiş olabilmesi için maximum mesafe değeri. Yani iki face'in aralarındaki mesafe bu değerden az ise üst üste gelmişler demektir.

* #### Materials
"Index Based" modunda yeni oluşturulan yüzler için Materials bölümündeki (Properties > Material) materyalleri sırasıyla kullanır. Eğer yeterli materyal yoksa sonuncuyu kullanır. "Transfer" modunda varsa hedef obje olarak kullanılan objenin materyalini, yoksa "Index Based" gibi modifier uygulanan objenin materyallerini kullanır.

* #### Self Intersection
Hedef objenin kendisi üzerinde üst üste gelen kısımlarını da hesaplar. Bu ayarı açmak hataları önleyebilir ama ek hesaplama yapar.

* #### Hole Tolerant
Eğer "Solver" ayarı olarak "Exact" kullanıyorsanız ve sonuç hatalı oluyorsa bu ayarı açabilirsiniz. Bu ayarı açmak [Non-manifold](https://docs.blender.org/manual/en/3.6/glossary/index.html#term-Non-manifold) yani hatalı yapılmış yüzeyleri optimize eder. Ek hesaplama yaptığı için yavaş olabilir.



## [Build](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/build.html)
Bu modifier objeye animasyonlu build efekti (inşa etme) verir. Belirtilen frame sayısına göre her frame'de objenin face'lerini görünmez halden görünür hale getirir. Bu da sanki obje yeniden oluşuyormuş gibi bir efekt verir. Ayrıca genellikle Build modifier'ı kullanıcı tarafından belirlenmiş face sıralamasına göre kullanılır. Face sıralamasını (Sort Order) nasıl yapacağınızı [buradan](https://brandonsdrawings.com/buildmodifier/) ögrenebilirsiniz.


* #### Start Frame
Animasyonun başlama frame'i. Mesela bunu 50 yaparsanız 50. frame'den sonra obje oluşmaya başlar.

* #### Length
Animasyonun kaç frame süreceğini belirler. Mesela 100 yaparsak inşa etme animasyonu 100 frame sürer.

* #### Reversed
İşlemi tersine çevirir, inşa etmek yerine yok eder. Başlangıçta tamamen görünür olan obje gitgide yok olur veya görünmez olur.

* #### Randomize
Face'lerin oluşma veya yok olma sıralamasını rastgele yapar.

* #### Seed
"Randomize" ayarı için seed değeri. Seed demek verilen sayıya göre işlemlerin bilgisayarda o sayıya özel olarak rastgele gerçekleşmesi demektir. Aynı seed'i kullandığınızda hep aynı sonucu alırsınız.



## [Decimate](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/decimate.html)
Bu modifier mesh üzerindeki vertex/face sayısını düşürmenize yarar.


* #### Mode

Mod | Açıklama
:---: | :---:
‎Collapse | Birbirine yakın olan vertex'leri birleştirir.
Un-Subdivide | Subdivision yani face'leri bölme işleminin tam tersini yapar, face'leri birleştirir. "Iterations" input'una verdiğiniz sayı kadar bölme işlemi gerçekleşir.
Planar | Aralarındaki açı verdiğiniz açı değerinden az olan komşu face'leri birleştirir. Yani yönleri birbirine benzeyen face'leri birbirleriyle birleştirir.

* #### Ratio
Sadece "Mode" ayarı "Collapse" modundayken vardır. Vertex sayısını düşürme derecesini belirler. 1'den 0'a doğru indikçe vertex sayısı %100'den %0'a doğru azalır.

* #### Symmetry
Sadece "Mode" ayarı "Collapse" modundayken vardır. Seçilen eksende simetriyi korur.

* #### Triangulate
Sadece "Mode" ayarı "Collapse" modundayken vardır. Bütün face'leri üçgene çevirir.

* #### Vertex Group
Sadece "Mode" ayarı "Collapse" modundayken vardır. Decimate modifier'ı belirli bir vertex group ile sınırlayabilirsiniz.

* #### Factor
Sadece "Mode" ayarı "Collapse" modundayken vardır. "Vertex Group" için etki derecesi.

* #### Angle Limit
Sadece "Mode" ayarı "Planar" modundayken vardır. Açı limiti, aralarındaki açı bu açıdan küçük olan komşu face'ler birleştirilir.

* #### Delimit
Sadece "Mode" ayarı "Planar" modundayken vardır. Belirli yerleri Decimate işleminin dışında bırakabilirsiniz.

Mod | Açıklama
:---: | :---:
‎Normal | Normal'ları farklı yönlere bakan (ön/arka) face'leri Decimate işleminin dışında bırakır.
Material | Farklı materyale sahip face'leri Decimate işleminin dışında bırakır.
Seam | Seam olarak işaretlenmiş kenarları Decimate işleminin dışında bırakır.
Sharp | Sharp olarak işaretlenmiş kenarları Decimate işleminin dışında bırakır.
UVs | UV Map'te olan kenarları Decimate işleminin dışında bırakır.

* #### All Boundaries
Sadece "Mode" ayarı "Planar" modundayken vardır. Bu ayar face'lerin boundary (sınırları) yani kenarları üzerindeki bütün vertice'leri siler. Yani bir nevi n-gon oluşmasına engel olur da denebilir.



## [Edge Split](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/edge_split.html)
Bu modifier mesh'in kenarlarını birbirinden ayırır, daha doğrusu face'leri birbirine bağlayan kenarları ayırır da denebilir çünkü kenarları ayırırken komşu face'lern birbirlerine olan açı farkına bakar. Bu modifier ile yapabildiklerinizin aynısını Auto Smooth (Properties > Data > Normals > Auto Smooth) ayarı ile de yapabilirsiniz, dolayısıyla artık kullanılmıyor, ek bilgiler için [buraya](https://www.youtube.com/watch?v=xMI3G_M_3dE) bakabilirsiniz.


* #### Edge Angle
Aralarındaki açı bu açı değerinden fazla olan kenarlar birbirlerinden ayrılır.

* #### Sharp Edges
"Sharp" olarak işaretlenmiş kenarların açıları "Edge Angle" ayarında verdiğiniz açıdan küçük olsalar bile ayrılırlar.



## [Geometry Nodes](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/geometry_nodes.html)
Bilmiyorum.



## [Mask](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/mask.html)
Bu modifier mesh'in sadece seçilen vertex group'unu veya seçilen armature'a bağlı olan kısmını gösterir, diğer kısımları göstermez. Bu modifier'ı debug aracı olarak kullanabilirsiniz.


* #### Mode
Mod.

Mod | Açıklama
:---: | :---:
‎Vertex Group | Sadece verdiğiniz vertex group'u gösterir. Ayrıca weight değerlerine göre eleme de yapabilirsiniz.
‎Armature | Mesh'in sadece verdiğiniz armature'a bağlı olan kısımlarını gösterir. Ayrıca weight değerlerine göre eleme de yapabilirsiniz.

* #### Smooth
Sadece "Mode" ayarı "Vertex Group" modunda iken vardır. Weight değerleri birbirine yakın olan kısımlar için yumuşak bir geçiş efekti verir. Yani tam olarak "Threshold" değerinden büyük olan yerleri göstermek yerine bölgedeki weight değerlerini ortalayıp keskin geçişleri yumuşak geçişe çevirir.

* #### Threshold
Weight değerleri için limit değeri. Vertex Group'un veya seçilen armature'un içinde olan vertex'lerin weight değeri bu değerden büyükse vertex gösterilir, küçükse veya eşitse gösterilmez.



## [Mirror](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/mirror.html)
Bu modifier mesh'i istediğiniz eksende aynalamanıza yarar, mesela yapmak istediğiniz obje simetrik ise sadece yarısını yapıp diğer yarısını da bu modifier ile yapabilirsiniz. Default olarak mesh'in orijin noktasını kullanır.


* #### Axis
Aynalama işleminin olacağı eksen.

* #### Bisect
Aynalama işlemi olurken mesh orijin noktasından karşı tarafa geçerse, yani aynalanan kısma geçerse, orijin noktasını geçen kısımlar otomatikmen silinir.

<img src="../../Dosyalar/Modifiers_Mirror_Bisect.gif" width="400">

* #### Flip
Aynalama yönünü değiştirir, "Bisect" ayarı açıkken bu ayarı da açarsanız yönler değişir, aynalama yönü tam tersi olur. Eğer aynalama yönünün tersten olmasını istiyorsanız bu ayarı kullanabilirsiniz.

* #### Mirror Object
Orijin noktası olarak başka bir objenin transform bilgilerini (location, rotation) kullanmanıza yarar.

* #### Clipping
Mesh'in edit modda orijin noktasını geçen kısımları orijin noktasına geldikten sonra daha fazla ilerleyemez. Yani bu ayar mesh'in orijin noktasının karşısına geçmesine izin vermez.

* #### Merge
Mesh ile aynalanan kopyanın vertice'lerinin arasındaki mesafe bu ayara verdiğiniz değerden küçükse otomatikmen birleştirilir.

* #### Bisect Distance
"Bisect" ayarı için mesafe değeri. Orijin noktasına bu ayara verdiğiniz değerden daha yakın olan vertice'ler bisect edilir. Yani orijin noktasında birleştirilir.


## Data

* #### Mirror U/V
Bilmiyorum.

* #### Offset U/V
Bilmiyorum.

* #### Vertex Groups
Bilmiyorum.

* #### Flip UDIM
Bilmiyorum.



## [Multiresolution](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/multiresolution.html)
Bilmiyorum.



## [Remesh](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/remesh.html)
Bu modifier mesh'i quad'lar yani dörtgenler kullanarak yeniden oluşturur.


* #### Mode
Mod.

Mod | Açıklama
:---: | :---:
‎Blocks | Mesh'i minecraft gibi küp küp yapar.
Smooth | Dörtgenler arası yumuşak geçişler yapar. Yumuşak bir şekil verir.
Sharp | "Smooth" modu gibidir ama keskin kısımları/köşeleri tutar.
Voxel | Mesh'i voxel'ler ile yeniden oluşturur.

* #### Octree Depth
Quad yani dörtgen sayısı/miktarı.

* #### Scale
Quad yani dörtgen sayısının/miktarının genel olarak scale değeri, dörtgenlerin büyüklüğünü ayarlar da denebilir.

* #### Sharpness
Sadece "Mode" ayarı "Sharp" modundayken vardır. Keskinlik derecesi.

* #### Remove Disconnected
Ana mesh'e bağlı olmayan kısımları silmeye yarar.

* #### Threshold
"Remove Disconnected" ayarı için threshold yani limit değeri. Silinecek kısımların ne kadar büyük olması gerektiğini belirtir.

* #### Smooth Shading
Mesh'e smooth shade uygular.

* #### Voxel Size
Sadece "Mode" ayarı "Voxel" modundayken vardır. Voxel büyüklüğünü ayarlar. Düşürdükçe daha çok voxel olacağı için detay artar ama face sayısı da artar.

* #### Adaptivity
Sadece "Mode" ayarı "Voxel" modundayken vardır. Bu ayar da aslında "Voxel Size" ayarı gibi voxel büyüklüğünü ayarlar ama bu ayarı voxel büyüklüğünü ayarlıyormuş gibi değil de voxel'leri birleştiriyormuş gibi düşünün. Yani bu ayarı arttırdıkça voxel'ler birleşir, böylelikle de voxel yani face sayısı düşmüş olur.



## [Screw](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/screw.html)
Bu modifier spin tool'unun modifier hali gibidir. Yaptıkları iş bakımından aynıdırlar denebilir.


* #### Angle
Orijin noktası etrafında seçilen eksende dönme derecesi.

* #### Screw
Seçilen eksende yükseklik değeri.

* #### Iterations
Tekrar etme sayısı. Bu sayıyı arttırarak oluşturduğunuz meshi tekrar edebilirsiniz. Her bir tekrar yani iteration uç uca eklenir.

* #### Axis
Dönme ekseni.

* #### Axis Object
Buradan obje seçerek orijin noktasını bu objeye göre belirleyebilirsiniz.

* #### Object Screw
Eğer bu ayarı açarsanız "Screw" input'u kapanır ve "Screw" değeri olarak verdiğiniz obje ile modifier'ın uygulandığı objenin "Axis" input'unda verdiğiniz eksendeki farkları kullanılır.

* #### Steps Viewport
Viewport için objenin step yani köşe sayısı.

* #### Steps Render
Render için objenin step yani köşe sayısı.

* #### Merge
Birbirine yakın olan vertice'leri birleştirmemize yarar. Buradan limiti ayarlayabilirsiniz. Ararlarındaki fark bu limit değerinden az olan vertice'ler birleştirilir.

* #### Stretch UVs
Eğer bu ayarı açarsanız seçtiğiniz eksende (U veya V) mesh'in UV'sini sündürür. Normalde mesh uzadıkça veya boyutu arttırkça U ve V eksenlerindeki UV değeri de tekrarlamaya başlar ama bu ayarı açarsanız tekrarlama değil de sıkıştırma işlemi uygulanır yani UV sündürülür ve mesh boyutuna göre şekillenir.


## Normals

* #### Smooth Shading
Mesh'e smooth shade uygular.

* #### Calculate Order
Kenarların sırasına göre normal'larını düzenler. Düzgün normal'lar için bu ayarı açın.

* #### Flip
Normal'ların yönünü tersine çevirir.



## [Skin](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/skin.html)
Bilmiyorum.



## [Solidify](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/solidify.html)
Solidify modifier'ı mesh'e kalınlık/derinlik ekler.


* #### Mode
Mod.

Mod | Açıklama
:---: | :---:
‎Simple | Default mod. Tek bir kenarın 2'den fazla bağlı olduğu face olduğunda hata verebilir.
Complex | Her türlü geometri için kesin sonuç sunar. Hesaplamalar daha fazla olduğu için bu modu seçmek yavaşlık ekleyebilir ama kesin sonuç döndürür.

* #### Thickness Mode
Sadece "Mode" ayarı "Complex" modundayken vardır.

Mod | Açıklama
:---: | :---:
‎Fixed | Bu mod, "Mode" ayarı "Simple" modundayken ve "Even Thickness" ayarı kapalı iken olan sonucun benzerini verir.
‎Even | Bu mod, "Mode" ayarı "Simple" modundayken ve "Even Thickness" ile "High Quality" ayarları açık iken olan sonucun benzerini verir.
‎Constraints | Bu mod her noktada en iyi kalınlık değerini bulmaya çalışan gelişmiş bir moddur.

* #### Boundary
Sadece "Mode" ayarı "Complex" modundayken vardır.

Mod | Açıklama
:---: | :---:
‎None | Herhangi bir değiklik yapılmaz.
Round | Köşelerde keskin geçişler oluyorsa bunu önlemek için belirli noktalarda kalınlığı kısar.
Flat | Düz bir geçiş olacak şekilde kalınlığı ayarlar.

* #### Thickness
Kalınlık.

* #### Offset
Kalınlığın ekleneceği yön, default olarak bu ayar -1'dir yani normal'ların tersine doğru yani içe doğru kalınlık ekler. Eğer bu ayarı 1 yaparsanız kalınlık normal'lar yönünde eklenir, yani dışa doğru. 0 yaparak iki yöne doğru da ortalı bir şekilde kalınlık ekleyebilirsiniz.

* #### Even Thickness
Sadece "Mode" ayarı "Simple" modundayken vardır. Eğer köşelerde uygulanan kalınlık azsa/fazlaysa bu ayarı açarak diğer kısımlar ile eşit şekilde kalınlık ekleyebilirsiniz. Daha fazla işlem gerektirdiği için yavaşlık ekleyebilir.

* #### Merge Threshold
Aralarındaki fark bu değerden daha az olan vertex'ler birleştirilir.

* #### Rim Fill
Bu ayar açıkken kalınlık ile mesh birbirine bağlıdır. Eğer bu ayarı kapatırsanız oluşturulan kalınlık mesh'e bağlı olmaz, bu da sanki yeni bir yüzey oluşturmuşsunuz gibi, yani kopya oluşturmuşsunuz gibi bir görünüm verir. Oluşturulan kalınlık ile mesh birbirinden ayrı kalır.

* #### Only Rim
"Mode" ayarı "Simple" modundayken bu ayar sadece kalınlık ekler. Yani mesh'in yüzeyine paralel olan kısımları sonuca eklemez. Sadece kalınlık ekler. Eklediği kalınlığın uçlarını veya iç taraflarını yapmaz. "Mode" ayarı "Complex" modundayken bu ayar kalınlık haricindeki her şeyi siler. Sadece yeni eklenen kalınlık kalır. Yani yüzeyler yeniden oluşturulmaz, sadece kalınlık olarak oluşturulan yeni kısım kalır.

* #### Vertex Group
Verdiğiniz Vertex Group içindeki vertex'ler kalınlaştırma işleminden etkilenir. Vertex'lerin sahip olduğu weight değeri kullanılarak kalınlık hesaplanır. 0 iken hiç kalınlık olmaz. 1 iken tam kalınlık olur.

* #### Factor
Vertex Group için factor değeri. Bu ayarın çalışma mantığı şudur, vertex group'un kalınlık değeri üzerinde ne kadar etkisi olacağını belirler. Mesela bu ayar 0 iken tamamen vertex group'un içindeki vertex'lerin weight değerleri kullanılır. Eğer bu ayarı 0.5 yaparsanız yarı yarıya vertex group kullanılır. Yani vertex group içerisinde weight değeri 0 olan vertex'ler olsa bile, bu vertex'ler sadece yarı yarıya vertex weight değerinden etkilendikleri için bu vertex'lere de "Thickness" input'una verdiğiniz değerin yarısı kadar kalınlık uygulanır. Yani kalınlık değerinin yarısı "Thickness" input'undan, yarısı vertex group'tan belirlenir. Eğer bu ayarı 1 yaparsanız vertex group'un hiç etkisi kalmaz. Yani vertex group içerisinde değeri 0 olan vertex'ler ile 1 olan vertex'ler arasında bir fark kalmaz.

* #### Flat Faces
Mesh'e paralel yani düz bir kalınlık oluşturmak için vertex'lerin weight değerlerini düzenler.


## Normals

* #### Flip
Normal'ların yönünü tersine çevirir.

* #### High Quality
Bu ayarı açarsanız kalınlık hesaplamaları daha doğru olur ama hesaplamalar artacağı için yavaşlık ekleyebilir.


## Materials

* #### Material Offset
Yeni oluşturulan kalınlıgın uç veya iç tarafları için (yani rim hariç, kalınlık hariç) materyal değeri. Bu değer şu anda kullanılan materyale ek olarak hesaplanır. Yani 1 yaparsanız bir sonraki, -1 yaparsanız bir önceki materyal kullanılır.

* #### Rim
Yeni oluşturulan kalınlıgın (rim) materyal değeri. Bu değer şu anda kullanılan materyale ek olarak hesaplanır. Yani 1 yaparsanız bir sonraki, -1 yaparsanız bir önceki materyal kullanılır.


## Edge Data

* #### Crease Inner
Sadece "Mode" ayarı "Simple" modundayken vardır. İç tarafa crease ekler.

* #### Crease Outer
Sadece "Mode" ayarı "Simple" modundayken vardır. Dış tarafa crease ekler.

* #### Rim
Sadece "Mode" ayarı "Simple" modundayken vardır. Kalınlık (rim) üzerine crease ekler.

<img src="../../Dosyalar/Modifiers_Solidify_Crease.png" width="400">

* #### Bevel Convex
Dış kenarlara eklenecek bevel weight değeri.


## Thickness Clamp

* #### Clamp
Bilmiyorum.

* #### Angle Clamp
Bilmiyorum.


## Output Vertex Groups

* #### Shell
Bilmiyorum.

* #### Rim
Bilmiyorum.



## [Subdivision Surface](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/subdivision_surface.html)
Subdivision Surface modifier'ı (veya Subsurf) mesh'inize ekstra geometri eklemenize yarar. Mesh'iniz ile low poly çalışıp (yani face sayısı az) işlerinizi bitirdikten sonra high poly (yani face sayısı fazla) yapabilmenize yarar.


* #### Mode

Mod | Açıklama
:---: | :---:
‎Catmull-Clark | Mesh'i subdivide ederken aynı zamanda yumuşak geçişler de uygular ve mesh'in şeklini de değiştirir.
‎Simple | Mesh'i sadece subdivide eder. Catmull-Clark'ın aksine şeklini değiştirmez.

* #### Adaptive Subdivision
Bu ayar sadece [Render Engine](../Render%20Properties#render-engine) "Cycles" iken ve [Feature Set](../Render%20Properties#feature-set) "Experimental" iken vardır. ["Adaptive Subdivision"](https://docs.blender.org/manual/en/3.6/render/cycles/object_settings/adaptive_subdiv.html) özelliğini açar.

* #### Dicing Scale
Sadece "Adaptive Subdivision" ayarı açıkken vardır. Dicing için scale değerini belirler. Bu değeri düşürürseniz daha fazla subdivision olur, arttırırsanız daha az. Ek ayarlara Render ayarlarında [Subdivision](../Render%20Properties#subdivision-1) kategorisinden ulaşabilirsiniz.

* #### Levels Viewport
Viewport için subdivide sayısı.

* #### Levels Render
Render için subdivide sayısı.

* #### Optimal Display
Viewport Shading "Wireframe" modundayken bu ayar mesh'in yeni oluşturulan kenarlarını göstermez. Sadece orijinal kenarları gösterir.


## Advanced

* #### Use Limit Surface
Bu ayar açıkken vertice'ler sadece sonsuz sayıda subdivision uygulanabilecek yüzeylere koyulur.

* #### Quality
"Use Limit Surface" ayarı açıkken bu ayar vertice'lerin koyulacakları yerleri belirler. Bu ayarı çok fazla arttırmanıza gerek yok, default değeri yeterli aslında.

* #### UV Smooth
UV üzerinde yapılacak değişiklikleri belirler.

Mod | Açıklama
:---: | :---:
‎None | UV üzerinde değişiklik yapılmaz.
Keep Corners | Bilmiyorum.
Keep Corners, Junctions | Bilmiyorum.
Keep Corners, Junctions, Concave | Bilmiyorum.
Keep Boundaries | Bilmiyorum.
All | Bilmiyorum.

* #### Boundary Smooth
UV üzerinde yapılacak yumuşatmaları belirler.

Mod | Açıklama
:---: | :---:
‎All | Köşeler de dahil olmak üzere her yerde geçişler yumuşatılır.
‎Keep Corners | Köşe kısımlar haricinde geriye kalan yerlerde geçişler yumuşatılır.

* #### Use Creases
Bilmiyorum.

* #### Use Custom Normals
Bilmiyorum.



## [Triangulate](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/triangulate.html)
Bu modifier mesh'inizin face'lerini üçgene çevirir, triangulate eder.


* #### Quad Method
Quad'lar (dörtgen) için kullanılacak triangulation (üçgene çevirme) metodu.

Mod | Açıklama
:---: | :---:
‎Beauty | Güzel bir şekilde bölmeye çalışır.
Fixed | 1. ve 3. vertice'leri kullanarak quad'ları üçgene çevirir.
Fixed Alternate | 2. ve 4. vertice'leri kullanarak quad'ları üçgene çevirir.
Shortest Diagonal | Quad'ları en kısa köşegeni bölerek üçgene çevirir.
Longest  Diagonal | Quad'ları en uzun köşegeni bölerek üçgene çevirir.

* #### N-gon Method
N-gon'lar (beşgen ve sonrası) için kullanılacak triangulation (üçgene çevirme) metodu.

Mod | Açıklama
:---: | :---:
‎Beauty | Güzel bir şekilde bölmeye çalışır.
Clip | Ear-clipping algoritması kullanır.

* #### Minimum Vertices
Triangulate edilecek face'lerin minimum vertice sayısı. Mesela bu ayarı 5 yaparsanız sadece beşgen ve sonrası çokgenler üçgene çevirilir.

* #### Keep Normals
Eğer [Custom Normals](https://docs.blender.org/manual/en/3.6/modeling/meshes/structure.html#modeling-meshes-normals-custom) kullanıyorsanız normal'ları bozmamaya çalışır.



## [Volume to Mesh](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/volume_to_mesh.html)
Bilmiyorum.



## [Weld](https://docs.blender.org/manual/en/3.6/modeling/modifiers/generate/weld.html)
Bu modifier birbirine yakın olan vertice'leri birleştirir.


* #### Mode

Mod | Açıklama
:---: | :---:
‎All | Objenin sahip olduğu bütün vertice'ler birleşebilir.
Connected | Objenin ayrık parçaları birleşemez, sadece birbirine connected yani bağlı olan kısımlar kendi içinde birleşebilir.

* #### Distance
Aralarındaki mesafe bu değerden az olan vertice'ler birleştirilir.

* #### Only Loose Edges
Sadece "Mode" ayarı "Connected" modundayken vardır. 

* #### Vertex Group
Sadece seçilen vertex group içerisindeki weight değeri 0'dan büyük olan vertice'ler birleştirilir. Ayrıca kenardaki invert işareti (yani <-> işareti) işlemi tersine çevirir, yani invert kapalıyken weight değeri 0'dan büyük olan vertice'ler birleştirilir ve weight değeri 0 olan vertice'ler birleştirilmez iken, invert açıldığında weight değeri 0'dan büyük olan vertice'ler birleştirilmez ve weight değeri 0 olan vertice'ler birleştirilir.










