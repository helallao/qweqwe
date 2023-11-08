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
Bilmiyorum.


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
‎World Space | Dünya uzayı (eksenleri) kullanılır. Ayrıca bu modda hedef objenin hareketini/konumunu etkileyen herhangi bir şey varsa modifier da bu hareketten etkilenir. Mesela hedef objenin bağlı olduğu parent hareket ederse modifier bu hareketi modifier'ın uygulandığı objeye de yansıtır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır. Ayrıca bu modda hedef objenin hareketini/konumunu etkileyen herhangi bir şey varsa modifier bu hareketten etkilenmez. Mesela hedef objenin bağlı olduğu parent hareket ederse modifier bu hareketi modifier'ın uygulandığı objeye yansıtmaz.

* #### Owner
Obje için hareketlerin gerçekleşeceği uzayı belirtir. Mesela bu ayarı "Local Space" yaparsanız objenin hareketlerinin kendi lokal uzayına göre olduğunu söylemiş olursunuz. Yani mesela diyelim ki obje X ekseninde ilerleyecek, eğer bu ayar "Local Space" ise ve objenin lokal X ekseni dünya üzerinde Y ekseni ise, o zaman obje X ekseninde ilerlerken aslında dünya üzerinde Y ekseninde ilerler. Yani demek istediğim şey eksenler birbirlerinden farklı olabilir, bu ayarı kullanarak seçtiğiniz uzayın eksenleri ne ise o kullanılır.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır. Ayrıca bu modda objenin hareketini/konumunu etkileyen herhangi bir şey varsa modifier da bu hareketten etkilenir. Mesela objenin bağlı olduğu parent hareket ederse hareket işlemi modifier'ın üzerine eklenir, yani obje hem parent'dan hem de modifier'dan etkilenir.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır. Ayrıca bu modda objenin hareketini/konumunu etkileyen herhangi bir şey varsa modifier bu hareketten etkilenmez. Mesela objenin bağlı olduğu parent hareket ederse hareket işlemi objeyi etkilemez, objeyi sadece modifier etkiler.




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
‎Replace | Default mod. Hedef objenin rotasyonunu modifier uygulanan objeye kopyalar.
Add | Hedef objenin rotasyonunu modifier uygulanan objenin rotasyonunun üzerine ekler.
Before Original | Rotasyon objenin orijinal rotasyonundan önce eklenir. Bunu şöyle düşünün, mesela objemizin bir parent'ı olsun, parent'a rotasyon uygularsanız objeye de rotasyon uygulanır, modifier'ın rotasyonu ise en son uygulanır (normalde), ama bu modu kullanırsanız rotasyon sanki parent'a uygulanan rotasyonmuş gibi olur.
After Original | Rotasyon objenin orijinal rotasyonundan sonra eklenir. Bunu şöyle düşünün, mesela objemiz başka bir objenin parent'ı olsun, parent'a rotasyon uygularsanız objeye de rotasyon uygulanır, normalde modifier'ın rotasyonu parent'a uygulanır sonra parent'a bağlı olan diğer obje parent'dan etkilenir, ama bu modu kullanırsanız rotasyon sanki parent'a bağlı olan objeye uygulanan rotasyonmuş gibi olur.
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
Modifier'ın etki derecesi. Bunu rotasyonu kopyalama derecesi olarak da düşünebilirsiniz. Mesela bu ayarı 0.5 yaparsanız, hedef obje 90 derece döndüğünde obje 45 derece döner, yani yarıya indirmiş olursunuz.



## [Copy Scale](https://docs.blender.org/manual/en/latest/animation/constraints/transform/copy_scale.html)
Objeye belirtilen hedef obje ile birlikte scale uygulanır, yani hedef objenin scale değerleri kopyalanır.


* #### Target
Hedef obje.

* #### Axis
Scale'in kopyalanacağı eksen.

* #### Power
Scale değeri için çarpan görevi görür. Mesela bu değer 2 iken hedef obje 2 kat scale edildiğinde modifier'ın uygulandığı obje 4 kat scale edilir, yani 2 kat daha fazla scale uygulanır.

