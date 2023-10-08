# Kategoriler

* [Input](#input)


<br>
<br>


# Input



## [Ambient Occlusion](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/ao.html)
Mesh'in üzerindeki gölgeleri veya gölgede kalan kısımlarını hesaplıp renki ve grayscale map'lerini verir. Bu hesaplama aslında ışıktan bağımsızdır yani gerçekten ışığın nereye vurduğunu nereye vurmadığını kontrol etmez. Gölgeleme işlemi çoğunlukla mesh'in kenarlarında ve çevresi bloklanan kısımlarında olur.


* #### Color (Output)
"Color" inputuna verdiginiz renk map'inin gölge vuran kısımlarının siyaha kaymış halini verir. Yani renkli map'e sanki gölge vurmuş gibi siyah renk eklenmiş halini verir.

* #### AO (Output)
Gölge vuran kısımların siyaha kaymış, diger kısımların da beyaz oldugu siyah-beyaz 1d renk.

* #### Samples (Input
Gölge vuran kısımların kalitesi.

* #### Inside (Input)
Gölge vuran kısımlar mesh'in içine göre hesaplanır.

* #### Only Local (Input)
Açıkken gölgeler sadece mesh'in kendisinden gelir. Kapalıyken başka objelerden de gölge gelebilir.

* #### Color (Input)
Mesh'in rengi.

* #### Distance (Input)
Gölgelerin maksimum gidebilecegi mesafe. Normalde gölgeler köşelerden mesh'in etrafına dogru biraz yayılır. Bu ayar ile yayılım mesafesini ayarlarsın. Eger bu ayarı kısarsan gölgelerin köşeye dogru kısıtlandıgını görebilirsin.

* #### Normal (Input)
Bilmiyorum.
