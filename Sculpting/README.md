Aşağıdaki döküman sözlük mantığında yapılmıştır, herhangi bir konuda genel olarak konu anlatımı sunmaz. Spesifik olarak aradığınız ayarların açıklamaları, kısayollar, özellikler ve konu anlatımlarına ulaşabileceğiniz kaynakların olduğu bir sözlüktür. Aşağıdaki bölümden benim işime yarayan kapsamlı kaynaklar var ama sadece bunları kullanarak öğrenemezsiniz. Sculping konusunda kendinizi geliştirmek için internetten bulabildiğiniz bütün yazılara ve videolara bakmalısınız ve öğrendiklerinizi kendiniz de uygulamalısınız.

<details>
<summary>Kullanılan Güzel Kaynaklar</summary>
<br>

* [CGCookie - Fundamentals of Digital Sculpting](https://cgcookie.com/courses/fundamentals-of-digital-sculpting-with-blender) - Udemy'deki en güzel sculpting kurslarından birisi. [Buradan](https://btdig.com/search?order=0&q=CGCookie+-+Fundamentals+of+Digital+Sculpting) torrent'ini bulabilirsiniz (vpn gerekebilir).
* [CGBoost - Master 3D Sculpting in Blender](https://www.cgboost.com/courses/master-3d-sculpting-in-blender) - En güzel sculpting kurslarından birisi. [Buradan](https://btdig.com/search?q=CGBoost+-+Master+3D+Sculpting+in+Blender) torrent'ini bulabilirsiniz (vpn gerekebilir).
* [Sculpting the Blender Way](https://www.packtpub.com/product/sculpting-the-blender-way/9781801073875) - Sculpting hakkında kapsamlı kaynaklardan birisi. [Buradan](https://annas-archive.org/md5/959e918ffd6c9275fa2b59694168a6a9) pdf'ini indirebilirsiniz.
* [ALL Sculpt Brushes (EXPLAINED) for 3D Print Design](https://www.youtube.com/playlist?list=PLvCZK2JKGQlPK51aQDWAvJJwh-elJiWXP) - Her brush için açıklamaların olduğu youtube playlist'i, isterseniz udemy linkine de [buradan](https://www.udemy.com/course/blender-sculpting-brushes-202/) ulaşabilirsiniz.

</details>

<br>

# [Brushlar](#brushlar-1)
* [Draw](#draw)
* [Draw Sharp](#draw-sharp)
* [Clay](#clay)
* [Clay Strips](#clay-strips)
* [Clay Thumb](#clay-thumb)
* [Layer](#layer)
* [Inflate](#inflate)
* [Blob](#blob)
* [Crease](#crease)
* [Smooth](#smooth)
* [Flatten](#flatten)
* [Fill](#fill)
* [Scrape](#scrape)
* [Multi-plane Scrape](#multi-plane-scrape)
* [Pinch](#pinch)
* [Grab](#grab)
* [Elastic Deform](#elastic-deform)
* [Snake Hook](#snake-hook)
* [Thumb](#thumb)
* [Pose](#pose)
* [Nudge](#nudge)
* [Rotate](#rotate)
* [Slide Relax](#slide-relax)
* [Boundary](#boundary)
* [Cloth](#cloth)
* [Simplify](#simplify)
* [Mask](#mask)
* [Draw Face Sets](#draw-face-sets)
* [Multires Displacement Eraser](#multires-displacement-eraser)
* [Multires Displacement Smear](#multires-displacement-smear)
* [Paint](#paint)
* [Smear](#smear)
* [Box Mask](#box-mask)
* [Lasso Mask](#lasso-mask)
* [Line Mask](#line-mask)
* [Box Hide](#box-hide)
* [Box Face Set](#box-face-set)
* [Lasso Face Set](#lasso-face-set)
* [Box Trim](#box-trim)
* [Lasso Trim](#lasso-trim)
* [Line Project](#line-project)
* [Mesh Filter](#mesh-filter)
* [Cloth Filter](#cloth-filter)
* [Color Filter](#color-filter)
* [Edit Face Set](#edit-face-set)
* [Mask by Color](#mask-by-color)

# [Brush Ayarları](#brush-ayarları-1)
* [Advanced](#advanced)
* [Texture](#texture)
* [Stroke](#stroke)
* [Falloff](#falloff)
* [Cursor](#cursor)

# [Workflowlar](#workflowlar-1)
* [Dynamic Topology (Dyntopo)](#dynamic-topology-dyntopo)
* [Voxel Remesh](#voxel-remesh)
* [Multiresolution](#multiresolution)

# [Kısayollar](#kısayollar-1)


<br>
<br>


# Brushlar
Bu kategoride her bir fırçanın kendisine özel ayarlarının ve ne işe yaradığının açıklamaları vardır.

## [Draw](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/draw.html)
Açıklama. Brush'ın kısayolu "V" dir ([Kısayollar](#kısayollar-1) bölümünden "Brush Kısayolları" na bakın).


* #### Radius
Fırçanın yarıçapı. 3D Viewport üzerinde mouse'unuzun etrafındaki çember fırçanın yarıçapını belirtir. "F" kısayolu ile ayarlayabilirsiniz ([Kısayollar](#kısayollar-1) bölümünden "Genel Kısayollar" a bakın). Yandaki "Size Pressure" ayarını açarak eğer sculpting için çizim tableti kullanıyorsanız, kaleminiz ile ekrana uyguladığınız baskıya göre kendisini otomatikmen değiştiren yarıçap modunu açabilirsiniz. Onun yanındaki "Use Unified Radius" ayarını açarak da yarıçap değerini bütün fırçalara uygulayabilirsiniz.

* #### Radius Unit
Fırçanın yarıçap değerini ayarlamak için kullanılacak birim değerini temsil eder. "View" modundayken yarıçap için piksel birimi kullanılır, bu da sculpting yaptığınız mesh'e olan uzaklığınıza göre fırçanın yarıçapının değişebilmesine sebep olur. "Scene" modunda ise yarıçap için Blender'ın kullandığı sahne birimleri (metre) kullanılır.

* #### Strength
Fırçanın uyguladığı efektin şiddeti, yani fırçanın şiddeti. 3D Viewport üzerinde mouse'unuzun etrafındaki çember fırçanın yarıçapını belirtir, bu çemberin içerisindeki ikinci çember de fırçanın şiddetini belirtir, mesela fırçanın şiddeti 0.5 yani yarım iken iç çemberin dış çemberin yarısı kadar olduğunu görebilirsiniz. "Shift + F" kısayolu ile ayarlayabilirsiniz ([Kısayollar](#kısayollar-1) bölümünden "Genel Kısayollar" a bakın). Yandaki "Strength Pressure" ayarını açarak eğer sculpting için çizim tableti kullanıyorsanız, kaleminiz ile ekrana uyguladığınız baskıya göre kendisini otomatikmen değiştiren fırça şiddeti modunu açabilirsiniz. Onun yanındaki "Use Unified Strength" ayarını açarak da fırça şiddeti değerini bütün fırçalara uygulayabilirsiniz.

* #### Direction
Fırçanın efektinin yönünü belirler. Artı yön mesh'in geometrisini kameraya doğru yaklaştırırken (yani kameraya doğru, efektin uygulandığı yöne doğru), eksi yönü geometriyi tam tersi yöne doğru götürür, yani uzaklaştırır. Fırçanın yönünü değiştirmek için bu ayarları neredeyse hep kısayollar ile kullanırız, yani manuel olarak bu ayarı elle değiştirmekle uğraşmayız. Fırçanın kısayolunu değiştirmek için çizim işlemine başlamadan önce "Ctrl" kısayoluna basılı tutmanız yeterlidir (çizmeye başladıktan sonra bırakabilirsiniz).

* #### Normal Radius
Bu ayar fırçanın normal'ını yani baktığı yönü hesaplamak için kullanılacak yarıçapı belirtir. 3D Viewport üzerinde mouse'unuzun etrafındaki çember fırçanın yarıçapını belirtir, çemberin baktığı yön ise fırçanın normal'ını belirtir. Fırçanın normal'ı mouse'unuzun şu an üzerinde olduğu konumdan verilen yarıçap boyunca çevredeki diğer vertex'lerin ortalaması alınarak bulunur. Yani verilen yarıçap içerisindeki vertex'lerin normal'larının ortalaması alınır ve çıkan sonuç fırçanın normal'ı olarak kullanılır. İşte bu ayar da bu yarıçapı belirleyen ayardır. Eğer bu ayarın değerini 1 olarak ayarlarsanız fırçanın şu anki yarıçapı ne ise o yarıçap büyüklüğünde "Normal Radius" kullanılır. Eğer bu ayarı 0.5 olarak ayarlarsanız fırçanın şu anki yarıçapı ne ise o yarıçapın yarısı büyüklüğünde "Normal Radius" kullanılır. Yani "Normal Radius" değeri fırçanın yarıçapına da bağlıdır.



## [Draw Sharp](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/draw_sharp.html)
a

## [Clay](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/clay.html)
a

## [Clay Strips](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/clay_strips.html)
a

## [Clay Thumb](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/clay_thumb.html)
a

## [Layer](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/layer.html)
a

## [Inflate](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/inflate.html)
a

## [Blob](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/blob.html)
a

## [Crease](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/crease.html)
a

## [Smooth](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/smooth.html)
a

## [Flatten](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/flatten.html)
a

## [Fill](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/fill.html)
a

## [Scrape](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/scrape.html)
a

## [Multi-plane Scrape](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/multiplane_scrape.html)
a

## [Pinch](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/pinch.html)
a

## [Grab](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/grab.html)
a

## [Elastic Deform](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/elastic_deform.html)
a

## [Snake Hook](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/snake_hook.html)
a

## [Thumb](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/thumb.html)
a

## [Pose](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/pose.html)
a

## [Nudge](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/nudge.html)
a

## [Rotate](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/rotate.html)
a

## [Slide Relax](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/slide_relax.html)
a

## [Boundary](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/boundary.html)
a

## [Cloth](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/cloth.html)
a

## [Simplify](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/simplify.html)
a

## [Mask](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/mask.html)
a

## [Draw Face Sets](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/draw_facesets.html)
a

## [Multires Displacement Eraser](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/multires_displacement_eraser.html)
a

## [Multires Displacement Smear](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/multires_displacement_smear.html)
a

## [Paint](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/paint.html)
a

## [Smear](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/smear.html)
a

## [Box Mask](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/box_mask.html)
a

## [Lasso Mask](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/lasso_mask.html)
a

## [Line Mask](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/line_mask.html)
a

## [Box Hide]()
a

## [Box Face Set](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/box_face_set.html)
a

## [Lasso Face Set](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/lasso_face_set.html)
a

## [Box Trim](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/box_trim.html)
a

## [Lasso Trim](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/lasso_trim.html)
a

## [Line Project](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/line_project.html)
a

## [Mesh Filter](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/mesh_filter.html)
a

## [Cloth Filter](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/cloth_filter.html)
a

## [Color Filter](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/color_filter.html)
a

## [Edit Face Set](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/edit_face_set.html)
a

## [Mask by Color](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tools/mask_by_color.html)
a


<br>
<br>


# Brush Ayarları
Bu kategoride ek fırça ayarlarının (her fırçanın kendine özel ayarlarının haricindeki) açıklamaları vardır.

## [Advanced](https://docs.blender.org/manual/en/4.0/sculpt_paint/brush/brush_settings.html#advanced)
a

## [Texture](https://docs.blender.org/manual/en/4.0/sculpt_paint/brush/texture.html)
a

## [Stroke](https://docs.blender.org/manual/en/4.0/sculpt_paint/brush/stroke.html)
a

## [Falloff](https://docs.blender.org/manual/en/4.0/sculpt_paint/brush/falloff.html)
a

## [Cursor](https://docs.blender.org/manual/en/4.0/sculpt_paint/brush/cursor.html)
a


<br>
<br>


# Workflowlar

## [Dynamic Topology (Dyntopo)](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tool_settings/dyntopo.html)

## [Voxel Remesh](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/tool_settings/remesh.html)

## [Multiresolution](https://docs.blender.org/manual/en/4.0/sculpt_paint/sculpting/introduction/adaptive.html#multiresolution)


<br>
<br>


# Kısayollar

<details>
<summary>Genel Kısayollar</summary>
<br>

Kısayol | Açıklama
:---: | :---:
F | Fırçanın yarıçapını ayarlayabilirsiniz (sol ve sağa hareket ettirerek). Ayarlarken sol üstten şu anki radius değerini görebilirsiniz. Fırça yarıçapını ayarlarken "Ctrl" kısayoluna tıklayarak radius değerini 10'un katı olan sayılarda ayarlayabilirsiniz, "Shift" kısayoluna tıklayarak da ince ayar yapabilirsiniz.
Shift + F | Fırçanın şiddetini ayarlayabilirsiniz (sol ve sağa hareket ettirerek). Fırça şiddetini ayarlarken "Ctrl" kısayoluna tıklayarak şiddet değerini 100'ün katı olan sayılarda ayarlayabilirsiniz, "Shift" kısayoluna tıklayarak da ince ayar yapabilirsiniz.
Ctrl + Sol tık | "Ctrl" kısayoluna basarken mouse'un sol tuşuna basıp çizim yaparsanız fırçanın yönünü değiştirmiş olursunuz, yani "Direction" ayarını terse almış olursunuz. Bazı özel fırçalarda "Ctrl" kısayoluna basılı tutarak tıklamak yön değiştirmeyi değil de fırçanın 2. özelliğini aktifleştirmede kullanılır. Yani "Ctrl" kısayoluna basılı tutarak tıklamak her fırçada yön değiştirmek için kullanılmaz, fırçanın 2. özelliğini kullanmak için de kullanılır.

</details>


<details>
<summary>Brush Kısayolları</summary>
<br>

Bu kısayolları tek tek anlatmama gerek yok. "Shift + Boşluk" kısayolunu kullandığınızda brush'ların kısayollarının da yanında yazdığı bir seçim menüsü çıkar. Bu menüden bütün brush kısayollarını ögrenebilirsiniz. Bütün brush'ların kısayollarını bilmenize gerek yok, eğer brush'ın kısayolunun içerisinde herhangi bir harf varsa o kısayolu ögrenin, yani içerisinde harf geçen kısayola sahip olan brush'lar ana brush'lardır. Bunun haricinde sculpting ile çok vakit geçiriyorsanız sürekli "Shift + Boşluk" kısayolundaki seçim menüsünü kullanarak zamanla kullandığınız brush'ların kısayollarını ezberleyebilirsiniz.

</details>
















