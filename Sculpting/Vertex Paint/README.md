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
Renklerin geçişini yumuşatır, yani bütün vertex'lerde [Blur](#blur) brush'ını kullanmışsınız gibi yapar.


## [Dirty Vertex Colors](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#dirty-vertex-colors)
Cavity yani oyuklara, girinti/çıkıntılara göre siyahtan beyaza (0-1) vertex'leri koyulaştırır/rengini değiştirir. Altta kalan kısımlar siyaha (0), üstte kalan kısımlar beyaza (1) kayacak şekilde.


* #### Blur Strength
Yumuşatma derecesi, yani vertex'lerin renk geçişlerinin ne kadar yumuşatılacağını belirler.

* #### Blur Iterations
Yumuşatma işlemi tekrar sayısı, kaç defa yumuşatma uygulanacağını belirler.

* #### Highlight Angle
a

* #### Dirt Angle
a

* #### Dirt Only
a

* #### Normalize
a


## [Vertex Color from Weight](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#vertex-color-from-weight)
Vertex'leri Weight değerlerine göre siyahtan beyaza (0-1) renklendirir.


## [Invert](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#invert)
Renkleri tam tersine çevirir.


## [Levels](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#levels)
a

## [Hue/Saturation/Value](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#hue-saturation-value)
Renklerin Hue/Saturation/Value değerlerini ayarlar. Hue renkleri renk paletinde saat yönünde döndürmeye yarar, [burada](https://www.gastroshot.com/fotografta-hue-nedir/) daha güzel anlatılmış. Saturation, renkleri renk paletinde uç noktalara getirir yani rengin renkliliğini arttırır, [burada](https://www.gastroshot.com/fotografta-saturation-nedir/) daha güzel anlatılmış. Value, renklerin koyuluk/açıklık derecesini ayarlar.


## [Brightness/Contrast](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#brightness-contrast)
Renklerin Brightness/Contrast değerlerini ayarlar. Brightness renkleri siyaha veya beyaza doğru kaydırır. Contrast renklerin [kontrast'ını](https://en.wikipedia.org/wiki/Contrast_(vision)) arttırır/azaltır.


## [Set Vertex Colors](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#set-vertex-colors)
Bütün geometriyi brush'ın şu anki rengine ayarlar. Kısayolu "Ctrl + X" dir ([Kısayollar](#kısayollar-1) bölümüne bakın).


## [Sample Color](https://docs.blender.org/manual/en/latest/sculpt_paint/vertex_paint/editing.html#sample-color)
Seçtiğiniz vertex'in rengini brush'ınızın rengi olarak ayarlar. Kısayolu "Shift + X" dir.


<br>
<br>


# Kısayollar

Kısayol | Açıklama
:---: | :---:
Shift + Sol Tık | Herhangi bir brush'ta "Shift" kısayoluna basılı tutarak çizim yapmak "Smooth" modunu açar, yani [Blur](#blur) brush'ını kullanmanıza yarar.
Ctrl + X | [Set Vertex Colors](#set-vertex-colors) aracının kısayoludur. Bütün geometriyi brush'ın şu anki rengine ayarlar.
1 | [Face Selection](#facevertex-selection-1) modunun kısayoludur.
2 | [Vertex Selection](#facevertex-selection-1) modunun kısayoludur.


