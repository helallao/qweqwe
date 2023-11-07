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
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Owner
Obje için hareketlerin gerçekleşeceği uzayı belirtir. Mesela bu ayarı "Local Space" yaparsanız objenin hareketlerinin kendi lokal uzayına göre olduğunu söylemiş olursunuz. Yani mesela diyelim ki obje X ekseninde ilerleyecek, eğer bu ayar "Local Space" ise ve objenin lokal X ekseni dünya üzerinde Y ekseni ise, o zaman obje X ekseninde ilerlerken aslında dünya üzerinde Y ekseninde ilerler. Yani demek istediğim şey eksenler birbirlerinden farklı olabilir, bu ayarı kullanarak seçtiğiniz uzayın eksenleri ne ise o kullanılır.

Mod | Açıklama
:---: | :---:
‎World Space | Dünya uzayı (eksenleri) kullanılır.
‎Custom Space | "Object" input'una verdiğiniz objenin lokal uzayı (eksenleri) kullanılır.
‎Local Space | Objenin lokal uzayı (eksenleri) kullanılır.

* #### Influence
Modifier'ın etki derecesi. Bunu hareketleri/konumu kopyalama derecesi olarak da düşünebilirsiniz. Mesela bu ayarı 0.5 yaparsanız, hedef obje 2 birim ilerlediğinde obje 1 birim ilerler, yani yarıya indirmiş olursunuz.








