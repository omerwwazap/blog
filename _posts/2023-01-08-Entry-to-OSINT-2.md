---
layout: post
title: "[TR] OSINT ile Coğrafi Konum Belirleme Teknikleri – Geolocation - 2"
date: 2023-01-08 13:00 +0200
categories: [OSINT, Geolocation]
tags: [Turkish]     # TAG names should always be lowercase
img_path: /images/2023OSINT2
image:
  path: /1.png
---

# OSINT ile Coğrafi Konum Belirleme Teknikleri – Geolocation[^1]

*OSINT, kamuya açık kaynaklardan elde edilen veriler ile anlamlı bilgiler oluşturulmasıdır. OSINT’in altında kabul edebileceğimiz Coğrafi Konum Belirleme, yani Geolocation. OSINT in özel bir alanıdır. Peki Gelocation nedir?*

## OSINT Nedir?

**O**pen **S**ource **Int**elligence (OSINT), dilimize Açık Kaynak İstihbaratı olarak çevrilir. "Açık Kaynak" kısmı, kamuya açık bilgileri ifade eder ve "istihbarat" kısmı ise, hedef hakkında belirli kalıplar ve profiller oluşturabileceğimiz bilgiler ve bu bilgiler arasındaki ilişkileri bulmayı ifade eder. OSINT çok geniş bir alandır ve uygulamamasının birçok da farklı yolu vardır. **Bu yazı ise genel olarak OSINT’in alt alanlarında olan Geolocation hakkında yazılmıştır.**

## Geolcation?

Geolocation en temelinde bir resmin, videonun veya cihazın içerisindeki farklı veri türleri veya analizi ile konumunun tespit edilmesidir. Bu yazı ise daha çok resim ve vide- konumlarının tespiti hakkında yazılmıştır. Geolocation’ın OSINT kapsamında kabul edebileceğimiz iki farklı yaygın kullanım alanı vardır.

- Olayların veya konumların tespiti.
- Paylaşılan resim ve videoların doğrulanması.

Farklı kullanım alanları olsa bile temelde bir içeriğin konumunu aramaktadır. Geolcation araştırması yaparken bakılacak ve kullanılacak yöntemler her zaman aynıdır. Her araştırmada aşağıdaki üç başlık sırası fark etmezsiniz incelenmelidir.

- Metadata
- Reverse Image Search (RIS) – Tersine Görsel Arama
- Resim, Video ya da Cihazın detaylı analizi.

### Metadata

Metadata, bir kaynağı yada veriyi tanımlayama yardımcı olan ek bilgilerdir. Basitçe, kitapları birer veri kaynağı olarak kabul edersek, metadatası, kitap hakkında bilgi veren ilk sayfaları olur. Yani kitabın yazım/basım yılı, basım yeri, basım şirketi, yazarı ve editörü birer metadata olarak düşünülebilir. Aynı şekilde resim ve videolar için de metadata bulunur.

#### EXIF

Resim veya Videolar içinde, GPS koordinatları, çekim yapan kamera/telefon bilgisi, çekim zamanı gibi birçok veriyi içeren uluslararası bir veri gurubu standardıdır. Geolocation yaparken bulunma ihtimali en az olan bilgi grubu olsa da bulunması durumunda en çok bilgiye ulaşabileceğiniz verilerdir.

| [PLACE HOLDER FOR IMAGE - 1 ] |
|:--:|
| *Şekil 1: EXIF Örneği* |

Günümüzde özellikle Facebook, Instagram, Twitter ve Imgur gibi bilindik sosyal medya siteleri otomatik olarak EXIF verisini silerek sistemlerine yüklemektedir. Ancak EXIF’ın bulunabildiği yerler de vardır. Kişisel bloglar, haber siteleri ve fotoğraf paylaşım siteleri (flicker, photobucket v.b) ya da blog oluşturma siteleri otomatik olarak EXIF verisini silmez. Bu da Geolocation yaparken çok güzel bir araştırma noktası olur. Bu sebep ile bulunma ihtimali az olsa da her zaman bakılmasında fayda vardır. 

Gerçek hayattan örnek vermek gerekirse, 2012 yılında farklı sebepler ile yetkililerden kaçan Mcafee Antivüris şirketinin kurucusu John Mcafee, kaçışı sürecince birçok röportaj veriyordu ve çoğunda durumunun iyi olduğunu gösteren özel resimler paylaşıyordu. Ancak Vice ile yaptığı bir röportajda paylaşılan fotoğrafın EXIF verileri silinmeden paylaşıldığı için Mcafee’nin konumunu istemsizce paylaşmış oldular.

