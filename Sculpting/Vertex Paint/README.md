# [Brushlar](#brushlar-1)
* [Draw](#draw)
* [Blur](#blur)
* [Average](#average)
* [Smear](#smear)


<br>
<br>


# Brushlar
Bu kategoride her bir fırçanın kendisine özel ayarlarının ve ne işe yaradığının açıklamaları vardır. Burada sadece Vertex Paint brush'larına özel olan ayarlara yer verilmiştir, diğer ayarlara [Sculpt Mode](../Sculpt) bölümünden ulaşabilirsiniz.


## [Draw](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/tools.html)
Klasik çizim brush'ıdır. Seçtiğiniz rengi çizer.


* #### Blend
Çizim yaptığınız vertex'lerin renkleri ile brush'ınızın renginin nasıl karıştırılacağını belirleyen tekniktir. Bunları ben de çok fazla anlamadığım için [bu linkten](https://docs.krita.org/en/reference_manual/blending_modes.html) tekniklerin açıklamalarına ulaşabilirsiniz.

### Color Picker
Brush'ın rengini ayarlamanıza yarar. "Color" ve "Secondary Color" şeklinde iki renk seçebilirsiniz. Çizim yaparken geçici olarak 2. rengi kullanmak için çizime başlamadan önce "Ctrl" kısayoluna basılı tutmanız yeterlidir. İki rengin yerini değiştirmek için ise yandaki "Swap Colors" butonunu veya "X" kısayolunu kullanabilirsiniz. Onun yanındaki "Use Unified Color" ayarını açarak da renk değerini bütün fırçalara uygulayabilirsiniz.


### Color Palette
Buradan kendinize renk paleti oluşturabilirsiniz. Artı butonuna bastığınızda "Color Picker" menüsünde seçili olan ilk renk değeri palete kaydedilir.


### Advanced

* #### Affect Alpha
Bu ayar açıkken renklerin alpha değerleri de değiştirilir. Kapalıyken değiştirilmez.


### Falloff

* #### Front-Face Falloff
Bu ayar vertex'lerin normal'ları yani baktıkları yön ile kameranın baktığı yönün farkına göre işlemi kısmaya yarar. Kameranın yönü ile "Angle" ayarında belirttiğiniz açı değerinden fazla farka sahip olan vertex'lere falloff uygulanır.



## [Blur](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/tools.html)
Çizim yaptığınız yerdeki vertex'lerin renkleri çevresindeki vertex'lerin renklerine göre ortalanır. Yani vertex'lerin renklerini çevresindeki vertex'lerin renklerinin ortalamasına benzetir. Bu da renk geçişini yumuşatır.


* #### Blend
Renklerin nasıl karıştırılacağını belirleyen tekniktir. Bunları ben de çok fazla anlamadığım için [bu linkten](https://docs.krita.org/en/reference_manual/blending_modes.html) tekniklerin açıklamalarına ulaşabilirsiniz.


### Advanced

* #### Affect Alpha
Bu ayar açıkken renklerin alpha değerleri de değiştirilir. Kapalıyken değiştirilmez.


### Falloff

* #### Front-Face Falloff
Bu ayar vertex'lerin normal'ları yani baktıkları yön ile kameranın baktığı yönün farkına göre işlemi kısmaya yarar. Kameranın yönü ile "Angle" ayarında belirttiğiniz açı değerinden fazla farka sahip olan vertex'lere falloff uygulanır.



## [Average](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/tools.html)
[Blur](#blur) brush'ına benzer ama çalışma şekli farklıdır. Çizim yaptığınız yerdeki vertex'lerin rengini, brush'ınızın yarıçapı içerisindeki bütün vertex'lerin renginin ortalaması olarak ayarlar.


* #### Blend
Renklerin nasıl karıştırılacağını belirleyen tekniktir. Bunları ben de çok fazla anlamadığım için [bu linkten](https://docs.krita.org/en/reference_manual/blending_modes.html) tekniklerin açıklamalarına ulaşabilirsiniz.


### Advanced

* #### Affect Alpha
Bu ayar açıkken renklerin alpha değerleri de değiştirilir. Kapalıyken değiştirilmez.


### Falloff

* #### Front-Face Falloff
Bu ayar vertex'lerin normal'ları yani baktıkları yön ile kameranın baktığı yönün farkına göre işlemi kısmaya yarar. Kameranın yönü ile "Angle" ayarında belirttiğiniz açı değerinden fazla farka sahip olan vertex'lere falloff uygulanır.



## [Smear](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/tools.html)
[Clay Thumb](../Sculpt#clay-thumb) brush'ının renkler için versiyonudur denebilir. Sanki parmağınızı kullanarak renkleri sürüklüyormuşsunuz gibi efekt verir. Yani geometriyi değil de renkleri çekiştiriyormuşsunuz gibi düşünün.


* #### Blend
Renklerin nasıl karıştırılacağını belirleyen tekniktir. Bunları ben de çok fazla anlamadığım için [bu linkten](https://docs.krita.org/en/reference_manual/blending_modes.html) tekniklerin açıklamalarına ulaşabilirsiniz.


### Advanced

* #### Affect Alpha
Bu ayar açıkken renklerin alpha değerleri de değiştirilir. Kapalıyken değiştirilmez.


### Falloff

* #### Front-Face Falloff
Bu ayar vertex'lerin normal'ları yani baktıkları yön ile kameranın baktığı yönün farkına göre işlemi kısmaya yarar. Kameranın yönü ile "Angle" ayarında belirttiğiniz açı değerinden fazla farka sahip olan vertex'lere falloff uygulanır.


