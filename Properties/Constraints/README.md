# Ek Bilgiler

<details>
<summary>Kullanılan Güzel Kaynaklar</summary>
<br>

* [The Blender 2.8 Encyclopedia](https://www.udemy.com/course/the-blender-encyclopedia/) - Udemy'deki sayısı bir elin parmaklarını geçmeyecek kadar az olan, gerçekten uğraşılmış kurslardan birisi. Bizim için önemli olan 8. bölüm "Constraints", constraints'lerin açıklamalarının olduğu bölüm, tabi isterseniz diğer kısımlara da bakabilirsiniz. [Buradan](https://btdig.com/search?q=The+Blender+2.8+Encyclopedia) torrent'ini bulabilirsiniz (vpn gerekebilir).

</details>



# [Motion Tracking](#motion-tracking-1)
* [Camera Solver](#camera-solver)

# [Transfrom](#transfrom-1)
* [Copy Location](#copy-location)
* [Copy Rotation](#copy-rotation)
* [Copy Scale](#copy-scale)
* [Copy Transforms](#copy-transforms)


<br>
<br>


# [Motion Tracking](https://docs.blender.org/manual/en/latest/animation/constraints/index.html#motion-tracking)
Bilmiyorum.


## [Camera Solver](https://docs.blender.org/manual/en/latest/animation/constraints/motion_tracking/camera_solver.html)
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