* #### Make Uniform
Scale değerini objeye tek bir (veya 2) eksende değil de bütün eksenlerde uygular. Mesela diyelim ki "Axis" ayarını sadece X olarak ayarladınız. Bu ayar kapalı iken hedef objenin X ekseninde scale değeri arttıkça modifier'ın uygulandığı objenin de X ekseninde scale değeri artar, eğer bu ayarı açarsanız hedef objenin X ekseninde scale değeri arttıkça modifier'ın uygulandığı objenin sadece X değil bütün eksenlerde scale değeri artar. Yani hedef objenin X ekseninde scale değerindeki artış modifier'ın uygulandığı objenin bütün eksenlerine paylaştırılır.

* #### Offset
Bu ayar açık iken objenin scale değerini değiştirebilirsiniz.

* #### Additive
Sadece "Offset" ayarı açık iken vardır. Bu ayar kapalı iken, "Offset" ayarını açıp offset uyguladıktan sonra, hedef obje ile modifier'ın uygulandığı obje arasındaki scale değeri çarpma şeklinde ayarlanır. Yani diyelim ki "Offset" ayarını açıp objenin scale değerini 3 katına çıkardınız. Bu durumda hedef objenin scale değeri değiştirildiğinde modifier'ın uygulandığı objenin scale değeri de 3 kat daha fazla değiştirilir. Yani modifier hedef objedeki scale değerini modifier'ın uygulandığı objeye aktarırken objelerin scale değerlerine göre yüzdelik olarak çalışır (yani oranları korur). Eğer bu ayarı açarsanız artık değerler çarparak değil de toplanarak hesaplanır. Yani mesela diyelim ki "Offset" ayarını açıp objenin scale değerini 3 katına çıkardınız, eğer bu ayar kapalı olsaydı bu durumda hedef objenin scale değerini 2 katına çıkardığınızda objenin de scale değeri 2 katına çıkacağından 6 olurdu, ama bu ayarı açarsanız çarpmak yerine toplama olarak hesaplanır ve objenin scale değeri 6 değil 3 + 1'den 4 olur.

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
Modifier'ın etki derecesi. Bunu scale değerini kopyalama derecesi olarak da düşünebilirsiniz. Mesela bu ayarı 0.5 yaparsanız, hedef objeye 4 kat scale uygulandığında objeye 2 kat scale uygulanır, yani yarıya indirmiş olursunuz.



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
‎Replace | Default mod. Hedef objenin transform değerlerini modifier uygulanan objeye kopyalar.
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
Modifier'ın etki derecesi. Bunu transform (location, rotation, scale) değerini kopyalama derecesi olarak da düşünebilirsiniz. Mesela bu ayarı 0.5 yaparsanız, hedef objeye uygulanan transform işlemlerinin yarısı objeye uygulanır, yani yarıya indirmiş olursunuz.



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
Bu ayar kapalı iken modifier objenin konum değerini gerçekten değiştirmez. Yani aslında objeyi hareket ettirirseniz obje gidemediği yerlere de gidebilir ama modifier objeyi orijinal konumunda göstermez, yani modifier objeyi sanki oradaymış gibi gösterir ama aslında konum değerleri farklıdır (sağdaki panelden görebilirsiniz). Eğer bu ayarı açarsanız modifier objenin konum değerlerini de değiştirir.

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
Modifier'ın etki derecesi.



## [Limit Location](https://docs.blender.org/manual/en/latest/animation/constraints/transform/limit_location.html)
Objenin konumunu belirttiğiniz minimum ve maximum değerleri arasında tutar.


* #### Minimum X/Y/Z
Objenin konumu bu eksenlerde belirttiğiniz değerden daha az olamaz. Eğer tik işaretine basıp ekseni açarsanız verdiğiniz değer kullanılır, açmazsanız objenin konumu için minimum değer belirlememişsiniz demektir (yani istediğiniz değeri verebilirsiniz).

