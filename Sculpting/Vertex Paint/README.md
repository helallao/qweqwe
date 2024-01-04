Bu bölüm Vertex Paint editörünü anlatıyor lakin Blender bu işlerde yeni yeni gelişmekte olduğu için çok az brush'a sahip. Ayrıca Vertex Paint ile ilgili bazı brush'lar bu editörde yer almamakta, mesela Sculpt editöründeki [Paint](../Sculpt#paint) ve [Smear](../Sculpt#smear) brush'ları burdaki [Draw](#draw) ve [Smear](#smear) brush'larına göre daha fazla özelliğe sahip, buna ek olarak Sculpt editöründe [Color Filter](../Sculpt#color-filter) ve [Mask by Color](../Sculpt#mask-by-color) brush'ları vardır. Yani anlayacağınız üzere bu editör o kadar da kapsamlı ve kullanışlı bir editör değil.

# [Brushlar](#brushlar-1)
* [Draw](#draw)
* [Blur](#blur)
* [Average](#average)
* [Smear](#smear)

# [Paint İşlemleri](#paint-i̇şlemleri-1)

# [Face/Vertex Selection](#facevertex-selection-1)

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


# Face/Vertex Selection
[Face/Vertex Selection](https://docs.blender.org/manual/en/latest/sculpt_paint/selection_visibility.html) modları sadece seçili olan vertex/face'ler üzerinde işlemler yapmamıza yarayan modlardır. 1 ve 2 kısayolunu kullanarak modlar arasında geçiş yapabilirsiniz ([Kısayollar](#kısayollar-1) bölümüne bakın) veya üst toolbar'ın (araç çubuğu) sol köşesinden manuel olarak da değiştirebilirsiniz. Bu modlardan biri açıldığında sol kenardaki brush menüsüne maske araçları eklenir. Maske araçlarının çalışma şekilleri [Sculpt](../Sculpt#box-mask) modundakiler ile aynıdır. Ayrıca bu modlarda kullanabileceğiniz kısayolların listesine de aşağıdan ulaşabilirsiniz.


Kısayol | Açıklama
:---: | :---:
Alt + Sol Tık | Maske brush'larının dışındaki brush'ları kullanırken bu kısayol ile tek tek vertex/face seçebilirsiniz. Ayrıca "Shift" tuşuna basarak birden fazla seçebilirsiniz. "Face Selection" modundayken ve maske brush'larından biri seçili iken face loop seçmeye yarar.
A | Bütün face/vertex'leri seçer.
A + A | Bütün face/vertex'lerin seçimini kaldırır.
B | Box Selection brush'ının tek kullanımlık kısayolu.
C | Circle Selection brush'ının kısayolu.
Ctrl + I | Seçimi tersine çevirir.
L | Mouse'unuzun altındaki face/vertex'e bağlı olan bütün face/vertex'leri seçer.
Ctrl + L | Şu anda seçili olan face/vertex'lere bağlı olan bütün face/vertex'leri seçer.
Ctrl + Numpad Artı | Seçimi genişletir (uç noktalardaki bağlı olan face/vertex'leri seçer).
Ctrl + Numpad Eksi | Seçimi küçültür (uç noktalardaki face/vertex'lerin seçimini kaldırır).


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
1 | [Face Selection](#facevertex-selection-1) modunun kısayoludur.
2 | [Vertex Selection](#facevertex-selection-1) modunun kısayoludur.


