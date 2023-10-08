# Kategoriler

* [Input](#input)


<br>
<br>


# Input



## Ambient Occlusion
Mesh'in gölgede kalan kısımlarını hesaplar ve renk mapini verir.


* #### [Color (Output)]()
Mesh Color inputuna verilen renk ile boyanmıştır. Bu output ise mesh'in rengini verir ama tamamen Color inputuna verilen renk ile boyanmış halde degil de, gölge vuran kısımların siyaha kaymış halini verir.

* #### [AO (Output)]()
Gölge vuran kısımların siyaha kaymış, diger kısımların da beyaz oldugu siyah-beyaz 1d renk.

* #### [Samples (Input)]()
Gölge vuran kısımların kalitesi.

* #### [Inside (Input)]()
Gölge vuran kısımlar mesh'in içine göre hesaplanır.

* #### [Only Local (Input)]()
Açıkken gölgeler sadece mesh'in kendisinden gelir. Kapalıyken başka objelerden de gölge gelebilir.

* #### [Color (Input)]()
Mesh'in rengi.

* #### [Distance (Input)]()
Gölgelerin maksimum gidebilecegi mesafe. Normalde gölgeler köşelerden mesh'in etrafına dogru biraz yayılır. Bu ayar ile yayılım mesafesini ayarlarsın. Eger bu ayarı kısarsan gölgelerin köşeye dogru kısıtlandıgını görebilirsin.

* #### [Normal (Input)]()
Bilmiyorum.
