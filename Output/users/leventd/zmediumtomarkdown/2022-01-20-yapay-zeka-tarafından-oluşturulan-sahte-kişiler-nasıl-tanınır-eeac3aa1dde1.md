---
title: "Yapay zeka tarafından oluşturulan sahte Kişiler nasıl tanınır?"
author: "Levent Durdalı"
date: 2022-01-20T15:44:48.537+0000
last_modified_at: 2022-01-24T10:39:18.375+0000
categories: ""
tags: ["sytlegan","yapay-zeka","nvidia","sosyal-medya","türkçe"]
description: "Hayatımıza ilk kez Matrix, Terminator, Hızlı ve Öfkeli ve Tron filmleri ile girmiş olan Sentetik Yüz Oluşturma teknolojisi…"
image:
  path: /assets/eeac3aa1dde1/1*jPG0ScHUAapfYBzgrZJAoA.png
---

### **Yapay** Zekâ **Tarafından Oluşturulan Sahte Kişiler Nasıl Tanınır?**
#### 2000'li yıllarda üzerinde çalışılmaya başlanılan ve hayatımıza ilk kez Matrix, Terminator ve Tron filmleri ile girmiş olan Sentetik Yüz Oluşturma teknolojisi 2014'te Ian Goodfellow’un GAN \(generative adversarial network\) teknolojisi ile çok farklı boyutlara ulaşmıştır\. Ancak 2018'e kadar gündelik hayatımıza girmemiştir\.

GAN nedir diye sorarsanız çok basit bir şekilde, İki adet öğrenebilen yapay zekâ olduğunu düşünün\. Bunlardan bir tanesi bir referanstan \(komut/resim\) yola çıkarak yapay bir resim oluşturuyor\. Diğer yapay zekâ da bu resmin gerçek olup olmadığını tahmin etmeye çalışıyor\. Bu şekilde resmi oluşturan yapay zekâ tahmin edilememek için gelişiyor ve diğer yapay zekâda resimleri daha doğru tahmin edebilmek için gelişiyor\. İlk basit örneklere bakacak olursak,


![2014 DCGAN Algoritması ile oluşturulmuş Sahte İnsan Yüzleri](assets/eeac3aa1dde1/1*-euXlaJoTs8IiPiPtDoUoA.png)

2014 DCGAN Algoritması ile oluşturulmuş Sahte İnsan Yüzleri

Görüldüğü 2014'te yapılan çalışmalar zamanına göre çok ilgi çekici olsa da, kolayca sahte olduklarını anlayabilirsiniz\. Ancak 2018'de NVIDIA’nın duyurmuş olduğu ve hâlâ geliştirmekte olan StyleGAN adı verilen GAN, yukarıdaki resimleri çok farklı bir boyuta getirmiştir\.


![2018 NVIDIA StyleGAN version 1 \(2022 itibari ile StyleGAN3 çıkmıştır\)](assets/eeac3aa1dde1/1*jPG0ScHUAapfYBzgrZJAoA.png)

2018 NVIDIA StyleGAN version 1 \(2022 itibari ile StyleGAN3 çıkmıştır\)

Görüldüğü gibi gerçek mi sahte mi olduğunu anlamak çok zor bir hâlâ gelmiştir\. Bunu fark edenler, yapay insan yüzleri ile Sosyal Medya hesapları açmaya başlamış ve dolandırıcılık gibi kötü amaçlı işler için kullanmaktadırlar\. Neyse ki şu an itibariyle bu teknoloji mükemmelleştirilmiş değildir\.

StyleGAN şu an en gelişmiş yapay yüz oluşturma metholdarında birisi olarak kabul edilse de\. Oluşturulan resimlerin sahte olduğu anlamamın birkaç yolu vardır\.


