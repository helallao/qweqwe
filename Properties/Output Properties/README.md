Aşağıdaki döküman Cycles render motoru kullanıldığı varsayılarak hazırlanmıştır. Cycles için output ayarlarının açıklamaları (Properties > Output) vardır. Eğer farklı bir render motoru kullanıyorsanız birçok özellik farklılık gösterecek veya çalışmayacaktır.


# [Format](#format-1)
* [Resolution X](#resolution-x)
* [Resolution Y](#resolution-y)
* [Resolution Percentage (%)](#resolution-percentage-)
* [Aspect X](#aspect-x)
* [Aspect Y](#aspect-y)
* [Render Region](#render-region)
* [Crop to Render Region](#crop-to-render-region)
* [Frame Rate](#frame-rate)

# [Frame Range](#frame-range-1)
* [Frame Start](#frame-start)
* [Frame End](#frame-end)
* [Frame Step](#frame-step)
* [Old (Frame Stretching)](#old)
* [New (Frame Stretching)](#new)


<br>
<br>


# [Format](https://docs.blender.org/manual/en/3.6/render/output/properties/format.html)
Bu kategori render çıktısı için ekran boyutunun (çözünürlük) ve frame rate'inin (fps) ayarlarının olduğu bölümdür.


* #### Resolution X
X ekseninde (Width) render çıktısının boyutunu temsil eder.

* #### Resolution Y
Y ekseninde (Height) render çıktısının boyutunu temsil eder.

* #### Resolution Percentage (%)
Render çıktısının boyutunun yani çözünürlüğünün "Resolution X" ve "Resolution Y" değerlerine dayanarak yüzdelik değeri. Yani bu değer %100 iken çıktının boyutu "Resolution X" ve "Resolution Y" değerlerine eşit olur. Eğer bu ayarı düşürürseniz, mesela %50 yaparsanız çıktının boyutu da yarıya düşer.

* #### Aspect X
Aspect ratio yani en boy oranı için X ekseni değeri. Bu değeri attırırsanız X ekseni sündürülür. En boy oranı standart orandan farklı olan ekranlar içindir.

* #### Aspect Y
Aspect ratio yani en boy oranı için Y ekseni değeri. Bu değeri attırırsanız Y ekseni sündürülür. En boy oranı standart orandan farklı olan ekranlar içindir.

* #### Render Region
Bu ayar açıkken sadece ["Render Region"](https://docs.blender.org/manual/en/3.6/editors/3dview/navigate/regions.html#render-region) olarak seçilen yer render edilir. Çıktının geriye kalan yerleri görünmez olarak ayarlanır.

* #### Crop to Render Region
Sadece "Render Region" ayarı açıkken vardır. Bu ayar açık değilken "Render Region" ayarı seçilen kısmı render eder, geriye kalan kısımlar ise görünmez olarak ayarlanır. Yani çıktı hala aynı boyuttadır ve sadece "Render Region" olarak seçilen kısım render edilir. Eğer bu ayarı açarsanız çıktıda arka plan da gösterilmez. Sadece "Render Region" olarak seçilen kısım render edilir ve bu kısım çıktının kendisidir.

* #### Frame Rate
Animasyonun frame rate'i (fps, kare hızı).


<br>
<br>


# [Frame Range](https://docs.blender.org/manual/en/3.6/render/output/properties/frame_range.html)
Bu kategori yaptığınız animasyonun frame (fps, kare hızı) sayısını ve hızını ayarladığınız bölümdür.


* #### Frame Start
Başlangıç frame'i.

* #### Frame End
Bitiş frame'i.

* #### Frame Step
Frame başına atlanacak frame sayısı, adım sayısı. Mesela bunu 2 yaparsanız her 2 frame'in biri animasyonda oynatılır.


## Frame Stretching

* #### Old
"Frame Stretching" frame ile oynatma hızının birbirlerinden farklı olarak ilerlemesini sağlar. Verdiğimiz orana göre animasyonu daha hızlı veya yavaş ilerlemeye alabiliriz. Blender'da default olarak bu ayar 100 olarak geliyor, aslında bu sayının kaç olduğunun önemi yok, önemli olan "Old" ile "New" sayılarının arasındaki oran. Mesela "Old" ve "New" 1 olarak ayarlanırsa oranlar eşit olacağı için 100'e ayarlandıklarında çıkacak animasyonunun aynısı olacaktır. Eğer oranlar farklı olursa, mesela "Old" 2, "New" 1 olursa oynatma hızı 2 kat daha hızlı oynatılacaktır. Oynatma hızının hızlı oynatılması ile frame hızı farklı şeylerdir, eğer animasyonu oynatırsanız bunu görebilirsiniz. Frame sayısı henüz yarıdayken animasyonun tamamının oynatıldığını görebilirsiniz. Yani oynatma hızını 2 katına çıkarmış olursunuz. Bu şekilde oynatma hızını hızlandırabilir/yavaşlatabilirsiniz. Ayrıca oranı manuel olarak hesaplamaktansa, eski ve yeni animasyonların frame sayısını girerek animasyonunuzun oynatma hızını başka bir animasyonun hızına ayarlayabilirsiniz.

* #### New
"Frame Stretching" frame ile oynatma hızının birbirlerinden farklı olarak ilerlemesini sağlar. Verdiğimiz orana göre animasyonu daha hızlı veya yavaş ilerlemeye alabiliriz. Blender'da default olarak bu ayar 100 olarak geliyor, aslında bu sayının kaç olduğunun önemi yok, önemli olan "Old" ile "New" sayılarının arasındaki oran. Mesela "Old" ve "New" 1 olarak ayarlanırsa oranlar eşit olacağı için 100'e ayarlandıklarında çıkacak animasyonunun aynısı olacaktır. Eğer oranlar farklı olursa, mesela "Old" 2, "New" 1 olursa oynatma hızı 2 kat daha hızlı oynatılacaktır. Oynatma hızının hızlı oynatılması ile frame hızı farklı şeylerdir, eğer animasyonu oynatırsanız bunu görebilirsiniz. Frame sayısı henüz yarıdayken animasyonun tamamının oynatıldığını görebilirsiniz. Yani oynatma hızını 2 katına çıkarmış olursunuz. Bu şekilde oynatma hızını hızlandırabilir/yavaşlatabilirsiniz. Ayrıca oranı manuel olarak hesaplamaktansa, eski ve yeni animasyonların frame sayısını girerek animasyonunuzun oynatma hızını başka bir animasyonun hızına ayarlayabilirsiniz.



