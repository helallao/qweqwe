Aşağıdaki döküman Cycles render motoru kullanıldığı varsayılarak hazırlanmıştır. Cycles için render ayarlarının açıklamaları (Properties > Render) vardır. Eğer farklı bir render motoru kullanıyorsanız birçok özellik farklılık gösterecek veya çalışmayacaktır.

# Ek Bilgiler

<details>
<summary>Güzel Kaynaklar</summary>
<br>

* [The Blender 2.8 Encyclopedia](https://www.udemy.com/course/the-blender-encyclopedia/) - Udemy'deki sayısı bir elin parmaklarını geçmeyecek kadar az olan, gerçekten uğraşılmış kurslardan birisi. Bizim için önemli olan 17. bölüm "Render (Cycles)", render ayarlarının açıklamalarının olduğu bölüm, tabi isterseniz diğer kısımlara da bakabilirsiniz. [Buradan](https://btdig.com/search?q=The+Blender+2.8+Encyclopedia) torrent'ini bulabilirsiniz (vpn gerekebilir).
* [The Cycles Encyclopedia](https://www.blenderdiplom.com/en/shop/576-the-cycles-encyclopedia.html) - Cycles üzerine shaderlar ve render ayarları hakkında en kapsamlı kaynaklardan birisi. Bizim için önemli olan kısım 237. sayfadan sonrası, tabi isterseniz kalan kısımlara da bakabilirsiniz. [Buradan](https://annas-archive.org/md5/070b8cc769760f1cd49350c046940a3e) pdf'ini indirebilirsiniz.

</details>



# [General](#general-1)
* [Render Engine](#render-engine)
* [Feature Set](#feature-set)
* [Device](#device)
* [Open Shading Language](#open-shading-language)

# [Sampling](#sampling-1)
* [Noise Threshold (Viewport)](#noise-threshold)
* [Max Samples (Viewport)](#max-samples)
* [Min Samples (Viewport)](#min-samples)
* [Denoise (Viewport)](#denoise)
* [Denoiser (Viewport)](#denoiser)
* [Passes (Viewport)](#passes)
* [Start Sample (Viewport)](#start-sample)
* [Noise Threshold (Render)](#noise-threshold-1)
* [Max Samples (Render)](#max-samples-1)
* [Min Samples (Render)](#min-samples-1)
* [Time Limit (Render)](#time-limit)
* [Denoise (Render)](#denoise-1)
* [Denoiser (Render)](#denoiser-1)
* [Passes (Render)](#passes-1)
* [Prefilter (Render)](#prefilter)
* [Light Tree (Lights)](#light-tree)
* [Light Threshold (Lights)](#light-threshold)


<br>
<br>


# [General]()
Bu kategori render ayarlarına başlamadan önce, render motorunu ve özelliklerini seçtiğimiz kısımdır.


* #### Render Engine
Buradan kullanacağınız render motorunu seçebilirsiniz.

* #### Feature Set
Sadece "Render Engine" ayarı "Cycles" iken vardır. "Experimental" ayarını seçerek deneysel özellikleri kullanabilirsiniz.

* #### Device
Sadece "Render Engine" ayarı "Cycles" iken vardır. Render işleminin cpu (işlemci) üzerinde mi yoksa gpu (ekran kartı) üzerinde yapılacağını seçebilirsiniz. Gpu (ekran kartı) seçeneğini kullanmadan önce ayarlara girip (Preferences) "System" menüsünde en üst bölümden gpu için kullanmak istediğimiz cihazı seçmeliyiz.

* #### Open Shading Language
Sadece "Render Engine" ayarı "Cycles" iken vardır. Shader'larda Open Shading Language'in kullanımını açar/kapatır. Bu ayarın kullanılabilmesi için "Device" ayarı cpu olmalıdır.


<br>
<br>


# [Sampling](https://docs.blender.org/manual/en/3.6/render/cycles/render_settings/sampling.html)
Bu kategoride genel olarak sampling işlemi ile ilgili ayarlar yani ışık ışınları ile ilgili ayarlar vardır.


## Viewport

* #### Noise Threshold
Bu ayar eskiden yoktu, blender 3.0 güncellemesi ile Cycles render motoru "Cycles X" olarak güncellendi ve bu ayar da yeni özelliklerden biri. Eskiden verdiğiniz samples sayısı kadar sample hesaplanıyordu ama artık piksellerin noise (gürültü) derecesine göre kalitesini belirleyebiliyor ve yeterince kaliteliyse sample sayısını da azaltabiliyoruz. İlk baş sample işleminin ne olduğunu anlamanız gerek, Cycles sahneyi render ederken her bir piksel için sample sayısı kadar kameradan sahneye ışık ışını (ray) yollar. Sonra bu ışık ışınları çarptığı yüzeylerden rastgele (tamamen rastgele değil, ışık ışının sekebileceği yerlerin listesi var ve bu listeden rastgele seçim yapılıyor) etrafa saçılır. Bu ışık ışınlarının bazıları ışık kaynağına ulaşır, bazıları ulaşamaz. Bu şekilde her bir piksel için o yerin/yüzeyin rengi belirlenir. Sample sayısı da her bir piksel için toplamda yollanacak ışık ışını sayısıdır. Sample sayısı arttıkça daha fazla tekrarlama olacağı için elimize o pikselin alabileceği renk hakkında (yani çevre/ortam hakkında) daha fazla bilgi geçer. Sonra da bütün sample'lardan alınan değerlerin ortalamasına göre o piksele renk verilir. Eğer samples sayısını düşük tutarsanız bazı piksellerin farklı farklı renklere sahip olduğunu yani noise (gürültü) olduğunu görebilirsiniz. Bu durumda samples sayısını arttırırız ve noise azalır.

Şimdi gelelim "Noise Threshold" ayarına, "Noise Threshold" ayarı bu durumlar için geliştirilmiş yeni bir özellik. "Noise Threshold" ayarı her bir piksel (veya daha fazla pikseli birden hesaplıyor da olabilir, bilmiyorum) için noise derecesini hesaplar ve verdiğimiz limit (threshold) değerine gelene kadar sample sayısını arttırmaya devam eder. Yani sample sayısı noise derecesine göre artar/azalır. Bu da bize noise'in az olduğu yerler için daha az sample alma imkanı sunar, böylelikle de render süresi kısalır. Bu sample sayısını otomatik ayarlama işlemine "Adaptive Sampling" deniyor. Tabi sample sayısı otomatik belirlenecek olsa bile yine de minimum ve maximum sample sayısı limitlerini ayarlayabilirsiniz (Min Samples, Max Samples).

Gelelim şimdi bu input'a verdiğiniz değerin çalışma şekline, "Noise Threshold" değeri aslında render'da her bir piksel için ne kadar noise olabileceğini yani ne kadar noise'e tahammül edilebileceğini temsil ediyor. Yani anladığınız üzere bu değer yükseldikçe render'da noise daha fazla (dolayısıyla samples daha az) olacak, değer azaldıkça da noise daha az (dolayısıyla samples daha fazla) olacak. Eğer isterseniz bu ayarı kapatabilirsiniz, ayarı kapattığınızda eskiden olduğu gibi tek bir "Samples" input'u olacak ve samples sayısını manuel olarak belirleyebileceksiniz. Ayrıca bu ayarların Viewport için olduğunu unutmayın, eğer render için bu ayarları yapmak istiyorsanız [Render](#render) kategorisine bakın.

* #### Max Samples
Sadece "Noise Threshold" ayarı açıkken vardır. Maximum sample sayısını temsil eder. Eğer render alınırken sample sayısı bu sayıya ulaşırsa, noise seviyesi yeteri kadar düşürülmemiş olsa bile o piksel için daha fazla sample alınmaz. Yani bu değer "Adaptive Sampling" için maximum sample sayısını temsil eder.

* #### Min Samples
Sadece "Noise Threshold" ayarı açıkken vardır. Minimum sample sayısını temsil eder. Eğer render alınırken noise seviyesi yeteri kadar düşürülmüş olsa bile, sample sayısı bu sayıya ulaşmadıysa o piksel için bu sayıya ulaşana kadar sample alınmaya devam eder. Yani bu değer "Adaptive Sampling" için minimum sample sayısını temsil eder. Ayrıca eğer render alınırken noise seviyesi yeteri kadar düşürülene kadar sample alınmasını istiyorsanız bu ayarı 0 yapabilirsiniz (tabi hala "Max Samples" değerini geçemez), 0 yaptığınızda Cycles sizin için otomatikmen bu değeri belirler.

* #### Denoise
Denoise ayarlarını açar. Denoise viewport üzerinde çıkan noise'ı (gürültü) silmeye yarayan çok etkili bir araçtır.

* #### Denoiser
Buradan denoise işlemini gerçekleştiren farklı modlar seçebilirsiniz.

* #### Passes
Buradan denoise işleminde kullanılacak bilgileri seçebilirsiniz, Albedo + Normal en detaylısıdır.

* #### Start Sample
Buradan denoise işleminin kaçıncı sample'dan sonra başlayacağınız belirleyebilirsiniz.


## Render

* #### Noise Threshold
Bu ayar eskiden yoktu, blender 3.0 güncellemesi ile Cycles render motoru "Cycles X" olarak güncellendi ve bu ayar da yeni özelliklerden biri. Eskiden verdiğiniz samples sayısı kadar sample hesaplanıyordu ama artık piksellerin noise (gürültü) derecesine göre kalitesini belirleyebiliyor ve yeterince kaliteliyse sample sayısını da azaltabiliyoruz. İlk baş sample işleminin ne olduğunu anlamanız gerek, Cycles sahneyi render ederken her bir piksel için sample sayısı kadar kameradan sahneye ışık ışını (ray) yollar. Sonra bu ışık ışınları çarptığı yüzeylerden rastgele (tamamen rastgele değil, ışık ışının sekebileceği yerlerin listesi var ve bu listeden rastgele seçim yapılıyor) etrafa saçılır. Bu ışık ışınlarının bazıları ışık kaynağına ulaşır, bazıları ulaşamaz. Bu şekilde her bir piksel için o yerin/yüzeyin rengi belirlenir. Sample sayısı da her bir piksel için toplamda yollanacak ışık ışını sayısıdır. Sample sayısı arttıkça daha fazla tekrarlama olacağı için elimize o pikselin alabileceği renk hakkında (yani çevre/ortam hakkında) daha fazla bilgi geçer. Sonra da bütün sample'lardan alınan değerlerin ortalamasına göre o piksele renk verilir. Eğer samples sayısını düşük tutarsanız bazı piksellerin farklı farklı renklere sahip olduğunu yani noise (gürültü) olduğunu görebilirsiniz. Bu durumda samples sayısını arttırırız ve noise azalır.

Şimdi gelelim "Noise Threshold" ayarına, "Noise Threshold" ayarı bu durumlar için geliştirilmiş yeni bir özellik. "Noise Threshold" ayarı her bir piksel (veya daha fazla pikseli birden hesaplıyor da olabilir, bilmiyorum) için noise derecesini hesaplar ve verdiğimiz limit (threshold) değerine gelene kadar sample sayısını arttırmaya devam eder. Yani sample sayısı noise derecesine göre artar/azalır. Bu da bize noise'in az olduğu yerler için daha az sample alma imkanı sunar, böylelikle de render süresi kısalır. Bu sample sayısını otomatik ayarlama işlemine "Adaptive Sampling" deniyor. Tabi sample sayısı otomatik belirlenecek olsa bile yine de minimum ve maximum sample sayısı limitlerini ayarlayabilirsiniz (Min Samples, Max Samples).

Gelelim şimdi bu input'a verdiğiniz değerin çalışma şekline, "Noise Threshold" değeri aslında render'da her bir piksel için ne kadar noise olabileceğini yani ne kadar noise'e tahammül edilebileceğini temsil ediyor. Yani anladığınız üzere bu değer yükseldikçe render'da noise daha fazla (dolayısıyla samples daha az) olacak, değer azaldıkça da noise daha az (dolayısıyla samples daha fazla) olacak. Eğer isterseniz bu ayarı kapatabilirsiniz, ayarı kapattığınızda eskiden olduğu gibi tek bir "Samples" input'u olacak ve samples sayısını manuel olarak belirleyebileceksiniz. Ayrıca bu ayarların render için olduğunu unutmayın, eğer Viewport için bu ayarları yapmak istiyorsanız [Viewport](#viewport) kategorisine bakın.

* #### Max Samples
Sadece "Noise Threshold" ayarı açıkken vardır. Maximum sample sayısını temsil eder. Eğer render alınırken sample sayısı bu sayıya ulaşırsa, noise seviyesi yeteri kadar düşürülmemiş olsa bile o piksel için daha fazla sample alınmaz. Yani bu değer "Adaptive Sampling" için maximum sample sayısını temsil eder.

* #### Min Samples
Sadece "Noise Threshold" ayarı açıkken vardır. Minimum sample sayısını temsil eder. Eğer render alınırken noise seviyesi yeteri kadar düşürülmüş olsa bile, sample sayısı bu sayıya ulaşmadıysa o piksel için bu sayıya ulaşana kadar sample alınmaya devam eder. Yani bu değer "Adaptive Sampling" için minimum sample sayısını temsil eder. Ayrıca eğer render alınırken noise seviyesi yeteri kadar düşürülene kadar sample alınmasını istiyorsanız bu ayarı 0 yapabilirsiniz (tabi hala "Max Samples" değerini geçemez), 0 yaptığınızda Cycles sizin için otomatikmen bu değeri belirler.

* #### Time Limit
Render süresi limiti. Eğer render süresi bu limiti geçerse render işlemi bitirilir. Ayrıca süre ile ilgili 2-3 saniye kaymalar olabilir çünkü bu ayar render işlemi başlamadan önceki hazırlık kısmında geçen süreyi saymaz.

* #### Denoise
Denoise ayarlarını açar. Denoise render üzerinde çıkan noise'ı (gürültü) silmeye yarayan çok etkili bir araçtır.

* #### Denoiser
Buradan denoise işlemini gerçekleştiren farklı modlar seçebilirsiniz.

* #### Passes
Buradan denoise işleminde kullanılacak bilgileri seçebilirsiniz, Albedo + Normal en detaylısıdır.

* #### Prefilter
Denoise işleminden önce "Passes" input'unda seçilen bilgilere filtreleme uygular. Kaliteyi etkiler, Accurate en detaylısıdır.


## Lights

* #### Light Tree
Light Tree ışıkların şiddetini/uzaklığı falan hesaplayıp, ışıkların renderda daha kaliteli görünmesini sağlar ve noise'i azaltır. Özellikle sahnenizde çok fazla ışık kaynağı varsa bu özelliğin çok büyük etkisi olduğunu görebilirsiniz. Sahnenizde az ışık kaynağı olsa bile bence bu ayarı kapatmayın, ama tabi isterseniz kapatabilirsiniz de, test edip etkisini kendiniz görün. Bu ayarın açık olması render işlemini biraz daha uzatır. Bu ayarı kapattığınızda otomatikmen "Light Threshold" ayarı aktifleşir. "Light Threshold" ayarı ile manuel olarak hesaplama yapılması gereken minimum ışık şiddetini belirtebilirsiniz.

* #### Light Threshold
"Light Threshold" ayarı kapatıldığında bu ayar aktifleşir. Bu ayar minimum ne kadar ışık şiddeti için hesaplama yapılması gerektiğini verir. Mesela çok düşük şiddetli veya çok uzakta olan ve etkisi çok az olan ışıkları hesaplama işlemlerine katmak istemiyorsanız bu ayarı biraz arttırabilirsiniz. Ya da minimum derecede etki eden ışıkları bile hesaplamak istiyorsanız bu ayarı düşürebilirsiniz. 0 yaparak bütün ışıkların hesaplanmasını sağlayabilirsiniz ama render süresi de uzar. Yani anladığınız üzere bu ayar ışık etkisinin hesaba katılabilmesi için minimum ne kadar olması gerektiğini belirtiyor, bu derecenin altında olan ışıklar da hesaplanmıyor.


## Advanced

* #### Seed
a

<video src='../Dosyalar/Render_Sampling_Seed.mp4' width=180/>







































































