# [Scene](#scene-1)
* [Camera](#camera)
* [Background Scene](#background-scene)
* [Active Clip](#active-clip)

# [Units](#units-1)
* [Unit System](#unit-system)
* [Unit Scale](#unit-scale)
* [Separate Units](#separate-units)
* [Rotation](#rotation)
* [Length](#length)
* [Mass](#mass)
* [Time](#time)
* [Temperature](#temperature)

# [Gravity](#gravity-1)
* [Gravity X](#gravity-x)
* [Gravity Y](#gravity-y)
* [Gravity Z](#gravity-z)

# [Keying Sets](#keying-sets-1)

# [Audio](#audio-1)
* [Volume](#volume)
* [Distance Model](#distance-model)
* [Doppler Speed](#doppler-speed)
* [Doppler Factor](#doppler-factor)
* [Update Animation Cache](#update-animation-cache)

# [Rigid Body World](#rigid-body-world)


<br>
<br>


# [Scene](https://docs.blender.org/manual/en/3.6/scene_layout/scene/properties.html#scene)
Bu kategoride sahne ile ilgili ayarlar var.


* #### Camera
Render'da kullanılacak kamera, aktif kamera. Sahnenizde aktif kamera üzerindeki üçgen dolu olan kameradır.

* #### Background Scene
Başka bir sahneyi şu anki sahne için arka plan olarak kullanabilirsiniz. Seçtiğiniz sahnedeki dünya görünümü arka plan olarak ayarlanır.

* #### Active Clip
Bilmiyorum.


<br>
<br>


# [Units](https://docs.blender.org/manual/en/3.6/scene_layout/scene/properties.html#units)
Bu kategoride sahnenin ölçü sistemi ile ilgili ayarlar var.


* #### Unit System
Kullanılacak ölçü sistemi. "None" seçerek blender'ın kendi ölçü sistemini, "Metric" seçerek metrik sistemi yani bizim de kullandığımız (metre, kilogram falan) ölçü sistemini, "Imperial" seçerek ingiliz ölçü sistemini (inch, feet falan) kullanabilirsiniz.

* #### Unit Scale
Ölçü değerleri için çarpan görevi görür.

* #### Separate Units
Ölçü değerlerini alt birimleriyle beraber gösterir. 1m yerine, 1m 0cm gibi.

* #### Rotation
Açılar için kullanılacak ölçü birimi, "Degrees" seçerek derece, "Radians" seçerek radyan kullanabilirsiniz.

* #### Length
Uzunluk için kullanılacak ölçü birimi. "Adaptive" seçerek otomatik moda alabilirsiniz, yani mesela 1000m olunca otomatikmen kilometre kullanmaya geçer ve 1km olur gibi.

* #### Mass
Ağırlık için kullanılacak ölçü birimi. "Adaptive" seçerek otomatik moda alabilirsiniz, yani mesela 1000 gr olunca otomatikmen kilogram kullanmaya geçer ve 1 kg olur gibi.

* #### Time
Süre için kullanılacak ölçü birimi. "Adaptive" seçerek otomatik moda alabilirsiniz, yani mesela 60 saniye olunca otomatikmen dakika kullanmaya geçer ve 1 dk olur gibi.

* #### Temperature
Sıcaklık için kullanılacak ölçü birimi.


<br>
<br>


# [Gravity](https://docs.blender.org/manual/en/3.6/scene_layout/scene/properties.html#gravity)
Bu kategoride yerçekimi ile ilgili ayarlar var.


* #### Gravity X
Fizik efektleri (Physics Effects) için X ekseninde yerçekimi. 

* #### Gravity Y
Fizik efektleri (Physics Effects) için Y ekseninde yerçekimi. 

* #### Gravity Z
Fizik efektleri (Physics Effects) için Z ekseninde yerçekimi. 


<br>
<br>


# [Keying Sets](https://docs.blender.org/manual/en/3.6/animation/keyframes/keying_sets.html)
Bu kategoride "Keying Sets" ile ilgili ayarlar var. Blender'ın bu konu ile ilgili kendi kaynağını yeterince açıklayıcı buldum, linke tıklayarak okuyabilirsiniz. Ayrıca "Keying Sets" konusu birazcık animasyon editörleri bilgisi gerektirir, youtube'den blender'da timeline kullanımı hakkında videolara bakarsanız zaten hemen anlarsınız ([mesela bu](https://www.youtube.com/watch?v=BLebjFHiDqk)).


<br>
<br>


# [Audio](https://docs.blender.org/manual/en/3.6/scene_layout/scene/properties.html#audio)
Bu kategoride sahnedeki sesler ile ilgili ayarlar vardır.


* #### Volume
Sahne için ses seviyesi.

* #### Distance Model
Sesin uzaklığa göre azalma modu. Bu modlar hakkında teknik bilgi edinmek istiyorsanız [buraya](https://www.openal.org/documentation/openal-1.1-specification.pdf) bakabilirsiniz.

* #### Doppler Speed
[Doopler Etkisi](https://en.wikipedia.org/wiki/Doppler_effect) için sesin hızı, mesela bu değer hava için 343.3 m/s, su için 1560 m/s dir. Eğer spesifik bir ortam için Doppler Etkisi ses hızını arıyorsanız google'da aratabilirsiniz.

* #### Doppler Factor
[Doopler Etkisi](https://en.wikipedia.org/wiki/Doppler_effect) şiddetini kontrol eder.

* #### Update Animation Cache
Animasyonun önbellekteki ses verilerini siler. Refresh atar yani.


<br>
<br>


# [Rigid Body World](https://docs.blender.org/manual/en/3.6/scene_layout/scene/properties.html#rigid-body-world)
Bilmiyorum.










