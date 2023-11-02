---
layout: post
title: "[TR - Work In Progress] Yapay Zekâ Tarafından Oluşturulan Sahte Kişiler Nasıl Tanınır?"
date: 2022-01-20 12:00 +0200
categories: [Cyber Security, General, Artificial Intelligence]
tags: [Turkish,AI]     # TAG names should always be lowercase
img_path: /images/2022AITespit
image:
  path: /0.png
  alt: Acaba Gerçek olan birisi var mı?
---

# Yapay Zekâ Tarafından Oluşturulan Sahte Kişiler Nasıl Tanınır?[^1]

> Bu blog yazısı 2022 Ocak Ayında yazılmıştır. 2023 sonuna doğru aşağıda bahsedilen bir çok konuda çok ciddi gelişmeler oldu. Lütfen bunu göz önünde bulundurarak okuyunuz ama yine de güzel bir temel oluşturmanızı sağlayabilir. Ilerleyen zamanlarda bu blogun sadece güncel olan konularını içerecek ikinci kısmını yazmayı planlıyorum.
{: .prompt-danger }

*2000'li yıllarda üzerinde çalışılmaya başlanılan ve hayatımıza ilk kez Matrix, Terminator ve Tron filmleri ile girmiş olan Sentetik Yüz Oluşturma teknolojisi 2014'te Ian Goodfellow’un GAN (generative adversarial network) teknolojisi ile çok farklı boyutlara ulaşmıştır. Ancak 2018'e kadar gündelik hayatımıza girmemiştir.*

GAN nedir diye sorarsanız çok basit bir şekilde, İki adet öğrenebilen yapay zekâ olduğunu düşünün. Bunlardan bir tanesi bir referanstan (komut/resim) yola çıkarak yapay bir resim oluşturuyor\. Diğer yapay zekâ da bu resmin gerçek olup olmadığını tahmin etmeye çalışıyor\. Bu şekilde resmi oluşturan yapay zekâ tahmin edilememek için gelişiyor ve diğer yapay zekâda resimleri daha doğru tahmin edebilmek için gelişiyor\. İlk basit örneklere bakacak olursak,

![Face Generation](/1.png)
*2014 DCGAN Algoritması ile oluşturulmuş Sahte İnsan Yüzleri*

Görüldüğü 2014'te yapılan çalışmalar zamanına göre çok ilgi çekici olsa da, kolayca sahte olduklarını anlayabilirsiniz. Ancak 2018'de NVIDIA’nın duyurmuş olduğu ve hâlâ geliştirmekte olan StyleGAN adı verilen GAN, yukarıdaki resimleri çok farklı bir boyuta getirmiştir.

![Face Generation](/0.png)
*2018 NVIDIA StyleGAN version 1 (2022 itibari ile StyleGAN3 çıkmıştır)*

Görüldüğü gibi gerçek mi sahte mi olduğunu anlamak çok zor bir hâlâ gelmiştir. Bunu fark edenler, yapay insan yüzleri ile Sosyal Medya hesapları açmaya başlamış ve dolandırıcılık gibi kötü amaçlı işler için kullanmaktadırlar. Neyse ki şu an itibariyle bu teknoloji mükemmelleştirilmiş değildir.

StyleGAN şu an en gelişmiş yapay yüz oluşturma metholdarında birisi olarak kabul edilse de. Oluşturulan resimlerin sahte olduğu anlamamın birkaç yolu vardır.

## Arka Plan

Yüz eğitmek için oluşturulan GAN’lar resimlerin arka planlarını oluşturmakta pekiyi değildir. Araka planda okunması zor yazılar, surreal görüntüler ve fiziksel olarak imkânsız manzaralar görebilirsiniz. Bunun nedeni GAN’ı oluştururken kullanılan resimlerin genelde sadece insan kafasının ortalanmış ve kesilmiş(crop) resimler ile oluşturulmasındandır. Bu sebep ile arka plandan bir bilgi öğrenmesi oldukça zordur

