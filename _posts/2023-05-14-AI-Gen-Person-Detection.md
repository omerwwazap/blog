---
layout: post
title: Yapay Zekâ Tarafından Oluşturulan Sahte Kişiler Nasıl Tanınır?
date: 2023-05-14 12:00 +0200
categories: [OSINT, AI]
tags: [Turkish]     # TAG names should always be lowercase
---

# Yapay Zekâ Tarafından Oluşturulan Sahte Kişiler Nasıl Tanınır?[^1]

> ==Güncel konular için kontrol edilmeli - To Do==

*2000'li yıllarda üzerinde çalışılmaya başlanılan ve hayatımıza ilk kez Matrix, Terminator ve Tron filmleri ile girmiş olan Sentetik Yüz Oluşturma teknolojisi 2014'te Ian Goodfellow’un GAN (generative adversarial network) teknolojisi ile çok farklı boyutlara ulaşmıştır. Ancak 2018'e kadar gündelik hayatımıza girmemiştir.*

GAN nedir diye sorarsanız çok basit bir şekilde, İki adet öğrenebilen yapay zekâ olduğunu düşünün. Bunlardan bir tanesi bir referanstan (komut/resim) yola çıkarak yapay bir resim oluşturuyor\. Diğer yapay zekâ da bu resmin gerçek olup olmadığını tahmin etmeye çalışıyor\. Bu şekilde resmi oluşturan yapay zekâ tahmin edilememek için gelişiyor ve diğer yapay zekâda resimleri daha doğru tahmin edebilmek için gelişiyor\. İlk basit örneklere bakacak olursak,

| [PLACE HOLDER FOR IMAGE - 1 ] |
|:--:|
| *2014 DCGAN Algoritması ile oluşturulmuş Sahte İnsan Yüzleri* |

Görüldüğü 2014'te yapılan çalışmalar zamanına göre çok ilgi çekici olsa da, kolayca sahte olduklarını anlayabilirsiniz. Ancak 2018'de NVIDIA’nın duyurmuş olduğu ve hâlâ geliştirmekte olan StyleGAN adı verilen GAN, yukarıdaki resimleri çok farklı bir boyuta getirmiştir.

| [PLACE HOLDER FOR IMAGE - 2 ] |
|:--:|
| *2018 NVIDIA StyleGAN version 1 (2022 itibari ile StyleGAN3 çıkmıştır)* |

Görüldüğü gibi gerçek mi sahte mi olduğunu anlamak çok zor bir hâlâ gelmiştir. Bunu fark edenler, yapay insan yüzleri ile Sosyal Medya hesapları açmaya başlamış ve dolandırıcılık gibi kötü amaçlı işler için kullanmaktadırlar. Neyse ki şu an itibariyle bu teknoloji mükemmelleştirilmiş değildir.

StyleGAN şu an en gelişmiş yapay yüz oluşturma metholdarında birisi olarak kabul edilse de. Oluşturulan resimlerin sahte olduğu anlamamın birkaç yolu vardır.

### Arka Plan
>
> ==Güncel konular için kontrol edilmeli==

Yüz eğitmek için oluşturulan GAN’lar resimlerin arka planlarını oluşturmakta pekiyi değildir. Araka planda okunması zor yazılar, surreal görüntüler ve fiziksel olarak imkânsız manzaralar görebilirsiniz. Bunun nedeni GAN’ı oluştururken kullanılan resimlerin genelde sadece insan kafasının ortalanmış ve kesilmiş(crop) resimler ile oluşturulmasındandır. Bu sebep ile arka plandan bir bilgi öğrenmesi oldukça zordur

