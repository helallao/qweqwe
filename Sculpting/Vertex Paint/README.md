Bu bölüm Vertex Paint editörünü anlatıyor lakin Blender bu işlerde yeni yeni gelişmekte olduğu için çok az brush'a sahip. Ayrıca Vertex Paint ile ilgili bazı brush'lar bu editörde yer almamakta, mesela Sculpt editöründeki [Paint](../Sculpt#paint) ve [Smear](../Sculpt#smear) brush'ları burdaki [Draw](#draw) ve [Smear](#smear) brush'larına göre daha fazla özelliğe sahip, buna ek olarak Sculpt editöründe [Color Filter](../Sculpt#color-filter) ve [Mask by Color](../Sculpt#mask-by-color) brush'ları vardır. Yani anlayacağınız üzere bu editör o kadar da kapsamlı ve kullanışlı bir editör değil.

# [Brushlar](#brushlar-1)
* [Draw](#draw)
* [Blur](#blur)
* [Average](#average)
* [Smear](#smear)

# [Kısayollar](#kısayollar-1)


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



<br>
<br>


# Paint İşlemleri
Bu kategoride üst toolbar'ın (araç çubuğu) sol köşesinden ulaşabileceğiniz "Paint" kategorisindeki işlemlerin açıklamaları vardır.


## [Smooth Vertex Colors](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#smooth-vertex-colors)
a

## [Dirty Vertex Colors](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#dirty-vertex-colors)
a

## [Vertex Color from Weight](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#vertex-color-from-weight)
a

## [Invert](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#invert)
a

## [Levels](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#levels)
a

## [Hue/Saturation/Value](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#hue-saturation-value)
a

## [Brightness/Contrast](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#brightness-contrast)
a

## [Set Vertex Colors](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#set-vertex-colors)
a

## [Sample Color](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#sample-color)
a


<br>
<br>


# Kısayollar

Kısayol | Açıklama
:---: | :---:
Shift + Sol Tık | Herhangi bir brush'ta "Shift" kısayoluna basılı tutarak çizim yapmak "Smooth" modunu açar, yani [Blur](#blur) brush'ını kullanmanıza yarar.
Ctrl + X | [Set Vertex Colors](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#set-vertex-colors) aracının kısayoludur. Bütün geometriyi brush'ın şu anki rengine ayarlar.
1 | a
2 | a