* #### Maximum X/Y/Z
Objenin konumu bu eksenlerde belirttiğiniz değerden daha fazla olamaz. Eğer tik işaretine basıp ekseni açarsanız verdiğiniz değer kullanılır, açmazsanız objenin konumu için maximum değer belirlememişsiniz demektir (yani istediğiniz değeri verebilirsiniz).

* #### Affect Transform
Bu ayar kapalı iken modifier objenin konum değerini gerçekten değiştirmez. Yani aslında objeyi hareket ettirirseniz obje gidemediği yerlere de gidebilir ama modifier objeyi orijinal konumunda göstermez, yani modifier objeyi sanki oradaymış gibi gösterir ama aslında konum değerleri farklıdır (sağdaki panelden görebilirsiniz). Eğer bu ayarı açarsanız modifier objenin konum değerlerini de değiştirir.

* #### Owner
Obje için konum işlemlerinin gerçekleşeceği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Influence
Modifier'ın etki derecesi.



## [Limit Rotation](https://docs.blender.org/manual/en/latest/animation/constraints/transform/limit_rotation.html)
Objenin rotasyonunu belirttiğiniz minimum ve maximum değerleri arasında tutar.


* #### Limit X/Y/Z
Objenin rotasyonu bu eksenlerde belirttiğiniz değerlerden daha az ve fazla olamaz. Eğer tik işaretine basıp ekseni açarsanız verdiğiniz değer kullanılır, açmazsanız objenin rotasyonu için değer belirlememişsiniz demektir (yani istediğiniz değeri verebilirsiniz).

* #### Order
XYZ eksenleri için rotasyon sıralamasını belirtir.

* #### Affect Transform
Bu ayar kapalı iken modifier objenin rotasyon değerini gerçekten değiştirmez. Yani aslında objeyi döndürürseniz objenin rotasyon değeri limiti geçebilir ama modifier objeyi orijinal rotasyonunda göstermez, yani modifier objeyi sanki limit rotasyonundaymış gibi gösterir ama aslında rotasyon değerleri farklıdır (sağdaki panelden görebilirsiniz). Eğer bu ayarı açarsanız modifier objenin rotasyon değerlerini de değiştirir.

* #### Owner
Obje için rotasyon işlemlerinin gerçekleşeceği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Influence
Modifier'ın etki derecesi.



## [Limit Scale](https://docs.blender.org/manual/en/latest/animation/constraints/transform/limit_scale.html)
Objenin scale değerini belirttiğiniz minimum ve maximum değerleri arasında tutar.


* #### Minimum X/Y/Z
Objenin scale değeri bu eksenlerde belirttiğiniz değerden daha az olamaz. Eğer tik işaretine basıp ekseni açarsanız verdiğiniz değer kullanılır, açmazsanız objenin scale değeri için minimum değer belirlememişsiniz demektir (yani istediğiniz değeri verebilirsiniz).

* #### Maximum X/Y/Z
Objenin scale değeri bu eksenlerde belirttiğiniz değerden daha fazla olamaz. Eğer tik işaretine basıp ekseni açarsanız verdiğiniz değer kullanılır, açmazsanız objenin scale değeri için maximum değer belirlememişsiniz demektir (yani istediğiniz değeri verebilirsiniz).

* #### Affect Transform
Bu ayar kapalı iken modifier objenin scale değerini gerçekten değiştirmez. Yani aslında objeyi scale ederseniz objenin scale değeri limiti geçebilir ama modifier objeyi orijinal scale değerinde göstermez, yani modifier objeyi sanki limit scale değerindeymiş gibi gösterir ama aslında scale değerleri farklıdır (sağdaki panelden görebilirsiniz). Eğer bu ayarı açarsanız modifier objenin scale değerlerini de değiştirir.

* #### Owner
Obje için scale işlemlerinin gerçekleşeceği uzayı belirtir.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Influence
Modifier'ın etki derecesi.



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
Modifier'ın etki derecesi.



## [Transformation](https://docs.blender.org/manual/en/latest/animation/constraints/transform/transformation.html)
a