| [PLACE HOLDER FOR IMAGE - 2 ] |
|:--:|
| *Şekil 2: Guatemala'da olduğu görülmekte* |

Tabii bu konu ortaya çıktıktan sonra John Macafee olayı ilk önce yalanladı ama sonra doğrulayıp Guatemala yetkilileri ile iletişimde olduğunu açıkladı. Kısacası neyi nasıl paylaştığına dikkat etmenizde fayda var.

EXIF hakkında bilinmesi en öneli konulardan birisi de EXIF verilerinin değiştirilebilir olduğudur. Bir EXIF verisi bulsanız dahi mutlak doğru olarak kabul etmeyip, verileri doğrulamanız gerekmektedir. 

#### Reverse Image Search (Tersine Resim Arama)

Tersine Resim arama son zamanlarda tüm arama motorlarına eklenen bir özelliktir. Temelde internette gördüğünüz bir görseli, normal bir Google’da/Bing’de araması yapıyormuş gibi bir görseli arayabilirsiniz. Ayrıca Google, Bing ve Yandex görsel aramanın yanında yapay zekâ ile resim içeriğini tanıyıp benzer içerikler ve cisim tanıması sayesinde arattığınız görsellere benzer görseller bulmanıza yardımcı olabilir. Bu tür araştırmalar yaparken tüm arama motorlarının denenmesi tavsiye edilir, birinin bulmadığını diğerinin bulma olasılığı çok yüksektir.

| [PLACE HOLDER FOR IMAGE - 3 ] |
|:--:|
| *Şekil 3: Reverse Image Search (RIS) Örneği* |

Elimizdeki bir kişin fotoğrafını Google ile RIS yaptığımız, Google otomatik olarak Hugh Jackman diye tamamladı ve onun hakkında bilgiler getirdi. Eğer bulamasaydı olası benzer fotoğrafları listeleyecekti.

Aramalarınızı yaparken, istediğiniz sonuçları alamazsanız, görseli kırparak ya da insan, araba gibi farklı cisimleri çıkartarak arayabilirsiniz. Temelde amacınız benzersiz özellikler kalacak şekilde bir arama yapmaktır.

| [PLACE HOLDER FOR IMAGE - 4 ] |
|:--:|
| *Şekil 4: cleanup.pictures gibi bir site ile düzelteme sonrası RIS yapabilirsiniz.* |

| [PLACE HOLDER FOR IMAGE - 5 ] |
|:--:|
| *Şekil 5: Korkulukları silindikten sonra sonucu bulabildik.* |

#### Detaylı Analiz

Çoğu zaman detaylı bir analiz yapmadan “Metadata” ve “Reverse Image Search” ile aradığınız yeri bulabilirsiniz. Ancak bazı durumlarda görseli ya da videoyu detaylı bir şekilde analiz etmek ve araştırma yapak dışında bir yolunuz olmayabilir. Bir analizi yapmadan önce yapılacak ilk şey, elinizdeki görselin en yüksek kaliteli halini bulmak olmalı, bundan sonra ise OSINT metodolojisinin dört temel sorusu ile (Ne biliyorum? Bildiklerim ne anlama geliyor? Neyi bilmem gerekiyor? Nasıl bulabilirim?) tabelalara, işaretlere, manzaraya, yapılara ve peyzajlara ve hava durumuna bakmaktır.

Eğer bir video analizi yapıyorsanız, videoyu tekli kareler halinde, “frame by frame” olarak incelemeniz yada frame by frame olarak listeleyip bakmanız işinizi kolaylaştırabilir.

#### Diğer Yöntemler

Bazen yukarıda bahsettiğimiz yöntemlerin hiç birisi işinize yaramayabilir. Bu durumda daha radikal daha niş alanlar ile arama yapak durumunuzdasınız.