> Aşağıdaki örnekler [thispersondoesnotexist](https://thispersondoesnotexist.com/) sitesinde oluşturulmuştur.

| [PLACE HOLDER FOR IMAGE - 3-4-5-6 ] |
|:--:|
| *Arka planlarda gariplikler* |

### Garip Dişler
>
> ==Güncel konular için kontrol edilmeli==

Dişlerin işlenmesi pek kolay değildir. Genellikle dişler tuhaf renkli, anormal şekilli veya asimetriktir. Bazı durumlarda, aşağıdaki gibi üç azı dişi bile görebilirsiniz.

| [PLACE HOLDER FOR IMAGE - 7-8-9 ] |
|:--:|
| *Resimlerin üzerinde tıklayarak dişlerdeki problemleri görebilirsiniz* |

### Saçların Görünüşü — Yeni uyanmış gibi saçlar
>
> ==Güncel konular için kontrol edilmeli==

Saçın gerçekçi bir şekilde işlenmesi büyük bir problem gibi gözüküyor. Bazen yüzlerde veya başka bir yerde bağlantısız saç telleri görebilrisiniz. Diğer zamanlarda ssaçın etrafında garip bir parıltı veya fon olabilir. Çok nadiren de sanki Paint ile photoshop’lanmış saç uçları da bulabilirsiniz.

| [PLACE HOLDER FOR IMAGE - 10-11-12-13 ] |
|:--:|
| *Kırmızı ile işaretlenmiştir.* |

### Renk Kanaması
>
> ==Güncel konular için kontrol edilmeli==

Bazı resimlerde ufak renk bozuklukları olduğunu görebilirsiniz.

| [PLACE HOLDER FOR IMAGE - 13-14-15-16 ] |
|:--:|
| *Tüm resimlerde, kıyafetlerin yakasına dikkatli bakmalısınız.* |

### Kayıp Küpeler — Asimetri
>
> ==Güncel konular için kontrol edilmeli==

GAN’ı oluştururken kullanılan resimlerin bazılarında küpe olması ve bazılarında olmaması, oluşturulan yapay yüzlerde sorunlar yatabiliyor. Ancak bu sorunlar son GAN versiyonlarında büyük oranda çözülmüştür.

| [PLACE HOLDER FOR IMAGE - 17-18 ] |
|:--:|
| *Sol resimde küpe kulak ile birleşmiş ve Sağ resimde bir küpe eksik.* |

### Water Splotches[^2]
>
> ==Güncel konular için kontrol edilmeli==

Bu şekilde olan resimleri birisi profil fotoğrafı olarak kullanmaz ancak görmeniz durumunda yapay yüz yaratma algoritması ile yapıldığını anlayabilirsiniz.

| [PLACE HOLDER FOR IMAGE - 19-20 ] |
|:--:|
| *Genellikle Küpelerin olduğu yerde görülse de yukarıdaki örnekleri gibi farklı yerlerde de karşınıza çıkabilir.* |

### Gözlükler — Asimetri
>
> ==Güncel konular için kontrol edilmeli==

Şu anda, algoritmalar gerçekçi görünümlü gözlükler oluşturmayı pek beceremiyor. Genel bir simetri sorunu yaşıyorlar. Oluşturulan çerçevelerde genellikle sağ tarafında ve sol tarafında fiziksel farklılıklar oluyor.

| [PLACE HOLDER FOR IMAGE - 21-22-23 ] |
|:--:|
| *Gözlüklerin çerçevelerinde deformasyonlar vardır ve tam simetrik değildir. Ayrıca ilk resimde gözlük camları eksiktir.* |

### Simetri Problemleri — Asimetri
>
> ==Güncel konular için kontrol edilmeli==

Genel olarak simetri, yüz oluşturma algoritmaları için şu an büyük bir problem oluşturuyor gibi gözüküyor. Gözlüklerine ek olarak sakalların asimetrik olması, sağ ve sol küpelerdeki deformasyon ve giyilen kıyafetteki tutarsızlıklar yapay yüzleri bulmamızda kolaylık sağlıyor.

| [PLACE HOLDER FOR IMAGE - 24-25 ] |
|:--:|
| *Sol resimde göz ve kaşlarda simetrik değildir. Sağ resimde ise kulakların birinde deformasyon vardır.* |

### ve En Önemlisi
>
> ==Güncel konular için kontrol edilmeli==

GAN, şu an aynı yapay resmin bir başka versiyonunu oluşturamıyor, yani kişinin farklı bir açıdan görüntüsünü yaratamıyorlar. Eğer sosyal medyadan birisi ile tanıştıysanız sadece bir resmi var ise ve yapay olduğunda şüpheleniyorsanız başka bir resmin isteyin. Veremezler ise durum sıkıntılı demektir.

Tabii belirtmekte fayda [Wombo.ai](https://www.w.ai/) gibi bir resim üzerinden insanların yüzünü video olarak oynatan ya da Deepfake gibi teknolojiler sayesinde tek bir resim üzerinden gerçekci videolarda yaratılabilir. Su an için tek teselliniz Deepfake yaratmanın, StyleGAN ile resim yaratmaya göre daha zor olmasıdır.

> Öğrendiklerinizi denemek isterseniz. Gerçek mi sahte mi adlı oyuna bakabilirsiniz. [Which Face Is Real?](https://www.whichfaceisreal.com/learn.html)

Daha farklı teknikler ve StyleGAN ile başka ne tür şeyler yapay olarak yapılabilir bakmak isterseniz, güzel bir liste hazırladım,

- Yapay Kedi Resimleri — [thiscatdoesnotexist.com](https://thiscatdoesnotexist.com/)
- Yapay Oda Resimleri — [Cozy apartment in coole — Guest suites for Rent](https://thisrentaldoesnotexist.com/)
- Yapay Stackoverflow soruları — [Stack Roboflow: This Question Does Not Exist](https://stackroboflow.com/)
- Yapay Araba Resimleri — [This Automobile / Car / Vehicle Does Not Exist](https://www.thisautomobiledoesnotexist.com/)
- Yapay Şehir/Uydu Görüntüleri — [This City Does Not Exist](https://thiscitydoesnotexist.com/)
- Yapay Sahiller — [This beach does not exist](https://thisbeachdoesnotexist.com/)
- Gerçek insanların yüzlerinden sahte insan resmi üretimi - [Generate look-a-like photos to protect your identity](https://generated.photos/anonymizer)
- Kriterlere göre insan resmi seçmenizi sağlayan bir site — [Gallery of AI Generated Faces](https://generated.photos/faces)
- ve daha farklı konular için — [This X Does Not Exist](https://thisxdoesnotexist.com/)
- ==PLACE HOLDER FOR NEW STUFF==

## Kaynak

[^1]: First published here [Levent's Medium](https://medium.com/@leventd/yapay-zeka-taraf%C4%B1ndan-olu%C5%9Fturulan-sahte-ki%C5%9Filer-nas%C4%B1l-tan%C4%B1n%C4%B1r-eeac3aa1dde1).
[^2]: Is not seen anymore with more advanced GAN applications.
