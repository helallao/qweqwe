# Ek Bilgiler

<details>
<summary>Kullanılan Güzel Kaynaklar</summary>
<br>

* [The Blender 2.8 Encyclopedia](https://www.udemy.com/course/the-blender-encyclopedia/) - Udemy'deki sayısı bir elin parmaklarını geçmeyecek kadar az olan, gerçekten uğraşılmış kurslardan birisi. Bizim için önemli olan 8. bölüm "Constraints", constraints'lerin açıklamalarının olduğu bölüm, tabi isterseniz diğer kısımlara da bakabilirsiniz. [Buradan](https://btdig.com/search?q=The+Blender+2.8+Encyclopedia) torrent'ini bulabilirsiniz (vpn gerekebilir).

</details>



# [Motion Tracking](#motion-tracking-1)
* [Camera Solver](#camera-solver)
* [Follow Track](#follow-track)
* [Object Solver](#object-solver)

# [Transfrom](#transfrom-1)
* [Copy Location](#copy-location)
* [Copy Rotation](#copy-rotation)
* [Copy Scale](#copy-scale)
* [Copy Transforms](#copy-transforms)
* [Limit Distance](#limit-distance)
* [Limit Location](#limit-location)
* [Limit Rotation](#limit-rotation)
* [Limit Scale](#limit-scale)
* [Maintain Volume](#maintain-volume)
* [Transformation](#transformation)
* [Transform Cache](#transform-cache)

# [Tracking](#tracking-1)
* [Clamp To](#clamp-to)
* [Damped Track](#damped-track)
* [Locked Track](#locked-track)
* [Stretch To](#stretch-to)
* [Track To](#track-to)

# [Relationship](#relationship-1)
* [Action](#action)
* [Armature](#armature)
* [Child Of](#child-of)
* [Floor](#floor)
* [Follow Path](#follow-path)
* [Pivot](#pivot)
* [Shrinkwrap](#shrinkwrap)


<br>
<br>


# [Motion Tracking](https://docs.blender.org/manual/en/latest/animation/constraints/index.html#motion-tracking)
Bilmiyorum.


## [Camera Solver](https://docs.blender.org/manual/en/latest/animation/constraints/motion_tracking/camera_solver.html)
Bilmiyorum.


## [Follow Track](https://docs.blender.org/manual/en/latest/animation/constraints/motion_tracking/follow_track.html)
Bilmiyorum.


## [Object Solver](https://docs.blender.org/manual/en/latest/animation/constraints/motion_tracking/object_solver.html)
Bilmiyorum.


<br>
<br>


# [Transfrom](https://docs.blender.org/manual/en/latest/animation/constraints/index.html#transform)
Bu kategorideki constraint'ler çoğunlukla kopyalama (bilgi aktarma), limitleme ve diğer transform (yani location, rotation, scale) işlemleri ile ilgilidir.


## [Copy Location](https://docs.blender.org/manual/en/latest/animation/constraints/transform/copy_location.html)
Obje belirtilen hedef obje ile birlikte hareket eder, hedef objenin hareketleri kopyalanır.


* #### Target
Hedef obje.

* #### Axis
Hareketlerin kopyalanacağı eksen.

* #### Invert
Seçilen eksenler terse döndürülür, yani konum seçilen eksende terse alınır. Bu da aynalama gibi bir görünüm verir.

* #### Offset
Objenin orijinal konumu kullanılır, bu ayarı açtıktan sonra objeyi hareket de ettirebilirsiniz. Ayrıca bu ayarı açtıktan sonra artık eksenlerin orijin noktası dünyanın orijin noktası olmaz, hareket ettirdikçe eksenlerin orijin noktası da değişir.

* #### Target
Hedef obje için hareketlerin gerçekleştiği uzayı belirtir. Mesela bu ayarı "Local Space" yaparsanız hedef objenin hareketlerinin kendi lokal uzayına göre olduğunu söylemiş olursunuz. Yani mesela hedef obje kendi lokal X ekseninde ilerlerse, dünya üzerinde Y ekseninde ilerliyor olsa bile sonuç X ekseninde ilerleme olarak hesaplanır.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır. Ayrıca bu modda hedef objenin hareketini/konumunu etkileyen herhangi bir şey varsa constraint da bu hareketten etkilenir. Mesela hedef objenin bağlı olduğu parent hareket ederse constraint bu hareketi constraint'in uygulandığı objeye de yansıtır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır. Ayrıca bu modda hedef objenin hareketini/konumunu etkileyen herhangi bir şey varsa constraint bu hareketten etkilenmez. Mesela hedef objenin bağlı olduğu parent hareket ederse constraint bu hareketi constraint'in uygulandığı objeye yansıtmaz.

* #### Owner
Obje için hareketlerin gerçekleşeceği uzayı belirtir. Mesela bu ayarı "Local Space" yaparsanız objenin hareketlerinin kendi lokal uzayına göre olduğunu söylemiş olursunuz. Yani mesela diyelim ki obje X ekseninde ilerleyecek, eğer bu ayar "Local Space" ise ve objenin lokal X ekseni dünya üzerinde Y ekseni ise, o zaman obje X ekseninde ilerlerken aslında dünya üzerinde Y ekseninde ilerler. Yani demek istediğim şey eksenler birbirlerinden farklı olabilir, bu ayarı kullanarak seçtiğiniz uzayın eksenleri ne ise o kullanılır.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır. Ayrıca bu modda objenin hareketini/konumunu etkileyen herhangi bir şey varsa constraint da bu hareketten etkilenir. Mesela objenin bağlı olduğu parent hareket ederse hareket işlemi constraint'in üzerine eklenir, yani obje hem parent'dan hem de constraint'den etkilenir.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır. Ayrıca bu modda objenin hareketini/konumunu etkileyen herhangi bir şey varsa constraint bu hareketten etkilenmez. Mesela objenin bağlı olduğu parent hareket ederse hareket işlemi objeyi etkilemez, objeyi sadece constraint etkiler.




## [Copy Rotation](https://docs.blender.org/manual/en/latest/animation/constraints/transform/copy_rotation.html)
Objeye belirtilen hedef obje ile birlikte rotasyon uygulanır, yani hedef objenin rotasyonu kopyalanır.


* #### Target
Hedef obje.

* #### Order
XYZ eksenleri için rotasyon sıralamasını belirtir.

* #### Axis
Rotasyonun kopyalanacağı eksen.

* #### Invert
Seçilen eksenler için rotasyon terse döndürülür, yani rotasyon seçilen eksende terse alınır. Bu da aynalama gibi bir görünüm verir.

* #### Mix
Rotasyonun nasıl uygulanacağını belirtir.

Mod | Açıklama
:---: | :---:
‎Replace | Default mod. Hedef objenin rotasyonunu constraint uygulanan objeye kopyalar.
Add | Hedef objenin rotasyonunu constraint uygulanan objenin rotasyonunun üzerine ekler.
Before Original | Rotasyon objenin orijinal rotasyonundan önce eklenir. Bunu şöyle düşünün, mesela objemizin bir parent'ı olsun, parent'a rotasyon uygularsanız objeye de rotasyon uygulanır, constraint'in rotasyonu ise en son uygulanır (normalde), ama bu modu kullanırsanız rotasyon sanki parent'a uygulanan rotasyonmuş gibi olur.
After Original | Rotasyon objenin orijinal rotasyonundan sonra eklenir. Bunu şöyle düşünün, mesela objemiz başka bir objenin parent'ı olsun, parent'a rotasyon uygularsanız objeye de rotasyon uygulanır, normalde constraint'in rotasyonu parent'a uygulanır sonra parent'a bağlı olan diğer obje parent'dan etkilenir, ama bu modu kullanırsanız rotasyon sanki parent'a bağlı olan objeye uygulanan rotasyonmuş gibi olur.
Offset (Legacy) | Eski offset ayarının mod hali ama bazı sorunları olduğu için artık kullanılmıyor.

* #### Target
Hedef obje için rotasyonun gerçekleştiği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Owner
Obje için rotasyonun gerçekleşeceği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Influence
Constraint'in etki derecesi. Bunu rotasyonu kopyalama derecesi olarak da düşünebilirsiniz. Mesela bu ayarı 0.5 yaparsanız, hedef obje 90 derece döndüğünde obje 45 derece döner, yani yarıya indirmiş olursunuz.



## [Copy Scale](https://docs.blender.org/manual/en/latest/animation/constraints/transform/copy_scale.html)
Objeye belirtilen hedef obje ile birlikte scale uygulanır, yani hedef objenin scale değerleri kopyalanır.


* #### Target
Hedef obje.

* #### Axis
Scale'in kopyalanacağı eksen.

* #### Power
Scale değeri için çarpan görevi görür. Mesela bu değer 2 iken hedef obje 2 kat scale edildiğinde constraint'in uygulandığı obje 4 kat scale edilir, yani 2 kat daha fazla scale uygulanır.

* #### Make Uniform
Scale değerini objeye tek bir (veya 2) eksende değil de bütün eksenlerde uygular. Mesela diyelim ki "Axis" ayarını sadece X olarak ayarladınız. Bu ayar kapalı iken hedef objenin X ekseninde scale değeri arttıkça constraint'in uygulandığı objenin de X ekseninde scale değeri artar, eğer bu ayarı açarsanız hedef objenin X ekseninde scale değeri arttıkça constraint'in uygulandığı objenin sadece X değil bütün eksenlerde scale değeri artar. Yani hedef objenin X ekseninde scale değerindeki artış constraint'in uygulandığı objenin bütün eksenlerine paylaştırılır.

* #### Offset
Bu ayar açık iken objenin scale değerini değiştirebilirsiniz.

* #### Additive
Sadece "Offset" ayarı açık iken vardır. Bu ayar kapalı iken, "Offset" ayarını açıp offset uyguladıktan sonra, hedef obje ile constraint'in uygulandığı obje arasındaki scale değeri çarpma şeklinde ayarlanır. Yani diyelim ki "Offset" ayarını açıp objenin scale değerini 3 katına çıkardınız. Bu durumda hedef objenin scale değeri değiştirildiğinde constraint'in uygulandığı objenin scale değeri de 3 kat daha fazla değiştirilir. Yani constraint hedef objedeki scale değerini constraint'in uygulandığı objeye aktarırken objelerin scale değerlerine göre yüzdelik olarak çalışır (yani oranları korur). Eğer bu ayarı açarsanız artık değerler çarparak değil de toplanarak hesaplanır. Yani mesela diyelim ki "Offset" ayarını açıp objenin scale değerini 3 katına çıkardınız, eğer bu ayar kapalı olsaydı bu durumda hedef objenin scale değerini 2 katına çıkardığınızda objenin de scale değeri 2 katına çıkacağından 6 olurdu, ama bu ayarı açarsanız çarpmak yerine toplama olarak hesaplanır ve objenin scale değeri 6 değil 3 + 1'den 4 olur.

* #### Target
Hedef obje için scale işleminin gerçekleştiği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Owner
Obje için scale işleminin gerçekleşeceği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Influence
Constraint'in etki derecesi. Bunu scale değerini kopyalama derecesi olarak da düşünebilirsiniz. Mesela bu ayarı 0.5 yaparsanız, hedef objeye 4 kat scale uygulandığında objeye 2 kat scale uygulanır, yani yarıya indirmiş olursunuz.



## [Copy Transforms](https://docs.blender.org/manual/en/latest/animation/constraints/transform/copy_transforms.html)
Objeye belirtilen hedef obje ile birlikte transform (location, rotation, scale) uygulanır, yani hedef objenin transform değerleri kopyalanır.


* #### Target
Hedef obje.

* #### Remove Target Shear
Bu ayar hakkında hiçbir yerde düzgün açıklama bulamadım. Kendim denesem bile bir etkisi olduğunu görmedim.

* #### Mix
Hedef objenin transform değerlerinin objeye nasıl uygulanacağını belirtir.

Mod | Açıklama
:---: | :---:
‎Replace | Default mod. Hedef objenin transform değerlerini constraint uygulanan objeye kopyalar.
Before Original (Full) | Bilmiyorum.
Before Original (Aligned) | Bilmiyorum.
Before Original (Split Channels) | Bilmiyorum.
After Original (Full) | Bilmiyorum.
After Original (Aligned) | Bilmiyorum.
After Original (Split Channels) | Bilmiyorum.

* #### Target
Hedef obje için transform işlemlerinin gerçekleştiği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Owner
Obje için transform işlemlerinin gerçekleşeceği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Influence
Constraint'in etki derecesi. Bunu transform (location, rotation, scale) değerini kopyalama derecesi olarak da düşünebilirsiniz. Mesela bu ayarı 0.5 yaparsanız, hedef objeye uygulanan transform işlemlerinin yarısı objeye uygulanır, yani yarıya indirmiş olursunuz.



## [Limit Distance](https://docs.blender.org/manual/en/latest/animation/constraints/transform/limit_distance.html)
Objeyi hedef objeden belirtilen mesafe değeri kadar yakında veya uzakta tutar, isterseniz tam olarak bu mesafeye de sabitleyebilirsiniz.


* #### Target
Hedef obje.

* #### Distance
Mesafe değeri.

* #### Clamp Region
"Distance" ayarı bir nevi yarıçap değeri görevi görür. Bu ayar da kullanılacak modu belirtir, objeyi yarıçap'ın içinde/dışında veya üzerinde tutabilirsiniz.

Mod | Açıklama
:---: | :---:
‎Inside | Obje yarıçap'ın içinde tutulur, yani obje belirtilen mesafe değerinden daha fazla uzağa gidemez.
‎Outside | Obje yarıçap'ın dışında tutulur, yani obje belirtilen mesafe değerinden daha fazla yakına gidemez.
‎On Surface | Obje yarıçap'ın üzerinde tutulur, yani obje belirtilen mesafe değerinden daha fazla yakına veya uzağa gidemez, tam olarak aynı mesafede durur.

* #### Affect Transform
Bu ayar kapalı iken constraint objenin konum değerini gerçekten değiştirmez. Yani aslında objeyi hareket ettirirseniz obje gidemediği yerlere de gidebilir ama constraint objeyi orijinal konumunda göstermez, yani constraint objeyi sanki oradaymış gibi gösterir ama aslında konum değerleri farklıdır (sağdaki panelden görebilirsiniz). Eğer bu ayarı açarsanız constraint objenin konum değerlerini de değiştirir.

* #### Target
Hedef obje için konum işlemlerinin gerçekleştiği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Owner
Obje için konum işlemlerinin gerçekleşeceği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Influence
Constraint'in etki derecesi.



## [Limit Location](https://docs.blender.org/manual/en/latest/animation/constraints/transform/limit_location.html)
Objenin konumunu belirttiğiniz minimum ve maximum değerleri arasında tutar.


* #### Minimum X/Y/Z
Objenin konumu bu eksenlerde belirttiğiniz değerden daha az olamaz. Eğer tik işaretine basıp ekseni açarsanız verdiğiniz değer kullanılır, açmazsanız objenin konumu için minimum değer belirlememişsiniz demektir (yani istediğiniz değeri verebilirsiniz).

* #### Maximum X/Y/Z
Objenin konumu bu eksenlerde belirttiğiniz değerden daha fazla olamaz. Eğer tik işaretine basıp ekseni açarsanız verdiğiniz değer kullanılır, açmazsanız objenin konumu için maximum değer belirlememişsiniz demektir (yani istediğiniz değeri verebilirsiniz).

* #### Affect Transform
Bu ayar kapalı iken constraint objenin konum değerini gerçekten değiştirmez. Yani aslında objeyi hareket ettirirseniz obje gidemediği yerlere de gidebilir ama constraint objeyi orijinal konumunda göstermez, yani constraint objeyi sanki oradaymış gibi gösterir ama aslında konum değerleri farklıdır (sağdaki panelden görebilirsiniz). Eğer bu ayarı açarsanız constraint objenin konum değerlerini de değiştirir.

* #### Owner
Obje için konum işlemlerinin gerçekleşeceği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Influence
Constraint'in etki derecesi.



## [Limit Rotation](https://docs.blender.org/manual/en/latest/animation/constraints/transform/limit_rotation.html)
Objenin rotasyonunu belirttiğiniz minimum ve maximum değerleri arasında tutar.


* #### Limit X/Y/Z
Objenin rotasyonu bu eksenlerde belirttiğiniz değerlerden daha az ve fazla olamaz. Eğer tik işaretine basıp ekseni açarsanız verdiğiniz değer kullanılır, açmazsanız objenin rotasyonu için değer belirlememişsiniz demektir (yani istediğiniz değeri verebilirsiniz).

* #### Order
XYZ eksenleri için rotasyon sıralamasını belirtir.

* #### Affect Transform
Bu ayar kapalı iken constraint objenin rotasyon değerini gerçekten değiştirmez. Yani aslında objeyi döndürürseniz objenin rotasyon değeri limiti geçebilir ama constraint objeyi orijinal rotasyonunda göstermez, yani constraint objeyi sanki limit rotasyonundaymış gibi gösterir ama aslında rotasyon değerleri farklıdır (sağdaki panelden görebilirsiniz). Eğer bu ayarı açarsanız constraint objenin rotasyon değerlerini de değiştirir.

* #### Owner
Obje için rotasyon işlemlerinin gerçekleşeceği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Influence
Constraint'in etki derecesi.



## [Limit Scale](https://docs.blender.org/manual/en/latest/animation/constraints/transform/limit_scale.html)
Objenin scale değerini belirttiğiniz minimum ve maximum değerleri arasında tutar.


* #### Minimum X/Y/Z
Objenin scale değeri bu eksenlerde belirttiğiniz değerden daha az olamaz. Eğer tik işaretine basıp ekseni açarsanız verdiğiniz değer kullanılır, açmazsanız objenin scale değeri için minimum değer belirlememişsiniz demektir (yani istediğiniz değeri verebilirsiniz).

* #### Maximum X/Y/Z
Objenin scale değeri bu eksenlerde belirttiğiniz değerden daha fazla olamaz. Eğer tik işaretine basıp ekseni açarsanız verdiğiniz değer kullanılır, açmazsanız objenin scale değeri için maximum değer belirlememişsiniz demektir (yani istediğiniz değeri verebilirsiniz).

* #### Affect Transform
Bu ayar kapalı iken constraint objenin scale değerini gerçekten değiştirmez. Yani aslında objeyi scale ederseniz objenin scale değeri limiti geçebilir ama constraint objeyi orijinal scale değerinde göstermez, yani constraint objeyi sanki limit scale değerindeymiş gibi gösterir ama aslında scale değerleri farklıdır (sağdaki panelden görebilirsiniz). Eğer bu ayarı açarsanız constraint objenin scale değerlerini de değiştirir.

* #### Owner
Obje için scale işlemlerinin gerçekleşeceği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Influence
Constraint'in etki derecesi.



## [Maintain Volume](https://docs.blender.org/manual/en/latest/animation/constraints/transform/maintain_volume.html)
Objenin kapladığı volume'ü (alanı) bozmadan scale değerlerini düzenler.


* #### Mode

Mod | Açıklama
:---: | :---:
‎Strict | "Free Axis" ayarında seçilen eksende yapılan scale işlemleri bozulmadan, diğer eksenlerde yapılan scale işlemlerini düzenler, böylelikle volume korunur (yani bozulmadan tutulur). Yani bu mod her türlü volume'ü korur ama "Free Axis" ayarında seçilen eksende yapılan scale işlemleri de bozulmadan tutulur. Diyelim ki "Free Axis" olarak Y eksenini seçtiniz, bu durumda eğer Z ekseninde scale değerini değiştirirseniz, volume X ekseninin scale değeri değiştirilerek korunur.
Uniform | Objeye bir eksende değil de bütün eksenlerde yani direktmen scale uygulandığında, objenin "Free Axis" ayarında seçilen ekseninde scale değeri korunur (yani bozulmadan tutulur). Diğer eksenlerde yapılan scale işlemleri için volume korunmaz (yani normal scale gibidirler).
Single Axis | Sadece "Free Axis" ayarında seçilen eksende yapılan scale işlemleri için volume korunur (yani bozulmadan tutulur). Diğer eksenlerde yapılan scale işlemleri için volume korunmaz (yani normal scale gibidirler).

* #### Free Axis
Objenin free yani serbest bir şekilde scale edilebilecek ekseni. Bu eksen scale edilirken diğer eksenler "Volume" ayarına verilen değere eşit olacak şekilde objenin alanını düzenler.

* #### Volume
Objenin kapladığı alan değeri, objenin scale değerleri objenin kapladığı alan bu değere eşit olacak şekilde düzenlenir.

* #### Owner
Obje için scale işlemlerinin gerçekleşeceği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Influence
Constraint'in etki derecesi.



## [Transformation](https://docs.blender.org/manual/en/latest/animation/constraints/transform/transformation.html)
Bu constraint hedef objenin transfrom değerlerinden birini, yani location/rotation/scale değerlerinden birini, constraint'in uygulandığı objenin transfrom değerlerinden birine, yani location/rotation/scale değerlerinden birinine çevirmemizi sağlar. Mesela hedef obje X ekseninde konumunu değiştirince constraint'in uygulandığı objenin rotasyon değerini değiştirmek için bu constraint'i kullanabilirsiniz.


* #### Target
Hedef obje.

* #### Extrapolate
Bu ayar açık iken "Map From" ve "Map To" değerleri için sınırlamalar kalkar. Değerler limitleri geçse bile aralarındaki oran bozulmadan işlemler devam eder. Yani mesela bu ayar kapalı iken "Map From" ile hedef objenin X ekseninde 0 ile 5 arasında konum değiştirmesini "Map To" ile constraint'in uygulandığı objenin scale değerini 0 ile 3 arasında değiştirmek için kullandığınızda, hedef objenin konumu 5'i geçse bile constraint'in uygulandığı objenin scale değeri 3'ü geçmez. Eğer bu ayarı açarsanız bu limitler kaldırılır ve oran bozulmadan işlemler olabilecek bütün değerler için hesaplanıp kullanılır. Mesela hedef objenin konumu 10 olursa constraint'in uygulandığı objenin scale değeri 6 olur (yani 2 katı olur, aralarındaki oran korunur).

* #### Target
Hedef obje için transform işlemlerinin gerçekleştiği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Owner
Obje için transform işlemlerinin gerçekleşeceği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Influence
Constraint'in etki derecesi.

* #### Map From
Hedef objeden alınıp kullanılacak değer. İlk baş hangi transform değerini kullanacağınızı seçmelisiniz (yani location/rotation/scale). Ardından kullanacağınız eksen için (birden fazla da kullanabilirsiniz) minimum ve maksimum değerler belirlemelisiniz. Ayrıca "Rotation" için farklı rotasyon modları seçebilirsiniz.

* #### Map To
İlk baş hangi transform değerini kullanacağınızı seçmelisiniz (yani location/rotation/scale). Ardından kullanacağınız eksen için (birden fazla da kullanabilirsiniz) minimum ve maksimum değerler belirlemelisiniz. Her eksen için "Source Axis" diye input vardır, bu input üzerinden hedef objeden gelen transform bilgisinin (yani location/rotation/scale) hangi ekseninin kullanılacağını seçebilirsiniz. Ayrıca "Location" için farklı "Mix" modları seçebilirsiniz, "Replace" direktmen hedef objeden gelen bilginin "Map From" da belirtilen minimum ve maximum oranına göre "Map To" da belirtilen minimum ve maximum aralığında hesaplanmasıdır, "Add" ise aynı işlemi yapar ama yeni değeri şu anki değerin üzerine ekler. "Rotation" için farklı rotasyon sıralamaları seçebilirsiniz, ek olarak "Before Original" ve "After Original" modlarını da kullanabilirsiniz ([Copy Rotation](#copy-rotation) constraint'inin "Mix" ayarına bakın). "Scale" için de farklı "Mix" modları seçebilirsiniz, "Replace" direktmen hedef objeden gelen bilginin "Map From" da belirtilen minimum ve maximum oranına göre "Map To" da belirtilen minimum ve maximum aralığında hesaplanmasıdır, "Multiply" ise aynı işlemi yapar ama yeni değer ile şu anki değerin çarpımını kullanır (anlamadıysanız [Copy Scale](#copy-scale) constraint'inin "Additive" ayarına bakın, orda ekleme ile çarpma arasındaki fark anlatılıyor).



## [Transform Cache](https://docs.blender.org/manual/en/latest/animation/constraints/transform/transform_cache.html)
Bilmiyorum.


<br>
<br>


# [Tracking](https://docs.blender.org/manual/en/latest/animation/constraints/index.html#tracking)
Bu kategoride objenin rotasyonunu hedef objeye doğru bakacak şekilde ayarlayabildiğiniz constraint'ler vardır.


## [Clamp To](https://docs.blender.org/manual/en/latest/animation/constraints/tracking/clamp_to.html)
Objeyi hedef curve boyunca hareket ettirir, objenin konumu değiştikçe curve üzerindeki konumu da değişir (ileri/geri).


* #### Target
Hedef curve.

* #### Main Axis
Objenin curve üzerindeki hareketi için kullanılacak konum (eksen) değeri.

Mod | Açıklama
:---: | :---:
‎Auto | Objenin dünya üzerindeki konumuna göre hesaplamalar yapılıp curve üzerindeki konumu bulunur.
X | Objenin dünya üzerindeki konumunun X ekseni kullanılır. Objenin X ekseninde konum değeri arttıkça curve üzerinde de ilerler.
Y | Objenin dünya üzerindeki konumunun Y ekseni kullanılır. Objenin Y ekseninde konum değeri arttıkça curve üzerinde de ilerler.
Z | Objenin dünya üzerindeki konumunun Z ekseni kullanılır. Objenin Z ekseninde konum değeri arttıkça curve üzerinde de ilerler.

* #### Cyclic
Bu ayar açıkken obje curve üzerinde sona ulaşırsa tekrar başa döner yani baştan başlar.

* #### Influence
Constraint'in etki derecesi.



## [Damped Track](https://docs.blender.org/manual/en/latest/animation/constraints/tracking/damped_track.html)
[Track To](#track-to) constraint'i ile aynı sayılır, tek farkı size ikincil ekseni (Up) seçebilme hakkı sunmaz. Objenin rotasyonunu hedef objeye bakacak şekilde düzenler. Bu constraint'i anlamanız için güzel bir şekilde test etmeniz gerekir, size en anlaşılır test yöntemini vereyim. Test etmek için normal objeler kullanırsanız yönleri anlama konusunda zorluk yaşayabilirsiniz, bu yüzden test için "Arrows" objesini kullanmanızı tavsiye ederim. Obje ekleme bölümünde (Shift + A) "Empty" kategorisindeki "Arrows" objesini kullanarak constraint'i test edebilirsiniz. Aşağıdaki açıklamalar ve biraz uğraş ile constraint'in nasıl çalıştığını anlayabilirsiniz.


* #### Target
Hedef obje.

* #### Track Axis
Objenin hangi ekseninin hedef objeye doğru bakacağını belirtir. Yani objenin kendi lokal yönlerinin hangisinin hedef objeye doğru bakacağını ayarlar. Eksi değere sahip yönler, o yönü hedef objenin tam tersi yöne bakmasını sağlar.

* #### Influence
Constraint'in etki derecesi.



## [Locked Track](https://docs.blender.org/manual/en/latest/animation/constraints/tracking/locked_track.html)
Objenin rotasyonunu tek bir eksende hedef objeye bakacak şekilde düzenler.


* #### Target
Hedef obje.

* #### Track Axis
Objenin hangi eksende hedef objeye doğru bakacağını belirtir. Eksi değere sahip yönler, o yönü hedef objenin tam tersi yöne bakmasını sağlar. "Locked Axis" ayarında belirtilen eksen ile aynı ekseni seçerseniz constraint düzgün çalışmaz.

* #### Locked Axis
Objenin "Track Axis" ayarında seçtiğiniz ekseni hedef objeye doğru bakacak şekilde düzenlenirken, bu düzenlemeden etkilenmeyecek olan eksen. Yani bu ayarda seçtiğiniz eksen sabit tutulur, değiştirilmez. "Track Axis" ayarında belirtilen eksen ile aynı ekseni seçerseniz constraint düzgün çalışmaz.

* #### Influence
Constraint'in etki derecesi.



## [Stretch To](https://docs.blender.org/manual/en/latest/animation/constraints/tracking/stretch_to.html)
Bilmiyorum.



## [Track To](https://docs.blender.org/manual/en/latest/animation/constraints/tracking/track_to.html)
[Damped Track](#damped-track) constraint'inin daha gelişmişidir denilebilir, size ikincil ekseni (Up) seçebilme hakkı sunar. Objenin rotasyonunu hedef objeye bakacak şekilde düzenler. Bu constraint'i anlamanız için güzel bir şekilde test etmeniz gerekir, size en anlaşılır test yöntemini vereyim. Test etmek için normal objeler kullanırsanız yönleri anlama konusunda zorluk yaşayabilirsiniz, bu yüzden test için "Arrows" objesini kullanmanızı tavsiye ederim. Obje ekleme bölümünde (Shift + A) "Empty" kategorisindeki "Arrows" objesini kullanarak constraint'i test edebilirsiniz. Aşağıdaki açıklamalar ve biraz uğraş ile constraint'in nasıl çalıştığını anlayabilirsiniz.


* #### Target
Hedef obje.

* #### Track Axis
Objenin hangi ekseninin hedef objeye doğru bakacağını belirtir. Yani objenin kendi lokal yönlerinin hangisinin hedef objeye doğru bakacağını ayarlar. Eksi değere sahip yönler, o yönü hedef objenin tam tersi yöne bakmasını sağlar. "Up" ayarında belirtilen eksen ile aynı ekseni seçerseniz constraint düzgün çalışmaz.

* #### Up
Objenin "Track Axis" ayarında seçtiğiniz yönü hedef objeye doğru bakar, ama hesaplamaların yapılabilmesi için bir eksene daha ihtiyacımız var ([Cross Product](https://en.wikipedia.org/wiki/Cross_product) hesaplaması için 2 eksen gerekir, yani toplamda 3 ekseni oluşturmak için 2 tane eksen belirlemelisiniz). İşte bu eksen de "Up", yani objenin "Track Axis" ayarında seçtiğiniz yönü hedef objeye doğru bakarken, obje hareket ettikçe dönüş (rotasyon) yapabilmesi için kullanılacak yukarı yönü (yani up). Eğer constraint'in açıklamasında yazdığım test yöntemini uyguladıysanız, "Arrows" objesinin bu ayarda seçtiğiniz ekseninin yukarıya doğru baktığını görebilirsiniz. "Track Axis" ayarında belirtilen eksen ile aynı ekseni seçerseniz constraint düzgün çalışmaz.

* #### Target Z
Normalde rotasyon gerçekleşirken objenin "Up" yönü dünyanın Z ekseni ile eşitlenir (hesaplamalar Z eksenine göre ayarlanır). Eğer bu ayarı açarsanız objenin "Up" yönü dünyanın Z eksenine değil hedef objenin lokal Z eksenine eşitlenir.

* #### Target
Hedef obje için transform işlemlerinin gerçekleştiği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Owner
Obje için transform işlemlerinin gerçekleşeceği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Influence
Constraint'in etki derecesi.


<br>
<br>


# [Relationship](https://docs.blender.org/manual/en/latest/animation/constraints/index.html#relationship)
Bilmiyorum.


## [Action](https://docs.blender.org/manual/en/latest/animation/constraints/relationship/action.html)
Bilmiyorum.



## [Armature](https://docs.blender.org/manual/en/latest/animation/constraints/relationship/armature.html)
Bilmiyorum.



## [Child Of](https://docs.blender.org/manual/en/latest/animation/constraints/relationship/child_of.html)
Bilmiyorum.



## [Floor](https://docs.blender.org/manual/en/latest/animation/constraints/relationship/floor.html)
Bilmiyorum.



## [Follow Path](https://docs.blender.org/manual/en/latest/animation/constraints/relationship/follow_path.html)
Bilmiyorum.



## [Pivot](https://docs.blender.org/manual/en/latest/animation/constraints/relationship/pivot.html)
Bilmiyorum.



## [Shrinkwrap](https://docs.blender.org/manual/en/latest/animation/constraints/relationship/shrinkwrap.html)
Bilmiyorum.