- Ülkeleri birinden nasıl ayırırım diye düşünüyorsanız, güzel ipuçları veren bu sitelere bakabilirsiniz,
  - [GeoH Hints](https://geohints.com/)
  - [Geo Tips](https://geotips.net/europe/)
  - Dil Tespiti için - [GeoGuessr The Top Tips, Tricks and Techniques](https://somerandomstuff1.wordpress.com/2019/02/08/geoguessr-the-top-tips-tricks-and-techniques/#languages)
- Bilmediğiniz bir araç plakası mı var? Dünyadaki tüm geçmiş ve mevcut araç plaka tiplerini listeleyen sitelere bakabilirsiniz.
  - [World License Plates](https://www.worldlicenseplates.com/)
- Ülke bayrağı olmadığını düşündüğünüz bayraklar mı görülüyorsunuz? Bunun için bu sitelere bakabilirsiniz.
  - [Flag ID](https://flagid.org/)
  - [The Flag-Finder](https://www.flaggenlexikon.de/flag-finder/index_dt.htm)
- Bir uçak kodu mu gördünüz ya da fotoğrafı mı var? Bunun için sitelere bu bakabilirsiniz.
  - [FlightAware](https://tr.flightaware.com/)
- Dağ ya da tepeler mi görüyorsunuz? Bunun için de özel siteler var.
  - [Mountain Explorer](https://peakvisor.com/)
  - [Peak Finder](https://www.peakfinder.com/)
- Bilmediğiniz bir futbol forması mı gördünüz? Bunun için bu sitelere bakabilirsiniz.
  - [Football Kit Archive](https://www.footballkitarchive.com/)
- Resmi bir kimlik ya da pasaport yüzümü gördünüz? Bunun için de özel siteler var.
  - [Netherlands Police Edison Software](https://www.edisontd.nl/)
  - [Passport Index](https://www.passportindex.org/)
- Askeri kamuflaj mı gördünüz? Bunun için bu siteye bakabilirsiniz.
  - [List of Military Clothing Camouflage Patterns](https://military-history.fandom.com/wiki/List_of_military_clothing_camouflage_patterns)
  - [Camopedia](https://www.camopedia.org/index.php/Main_Page)

Gibi yukarıdaki siteler ve aklınıza gelebilecek her şeyin listesini tutan sitler bulunuyor. Yapmanız gereken tek şey arayabileceğiniz bir şey bulup, aradığınız coğrafi alanı daraltmaktır.

Basit bir geolcation örneği görmek isterseniz; bu basit örneğe bakabilirsiniz. [Last Toy Train Home — OSINT Challenge 11](https://medium.com/@leventd/quiztime-random-osint-challenge-11-abc5ea122597) Medium hesabımda 30'a yakın geolcation çözümü bulunuyor 😀

## Kaynak[^2]

- [Last Toy Train Home — OSINT Challenge 11](https://medium.com/@leventd/quiztime-random-osint-challenge-11-abc5ea122597)
- [A Very Particular Set of Skills: Geolocation Techniques For OSINT and Investigation](https://www.irongeek.com/i.php?page=videos/circlecitycon2018/circle-city-con-50-304-a-very-particular-set-of-skills-geolocation-techniques-for-osint-and-investigation-chris-kindig)
- [Tell, Explain, Describe… Asking The Right Questions To Get The Right Answers – Quiztime 25th June 2019 – NixIntel](https://nixintel.info/osint/tell-explain-describe-asking-the-right-questions-to-get-the-right-answers-quiztime-25th-june-2019/)
- [10 Minute Tip: How to geolocate from images and videos, Part 1](https://osintcurio.us/2020/11/01/ten-minute-tip-image-geolocation-part-1/)
- [The Sunny Side of Geolocation Verifications](https://keyfindings.blog/2018/10/02/the-sunny-side-of-geolocation-verifications/)
- [John mMcafee Location Exif](https://nakedsecurity.sophos.com/2012/12/03/john-mcafee-location-exif/)
- [EXIF Data May Have Revealed Location of Fugitive Software Tycoon John McAfee](https://petapixel.com/2012/12/03/exif-data-may-have-revealed-location-of-fugitive-billionaire-john-mcafee/)
- [Vice.com John McAfee Exclusive Reveals His Location in iPhone EXIF Data](https://www.mobileprivacy.org/2012/12/vice-com-publishes-exclusive-with-john-mcafee-reveals-location-in-iphone-metadata-exif/)

[^1]: First published here [Levent's Turkcell Geleceği Yazanlar](https://gelecegiyazanlar.turkcell.com.tr/blog/osint-ile-cografi-konum-belirleme-teknikleri-geolocation-2).
[^2]: [Banner resim kaynağı](https://www.browserstack.com/blog/geolocation-takes-over-the-power-of-testing-websites-and-mobile-apps-around-the-world/)