> Aşağıdaki örnekler [thispersondoesnotexist](https://thispersondoesnotexist.com/) sitesinde oluşturulmuştur.

| ![Face Generation](/2.jpeg) | ![Face Generation](/3.jpeg) |
| ![Face Generation](/4.jpeg) | ![Face Generation](/5.jpeg) |

<p style="text-align: center;"> Arka planlarda gariplikler</p>

## Garip Dişler

Dişlerin işlenmesi pek kolay değildir. Genellikle dişler tuhaf renkli, anormal şekilli veya asimetriktir. Bazı durumlarda, aşağıdaki gibi üç azı dişi bile görebilirsiniz.

| ![Face Generation](/6.jpeg) | ![Face Generation](/7.jpeg) | ![Face Generation](/8.jpeg) |

<p style="text-align: center;"> Resimlerin üzerinde tıklayarak dişlerdeki problemleri görebilirsiniz</p>

## Saçların Görünüşü — Yeni uyanmış gibi saçlar

Saçın gerçekçi bir şekilde işlenmesi büyük bir problem gibi gözüküyor. Bazen yüzlerde veya başka bir yerde bağlantısız saç telleri görebilrisiniz. Diğer zamanlarda ssaçın etrafında garip bir parıltı veya fon olabilir. Çok nadiren de sanki Paint ile photoshop’lanmış saç uçları da bulabilirsiniz.

| ![Face Generation](/9.jpeg) | ![Face Generation](/10.jpeg) |
| ![Face Generation](/11.jpeg) | ![Face Generation](/12.jpeg) |

<p style="text-align: center;"> Kırmızı ile işaretlenmiştir.</p>

## Renk Kanaması

Bazı resimlerde ufak renk bozuklukları olduğunu görebilirsiniz.

| ![Face Generation](/13.jpeg) | ![Face Generation](/14.jpeg) |
| ![Face Generation](/15.jpeg) | ![Face Generation](/16.jpeg) |

<p style="text-align: center;">Tüm resimlerde, kıyafetlerin yakasına dikkatli bakmalısınız.</p>

## Kayıp Küpeler — Asimetri

GAN’ı oluştururken kullanılan resimlerin bazılarında küpe olması ve bazılarında olmaması, oluşturulan yapay yüzlerde sorunlar yatabiliyor. Ancak bu sorunlar son GAN versiyonlarında büyük oranda çözülmüştür.

| ![Face Generation](/17.jpeg) | ![Face Generation](/18.jpeg) |

<p style="text-align: center;">Sol resimde küpe kulak ile birleşmiş ve Sağ resimde bir küpe eksik.</p>

## Water Splotches[^2]

Bu şekilde olan resimleri birisi profil fotoğrafı olarak kullanmaz ancak görmeniz durumunda yapay yüz yaratma algoritması ile yapıldığını anlayabilirsiniz.

| ![Face Generation](/19.jpeg) | ![Face Generation](/20.jpeg) |

<p style="text-align: center;">Genellikle Küpelerin olduğu yerde görülse de yukarıdaki örnekleri gibi farklı yerlerde de karşınıza çıkabilir.</p>

## Gözlükler — Asimetri

Şu anda, algoritmalar gerçekçi görünümlü gözlükler oluşturmayı pek beceremiyor. Genel bir simetri sorunu yaşıyorlar. Oluşturulan çerçevelerde genellikle sağ tarafında ve sol tarafında fiziksel farklılıklar oluyor.

| ![Face Generation](/21.jpeg) | ![Face Generation](/18.jpeg) | ![Face Generation](/22.jpeg) |

<p style="text-align: center;">Gözlüklerin çerçevelerinde deformasyonlar vardır ve tam simetrik değildir. Ayrıca ilk resimde gözlük camları eksiktir.</p>

## Simetri Problemleri — Asimetri

Genel olarak simetri, yüz oluşturma algoritmaları için şu an büyük bir problem oluşturuyor gibi gözüküyor. Gözlüklerine ek olarak sakalların asimetrik olması, sağ ve sol küpelerdeki deformasyon ve giyilen kıyafetteki tutarsızlıklar yapay yüzleri bulmamızda kolaylık sağlıyor.

| ![Face Generation](/23.jpeg) | ![Face Generation](/24.jpeg) |

<p style="text-align: center;">Sol resimde göz ve kaşlarda simetrik değildir. Sağ resimde ise kulakların birinde deformasyon vardır.</p>

## ve En Önemlisi

GAN, şu an aynı yapay resmin bir başka versiyonunu oluşturamıyor, yani kişinin farklı bir açıdan görüntüsünü yaratamıyorlar. Eğer sosyal medyadan birisi ile tanıştıysanız sadece bir resmi var ise ve yapay olduğunda şüpheleniyorsanız başka bir resmin isteyin. Veremezler ise durum sıkıntılı demektir.

Tabii belirtmekte fayda [Wombo.ai](https://www.w.ai/) gibi bir resim üzerinden insanların yüzünü video olarak oynatan ya da Deepfake gibi teknolojiler sayesinde tek bir resim üzerinden gerçekci videolarda yaratılabilir. Su an için tek teselliniz Deepfake yaratmanın, StyleGAN ile resim yaratmaya göre daha zor olmasıdır.

Öğrendiklerinizi denemek isterseniz, gerçek mi sahte mi adlı oyunlarına bakabilirsiniz.

- [Which Face Is Real?](https://www.whichfaceisreal.com/learn.html)
- [Detect Fakes - Attention check: Fabricated or Authentic](https://detectfakes.media.mit.edu/)

Ek olarak, bu resimlerin gerçek hayatta istihbarat örgütleri tarafından nasıl kullanıldığını görmek istiyorsanız bu habere bakmanızda fayda var. [Incelemek isterseniz buradan bakabilirsiniz.](https://apnews.com/article/ap-top-news-artificial-intelligence-social-platforms-think-tanks-politics-bc2f19097a4c4fffaa00de6770b8a60d)

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

> 2022 Ocak'tan beri çok fazla farklı uygulamalar çıktı, internette araştırmanızda fayda var.
{: .prompt-tip }

Teknik olarak daha detaylı bir yazı için bu seriyi okuyabilirsiniz,

- [Detect AI-generated Images & Deepfakes (Part 1)](https://jonathan-hui.medium.com/detect-ai-generated-images-deepfakes-part-1-b518ed5075f4)
- [Detect AI-generated Images & Deepfakes (Part 2)](https://jonathan-hui.medium.com/detect-ai-generated-images-deepfakes-part-2-436c57eeb878)
- [Detect AI-generated Images & Deepfakes (Part 3)](https://jonathan-hui.medium.com/detect-ai-generated-images-deepfakes-part-3-9c3fdf97d572)

Ilginizi çekebilecek diğer siteler,

- [How to Spot Synthetic Faces Online — the Clue Is in the Eyes](https://www.discovermagazine.com/technology/how-to-spot-synthetic-faces-online-the-clue-is-in-the-eyes)
- [Glut of Fake LinkedIn Profiles Pits HR Against the Bots](https://krebsonsecurity.com/2022/10/glut-of-fake-linkedin-profiles-pits-hr-against-the-bots/)

## Kaynak

[^1]: İl olarak burada paylaşıldı [Levent's Medium](https://medium.com/@leventd/yapay-zeka-taraf%C4%B1ndan-olu%C5%9Fturulan-sahte-ki%C5%9Filer-nas%C4%B1l-tan%C4%B1n%C4%B1r-eeac3aa1dde1).
[^2]: Yeni GAN uygulamalarında artık pek fazla karşılaşılmıyor.