> Aşağıdaki örnekler [thispersondoesnotexist](https://thispersondoesnotexist.com/) sitesinde oluşturulmuştur\. 




### **Arka Plan**

Yüz eğitmek için oluşturulan GAN’lar resimlerin arka planlarını oluşturmakta pekiyi değildir\. Araka planda okunması zor yazılar, surreal görüntüler ve fiziksel olarak imkânsız manzaralar görebilirsiniz\. Bunun nedeni GAN’ı oluştururken kullanılan resimlerin genelde sadece insan kafasının ortalanmış ve kesilmiş\(crop\) resimler ile oluşturulmasındandır\. Bu sebep ile arka plandan bir bilgi öğrenmesi oldukça zordur\.


![](assets/eeac3aa1dde1/1*0shYnaK0FhkpVopiOENBVw.jpeg)



![](assets/eeac3aa1dde1/1*wbUAdjDstoU0uJb9Pl0_xA.jpeg)



![](assets/eeac3aa1dde1/1*lXEzsIe-LvDhI5UAwPN5Hw.jpeg)



![Arka planlarda gariplikler](assets/eeac3aa1dde1/1*GMbnt19pFVENBV3jFHoaIg.jpeg)

Arka planlarda gariplikler
### **Garip Dişler**

Dişlerin işlenmesi pek kolay değildir\. Genellikle dişler tuhaf renkli, anormal şekilli veya asimetriktir\. Bazı durumlarda, aşağıdaki gibi üç azı dişi bile görebilirsiniz\.


![](assets/eeac3aa1dde1/1*-BAuQnY4LvC_WEz3ZphmAg.jpeg)



![](assets/eeac3aa1dde1/1*KsSidfYnIEhsgrdWJedFTg.jpeg)



![Resimlerin üzerinde tıklayarak dişlerdeki problemleri görebilirsiniz](assets/eeac3aa1dde1/1*d0fwGw43LE1dGcjw8GIuYA.jpeg)

Resimlerin üzerinde tıklayarak dişlerdeki problemleri görebilirsiniz
### **Saçların Görünüşü — Yeni uyanmış gibi saçlar**

Saçın gerçekçi bir şekilde işlenmesi büyük bir problem gibi gözüküyor\. Bazen yüzlerde veya başka bir yerde bağlantısız saç telleri görebilrisiniz\. Diğer zamanlarda ssaçın etrafında garip bir parıltı veya fon olabilir\. Çok nadiren de sanki Paint ile photoshop’lanmış saç uçları da bulabilirsiniz\.


![](assets/eeac3aa1dde1/1*Ppi8mLksv47wpiSHanxg_g.jpeg)



![](assets/eeac3aa1dde1/1*hN_cxJPPFoYlyWlg-ACKgw.jpeg)



![](assets/eeac3aa1dde1/1*HDCHn059ZGeccbqmPpHniw.jpeg)



![Kırmızı ile işaretlenmiştir\.](assets/eeac3aa1dde1/1*5tElVD7vMqkGNZmg89BcpQ.jpeg)

Kırmızı ile işaretlenmiştir\.
### **Renk Kanaması**

Bazı resimlerde ufak renk bozuklukları olduğunu görebilirsiniz\.


![](assets/eeac3aa1dde1/1*79q6AMs17fvr2GvRQxJi8w.jpeg)



![](assets/eeac3aa1dde1/1*W__Xn7Wc8l7nMdVFbWsK4w.jpeg)



![](assets/eeac3aa1dde1/1*ckVis_Fo_uFltkueLxcb8w.jpeg)



![Tüm resimlerde, kıyafetlerin yakasına dikkatli bakmalısınız\.](assets/eeac3aa1dde1/1*80fFlAAijVs2kUEcg7xZrA.jpeg)

Tüm resimlerde, kıyafetlerin yakasına dikkatli bakmalısınız\.
### **Kayıp Küpeler — Asimetri**

GAN’ı oluştururken kullanılan resimlerin bazılarında küpe olması ve bazılarında olmaması, oluşturulan yapay yüzlerde sorunlar yatabiliyor\. Ancak bu sorunlar son GAN versiyonlarında büyük oranda çözülmüştür\.


![](assets/eeac3aa1dde1/1*myuesGkcvcz6oCDB6rxaLQ.jpeg)



![Sol resimde küpe kulak ile birleşmiş ve Sağ resimde bir küpe eksik\.](assets/eeac3aa1dde1/1*jlHS5K1wS6Z5PmD5VjOlPw.jpeg)

Sol resimde küpe kulak ile birleşmiş ve Sağ resimde bir küpe eksik\.
### **Water Splotches**

Bu şekilde olan resimleri birisi profil fotoğrafı olarak kullanmaz ancak görmeniz durumunda yapay yüz yaratma algoritması ile yapıldığını anlayabilirsiniz\.


![](assets/eeac3aa1dde1/1*CWJ6CGnjAUvdph2i0uGJWQ.jpeg)



![Genellikle Küpelerin olduğu yerde görülse de yukarıdaki örnekleri gibi farklı yerlerde de karşınıza çıkabilir\.](assets/eeac3aa1dde1/1*XY9yumN8IES7ATy9dLLFZA.jpeg)

Genellikle Küpelerin olduğu yerde görülse de yukarıdaki örnekleri gibi farklı yerlerde de karşınıza çıkabilir\.
### **Gözlükler — Asimetri**

Şu anda, algoritmalar gerçekçi görünümlü gözlükler oluşturmayı pek beceremiyor\. Genel bir simetri sorunu yaşıyorlar\. Oluşturulan çerçevelerde genellikle sağ tarafında ve sol tarafında fiziksel farklılıklar oluyor\.


![](assets/eeac3aa1dde1/1*bxEuY0jHAF4E24Fe3q6WYw.jpeg)



![](assets/eeac3aa1dde1/1*jlHS5K1wS6Z5PmD5VjOlPw.jpeg)



![Gözlüklerin çerçevelerinde deformasyonlar vardır ve tam simetrik değildir\. Ayrıca ilk resimde gözlük camları eksiktir\.](assets/eeac3aa1dde1/1*hNiRDFYt-QXKb1TlRtA0tw.jpeg)

Gözlüklerin çerçevelerinde deformasyonlar vardır ve tam simetrik değildir\. Ayrıca ilk resimde gözlük camları eksiktir\.
### **Simetri Problemleri — Asimetri**

Genel olarak simetri, yüz oluşturma algoritmaları için şu an büyük bir problem oluşturuyor gibi gözüküyor\. Gözlüklerine ek olarak sakalların asimetrik olması, sağ ve sol küpelerdeki deformasyon ve giyilen kıyafetteki tutarsızlıklar yapay yüzleri bulmamızda kolaylık sağlıyor\.


![](assets/eeac3aa1dde1/1*7dT_fpEXYRLE44EgrBIp4w.jpeg)



![Sol resimde göz ve kaşlarda simetrik değildir\. Sağ resimde ise kulakların birinde deformasyon vardır\.](assets/eeac3aa1dde1/1*bGW8-mTETibLaEYnnKOJNw.jpeg)

Sol resimde göz ve kaşlarda simetrik değildir\. Sağ resimde ise kulakların birinde deformasyon vardır\.
### **ve En Önemlisi**

GAN, şu an aynı yapay resmin bir başka versiyonunu oluşturamıyor, yani kişinin farklı bir açıdan görüntüsünü yaratamıyorlar\. Eğer sosyal medyadan birisi ile tanıştıysanız sadece bir resmi var ise ve yapay olduğunda şüpheleniyorsanız başka bir resmin isteyin\. Veremezler ise durum sıkıntılı demektir\.

Tabii belirtmekte fayda Wombo\.ai gibi bir resim üzerinden insanların yüzünü video olarak oynatan ya da Deepfake gibi teknolojiler sayesinde tek bir resim üzerinden gerçekci videolarda yaratılabilir\. Su an için tek teselliniz Deepfake yaratmanın, StyleGAN ile resim yaratmaya göre daha zor olmasıdır\.


> Öğrendiklerinizi denemek isterseniz\. Gerçek mi sahte mi adlı oyuna bakabilirsiniz\. [Which Face Is Real?](https://www.whichfaceisreal.com/learn.html) 





Bu resimlerin gerçek hayatta istihbarat örgütleri tarafından nasıl kullanıldığını görmek istiyorsanız bu habere bakmanızda fayda var\.


[![](https://storage.googleapis.com/afs-prod/media/afs:Medium:5682690254/800.jpeg)](https://apnews.com/article/ap-top-news-artificial-intelligence-social-platforms-think-tanks-politics-bc2f19097a4c4fffaa00de6770b8a60d)


Daha farklı teknikler ve StyleGAN ile başka ne tür şeyler yapay olarak yapılabilir bakmak isterseniz, güzel bir liste hazırladım,
- Yapay Kedi Resimleri — [thiscatdoesnotexist\.com \(512×512\)](https://thiscatdoesnotexist.com/)
- Yapay Oda Resimleri — [Cozy apartment in coole — Guest suites for Rent \(thisrentaldoesnotexist\.com\)](https://thisrentaldoesnotexist.com/)
- Yapay Stackoverflow soruları — [Stack Roboflow: This Question Does Not Exist](https://stackroboflow.com/)
- Yapay Araba Resimleri — [This Automobile / Car / Vehicle Does Not Exist](https://www.thisautomobiledoesnotexist.com/)
- Yapay Şehir/Uydu Görüntüleri — [This City Does Not Exist](http://thiscitydoesnotexist.com/)
- Yapay Sahiller — [This beach does not exist](https://thisbeachdoesnotexist.com/)
- Gerçek insanların yüzlerinden sahte insan resmi üretimi [Generate look\-a\-like photos to protect your identity \(generated\.photos\)](https://generated.photos/anonymizer)
- Kriterlere göre insan resmi seçmenizi sağlayan bir site — [Gallery of AI Generated Faces \| Generated\.photos](https://generated.photos/faces)
- ve Daha fazlası için — [This X Does Not Exist](https://thisxdoesnotexist.com/)


Son olarak size bir test, Aşağıdakilerin hangileri Gerçektir ve hangileri sahtedir\.


![](assets/eeac3aa1dde1/1*rZUL06xwNRsXslWTQ9ighA.jpeg)



![](assets/eeac3aa1dde1/1*Pa9fJdOy4AexYue04yCXTg.jpeg)



![](assets/eeac3aa1dde1/1*cS7fUvbfw6EW-JobBqwNYQ.jpeg)



![](assets/eeac3aa1dde1/1*XSh84q_uRNEIyA729fj-GQ.jpeg)



![](assets/eeac3aa1dde1/1*vZnI2rNd48_K3ldCDzRlBg.jpeg)



![](assets/eeac3aa1dde1/1*1DCZsemALkEY1_fAHq5atA.jpeg)



![](assets/eeac3aa1dde1/1*y8-M3urrv4Apfy3gR7aYng.jpeg)



![Gerçek mi Sahte mi?](assets/eeac3aa1dde1/1*6qfxlU3dLh3AcRdak3NROw.jpeg)

Gerçek mi Sahte mi?
### Kaynak

[https://kcimc\.medium\.com/how\-to\-recognize\-fake\-ai\-generated\-images\-4d1f6f9a2842](https://kcimc.medium.com/how-to-recognize-fake-ai-generated-images-4d1f6f9a2842)

[Which Face Is Real?](https://www.whichfaceisreal.com/learn.html)

[Signs You’re Following A Fake Twitter Account… — NixIntel](https://nixintel.info/osint/signs-youre-following-a-fake-twitter-account/)

[AI fake\-face generators can be rewound to reveal the real faces they trained on \| MIT Technology Review](https://www.technologyreview.com/2021/10/12/1036844/ai-gan-fake-faces-data-privacy-security-leak/)

[Fact check: How do I spot a deep fake? \| World \| Breaking news and perspectives from around the globe \| DW \| 14\.01\.2022](https://www.dw.com/en/fact-check-how-do-i-spot-a-deep-fake/a-60029650)

[Joyful white adult male with short black hair and brown eyes \| Generated\.photos](https://generated.photos/face/joyful-white-adult-male-with-short-black-hair-and-brown-eyes--5e680ad76d3b380006d5dd65)

[Gallery of AI Generated Faces \| Generated\.photos](https://generated.photos/faces)



_[Post](https://medium.com/@leventd/yapay-zeka-taraf%C4%B1ndan-olu%C5%9Fturulan-sahte-ki%C5%9Filer-nas%C4%B1l-tan%C4%B1n%C4%B1r-eeac3aa1dde1) converted from Medium by [ZMediumToMarkdown](https://github.com/ZhgChgLi/ZMediumToMarkdown)._
