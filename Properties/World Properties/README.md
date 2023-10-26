Aşağıdaki döküman Cycles render motoru kullanıldığı varsayılarak hazırlanmıştır. Cycles için render ayarlarının açıklamaları (Properties > Render) vardır. Eğer farklı bir render motoru kullanıyorsanız birçok özellik farklılık gösterecek veya çalışmayacaktır. Bu bölümdeki ayarları anlamak için [Shader Nodes](../../Shader%20Nodes) bölümüne de bakın.


# [Preview](#preview-1)

# [Surface](#surface-1)
* [Surface](#surface-2)

# [Volume](#volume-1)
* [Volume](#volume-2)

# [Ray Visibility](#ray-visibility-1)
* [Camera](#camera)
* [Diffuse](#diffuse)
* [Glossy](#glossy)
* [Transmission](#transmission)
* [Volume Scatter](#volume-scatter)

# [Settings](#settings-1)
* [Sampling (Surface)](#sampling)
* [Map Resolution (Surface)](#map-resolution)
* [Max Bounces (Surface)](#max-bounces)
* [Shadow Caustics (Surface)](#shadow-caustics)
* [Sampling (Volume)](#sampling)
* [Interpolation (Volume)](#interpolation)
* [Homogeneous (Volume)](#homogeneous)
* [Step Size (Volume)](#step-size)
* [Light Group (Light Group)](#light-group)


<br>
<br>


# [Preview]()
Buradan dünyanızın preview'ini (öngösterim) görebilirsiniz.


<br>
<br>


# [Surface]()
Bu kategoride World yani sahne için shader ayarları vardır.


* #### Surface
Bu ayar Shader Editör'ünde "World" modunda shader kodlamak ile aynıdır. Surface ayarı [World Output](https://github.com/helallao/qweqwe/tree/main/Shader%20Nodes#world-output) node'unun [Surface](https://github.com/helallao/qweqwe/tree/main/Shader%20Nodes#surface-socket-input-2) output'unu temsil eder. Dünyanın yani sahnenin shader'ını ayarlar.


<br>
<br>


# [Volume]()
Bu kategoride World yani sahne için shader ayarları vardır.


* #### Volume
Bu ayar Shader Editör'ünde "World" modunda shader kodlamak ile aynıdır. Volume ayarı [World Output](https://github.com/helallao/qweqwe/tree/main/Shader%20Nodes#world-output) node'unun [Volume](https://github.com/helallao/qweqwe/tree/main/Shader%20Nodes#volume-socket-input-1) output'unu temsil eder. Dünyanın yani sahnenin shader'ını ayarlar.


<br>
<br>


# [Ray Visibility](https://docs.blender.org/manual/en/latest/render/cycles/world_settings.html#ray-visibility)
Ray (ışık ışınları) için visibility yani görünürlük ayarlarının olduğu kategoridir. Eğer ray'ler (ışık ışınları) hakkında bilgili değilseniz [Shader Nodes](../../Shader%20Nodes) bölümünün [Ek Bilgiler](../../Shader%20Nodes#ek-bilgiler) bölümündeki "The Cycles Encyclopedia" kitabını okuyun.


* #### Camera
Kamera ray'lerini görünmez yapar. [Bakınız](../../Shader%20Nodes#is-camera-ray-output).

* #### Diffuse
Diffuse ray'lerini görünmez yapar. [Bakınız](../../Shader%20Nodes#is-diffuse-ray-output).

* #### Glossy
Glossy ray'lerini görünmez yapar. [Bakınız](../../Shader%20Nodes#is-glossy-ray-output).

* #### Transmission
Transmission ray'lerini görünmez yapar. [Bakınız](../../Shader%20Nodes#is-transmission-ray-output).

* #### Volume Scatter
Volume Scatter'den gelen ray'leri görünmez yapar.


<br>
<br>


# [Settings](https://docs.blender.org/manual/en/latest/render/cycles/world_settings.html#ray-visibility)
Dünya shader'ının render'ı hakkında ayarların olduğu kategoridir.


## Surface

* #### Sampling
"Sampling" dünya shader'ının sahnedeki objeler üzerindeki ışık etkisinin kalitesini belirler. Bu ayar sampling modunu belirler. "None" modunda sampling kullanılmaz ve render'da noise olabilir. "Manual" modunda sampling ayarlarını yapabilirsiniz. "Auto" modunda sampling ayarı otomatik olarak belirlenir. "Manual" veya "Auto" modunu seçmek "Multiple Importance Sampling" ayarını açar. Bu ayar render'daki noise'ı azaltan bi özelliktir. Ayrıca [burayı](https://projects.blender.org/blender/blender/issues/72314) da okuyabilirsiniz, ".blend" dosyalarını yükleyerek kendiniz test edip bu ayarı anlayabilirsiniz.

* #### Map Resolution
Dünya shader'ının sahnedeki objeler üzerindeki ışık etkisinin kalitesini belirler. Bu değeri arttırmak render'daki noise'ı düşürür ama daha fazla ram kullanımı olur. Eğer HDRi kullanıyorsanız ve render üzerinde parlak noktalar (firefly) oluyorsa, bu ayarı arttırın.

* #### Max Bounces
Dünya shader'ından gelen ışıkların kameraya gelmeden önceki maksimum sekme sayısı.

* #### Shadow Caustics
Bilmiyorum.


## Volume

* #### Sampling
Bilmiyorum.

* #### Interpolation
Bilmiyorum.

* #### Homogeneous
Bilmiyorum.

* #### Step Size
Bilmiyorum.


## Light Group

* #### Light Group
Bilmiyorum.











