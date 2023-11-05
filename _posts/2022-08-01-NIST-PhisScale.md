---
layout: post
title: "[TR] NIST Phish Scale Oltalama Testlerinin Optimize Edilmesi"
date: 2023-05-01 12:00 +0200
categories: [Cyber Security, Phishing]
tags: [Turkish, Academic]     # TAG names should always be lowercase
img_path: /images/2023PhishScale
pin: true
image:
  path: /0.webp
  alt: NIST Phish Scale.
---

# NIST Phish Scale: Oltalama Testlerinin Optimize Edilmesi [^1]

*2020 yılında ABD Ulusal Standartlar ve Teknoloji Enstitüsü (NIST) tarafından akademik bir çalışma olarak ortaya çıkan ve halen geliştirilmekte olan Phish Scale bir Oltalama Test Zorluk Ölçeğidir. Hedefi kuruluşların çalışanlarına daha iyi eğitim vermesine yardımcı olmak ve çalışanların neden Oltalama maillerine tıkladıklarını daha iyi anlaması için yapılan analitik bir değerlendirme ölçeğidir.*

## Oltalama Nedir

Oltalama, suçluların insanları tehlikeli bir web sitesinin bağlantısına tıklamak gibi “yanlış olanı” yapmaları için kandırmaya çalışmasıdır. Oltalama, SMS, MMS, Sosyal Medya veya Telefon yoluyla gerçekleştirilebilir, ancak “Oltalama” terimi esas olarak e-posta yoluyla gelen saldırıları tanımlamak için kullanılır. Kurumlar, kendini korumak için her ne kadar spam filtreleri ve mail güvenliği sağlayan uygulamalar, URL analiz araçları gibi teknik önlemler kullansa da her zaman zararlı e-postaları tespit edemeyebilirler. Bu sebeple şirketler, çalışılanların bu tür saldırılara karşı eğitmek için Oltalama Testleri yapmaktadır.

## Oltalama Testleri

Oltalama Testleri etkili bir şekilde yapmanın belli başlı zorlukları vardır. Testin **etkili ve gerçekçi** olmasını isterken, çalışanları bunaltmak, onlar için sorunlar yaratmak veya zorlamak istemezsiniz. Ayrıca tespitin imkânsız olmasını, kurum içi veya kurum dışı problemler oluşturmasını kesinlikle istemezsiniz. NIST’in Phish Scale’i ise oltalamanın tespit edilebilirlik sorununu çözmek için geliştirilmektedir. Zam beklenen bir zamanda prim, promosyon veya zam hakkında bir oltalama yapmak çok risklidir. Hem çalışanı rahatsız etmiş olursunuz hem de şirket içi sorunlar yaratabilirsiniz. 
2022 yılında zam ve promosyon konuları hakkında Oltalama Testi yapan ve özür dilemek zorunda kalan şirketler oldu. Bu tür konulara hakkında test yapılacak ise yönetimden onay alınarak ilerlenmesi çok daha doğru olacaktır.

Phish Scale, oltalama testlerinin zorluğunu değerlendirmenize yardımcı olacak ve kullanımı kolay bir araç olarak sunulmaktadır. Yalnızca testlerin zorluğunu optimize etmenize yardımcı olmakla kalmaz, aynı zamanda önemli performans ölçümlerine odaklanabilmek için çalışanların güçlü ve zayıf yönlerine ilişkin bilgiler de sağlayabilir.

Oltalama Testlerinin çoğunda indikatör (KPI) olarak tıklama oranı kullanılır ve buna göre bir analiz oluşturulur, ancak bu pek yeterli olmaz. Phish Scale tıklama oranı dışında birkaç farklı KPI sunarak, derinlemesine bilgi edinmemize yardımcı oluyor. Bunu ise iki farklı veri setiyle gerçekleştiriyor;

- **Gözlemlenebilir İpuçları:** Test gönderiminde yazım hatası, yanlış isim veya diğer yanlış içeriklerin sayısıdır. Çalışana bir oltalamanın sahte olduğuna dair kaç ipucu vardır sorusunu cevaplar.
- **Uyum/Bilinirlik:** İşyeri süreçlerini, mevcut şirket olaylarını veya iş dışı gündem ile alakaları ne seviyededir diye bakılır. Çalışanın konu ile uyumu, bilinirliği ve tanınırlığı ne derecededir sorusunu cevaplar.

Bu veriler ile birlikte NIST, bir oltalama senaryosunun ne kadar zor olduğunu analitik olarak hesaplamaya çalışmaktadır.

### Phish Scale’in Uygulanması

**Gözlemlenebilir İpuçları**, 5 temel başlık altında değerlendirilmektedir.

| | | | | |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| Yazım Hataları | Genel Hatalar | Görsel Hatalar | Dil ve Anlam Hataları | Teknik Belirtiler |

Bu kategorilerdeki örnekler yazım ve dil bilgisi düzensizlikleri, tutarsız e-posta adresi, logo taklidi, tehdit edici dil ve aciliyet hissi veren teklifler sayılabilir. Bu tür ipuçlarının toplam sayısı kullanılmaktadır.

**Uyum/Bilinirlik**, yine 5 temel başlık altında değerlendirilmektedir.

| | | | | |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| İşyeri sürecinin taklidi | İşyeri ile alakası | Güncel durum ve olaylar ile alakası | Tıklama için endişe ve süre ile endişe verme | Hedeflenen eğitime veya özel uyarılara maruz kalma |

Bu değerlendirmelerin her biri için “aşırı” (8 puan), “önemli” (6 puan), “orta” (4 puan), “düşük” (2 puan) veya “uygun değil” (0 puan) olarak derecelendirilmesi gerekmektedir. Daha sonra gözlemlenebilir ipuçları verisi ile birlikte değerlendirilip bize zorluk seviyesini verir.

Bu değerlendirmelerin her biri için **“aşırı” (8 puan), “önemli” (6 puan), “orta” (4 puan), “düşük” (2 puan) veya “uygun değil” (0 puan)** olarak derecelendirilmesi gerekmektedir. Daha sonra gözlemlenebilir ipuçları verisi ile birlikte değerlendirilip bize zorluk seviyesini verir.

#### Sonuçların Hesaplanması

Zorluk derecesini değerlendirmek için, öncelikle her bir Gözlemlenebilir İpucu örneğini saymanız gerekiyor (örneğin, her bir yazım ve dilbilgisi hatası). Toplamı ipucu sayısı bulunduktan sonra ise ipucu derecesini belirlemeniz gerekiyor.

| Toplam Gözlemlenebilir İpuçları | Phish Scale – İpucu Derecesi |
| :-------------: | :-------------: |
| 1 – 8 | Az |
| 1 – 8 | Biraz |
| 15 ve fazlası | Çok |

Ardından Uyum/Bilinirlik hesaplamaları için NITS Phis Scale iki farklı yol sunuyor,

- Uyum/Bilinirlik konularının her biri için karşılık gelen derecesi ile hesaplama yapmak.
- Herhangi bir hesap yapmadan, Yüksek, Orta ve Düşük olarak subjektif bir uyumluluk seçimi yapmak.

![Image](/1.png) _NIST Phish Scale Tanıtım Sunumundan alınmıştır._

##### Uyum/Bilinirlik Hesapları – Seçerek Hesaplama

**Yüksek Uyumlu**; Oltalama Testi, hedef kitlenin iş sorumlulukları veya uygulamalarıyla örtüştüğü, son derece makul olduğu ve/veya hedef ilgili bir olayla bağdaşan konulardır. Örneğin, alıcı finans departmanıysa ve oltalama mesajında ​​ödeme gecikmiş veya yapılmamışsa gibi konular işleniyorsa, genel uyum yüksektir.

**Orta Uyumlu**; Orta uyum iki farklı şekilde sağlanır, birincisi Oltalama testinin konusu makul ve mantıklı olması ama hedef ile ilişkisinin kuvvetli olmaması durumu. İkincisi ise, hedefin bir kısmı ile makul ve mantıklı bir oltalama konusu seçilmesi. Örneğin, Oltalama testinde Metaverse konusu işleniyorsa ve şirketin bir kısmı bu konu ile ilgileniyorsa, genel uyum orta seviyesindedir denebilir.

**Düşük Uyumlu**; Testin hedef kitlesi ile alakalı olmayan bir konu ile ilgili olduğunda uyum düşüktür. Örneğin, alıcı finans departmanıysa ve oltalama, biyoteknoloji araştırmaları veya benzer şekilde ilgisiz bir konu hakkında ise, genel uyum düşüktür.

##### Uyumluluk Hesapları – Puan ile Hesaplama

Diğer bir hesaplama yöntemi ise Uyumluğun 5 temel başlığına verilen puanlama ile yapılmaktadır. Subjektifliği azalttığı için bu yöntem daha çok tercih edilmektedir.

| Uyum / Bilinirlik | Phish Scale – Uyum Derecesi |
| :-------------: | :-------------: |
| Aşırı Yüksek Düzeyde Uyum ve Alaka | 8 |
| Yüksek Düzeyde Uyum ve Alaka | 6 |
| Orta Düzeyde Uyum ve Alaka | 4 |
| Düşük Düzeyde Uyum ve Alaka | 2 |
| Uyum ve Alaka Yok | 0 |

Bu yöntem ile elde edilen sonuçlar -8 ile 32 arasında hesaplanacak şekilde derecelendirilmiştir. Hesaplama yönetimi ise aşağıdaki gibidir.

| Uyum / Bilinirlik | Phish Scale – Uyum Derecesi |
| :-------------: | :-------------: |
| İşyeri sürecinin taklidi | + Toplama |
| İşyeri ile alakası | + Toplama |
| Güncel durum ve olaylar ile alakası | + Toplama |
| Tıklama için endişe ve süre ile endişe verme | + Toplama |
| Hedeflenen konu için eğitime veya özel uyarılara maruz kalma | - Çıkarma |

Gerekli hesaplamalar yapıldıktan sonra elde edilen sonuçları aşağıdaki tabloya göre derecelendirerek genel testin genel uyum derecesi bulunur.

| Uyum / Bilinirlik - Puanı | Phish Scale – Uyum Derecesi |
| :-------------: | :-------------: |
| -8 ve 10 | Düşük Uyumlu |
| 11 – 17 | Orta Uyumlu |
| 18 ve daha fazlası | Yüksek Uyumlu |

Yukarıda bahsedildiği gibi Uyum/Bilinirlik değerlendirmesi her ne kadar sayısal bir hesaplama olsa da temelinde **subjektif** bir yöntem ile hesaplanıyor. Yani oltalama uyumluluğu için farklı kişiler farklı Phish Scale hesaplamaları yapabilmektedir.
Bu durum NIST makalelerinde de dile getirilmektedir ancak farklı araştırmacılar ile yapılan analizlerde subjektifliğin göz ardı edilebilir bir seviyede olduğu gözlemlenmiştir. A
ynı şekilde Turkcell olarak da bunun göz ardı edilebilir olduğunu gözlemledik.

##### Test Zorluk Derecesinin Belirlenmesi

Uyum ve İpucu dereceleri belirlendikten sonra, aşağıdaki tabloyu kullanarak Oltalama testinin zorluk seviyesini kolayca belirleyebilirsiniz.

| İpucu Sayısı | Uyum Derecesi | Oltalama Zorluğu |
| ----------- | ----------- | ----------- |
|Az (daha zor) | Yüksek| Çok Zor|
|Az (daha zor)| Orta| Çok Zor|
|Az (daha zor) | Düşük| Orta Derecede Zor|
|Biraz | Yüksek| Çok Zor|
|Biraz | Orta| Orta Derecede Zor|
|Biraz | Düşük| Ortala ile Basit Arasında|
|Çok (zor değil) | Yüksek| Orta Derecede Zor|
|Çok (zor değil) | Orta| Orta Derecede Zor|
|Çok (zor değil) | Düşük| Basit|

Bu şekilde yapılan veya yapmak istediğiniz bir oltalama testinin zorluğunu belirlemiş oluyorsunuz.

![Image](/2.png) _NIST Phish Scale Tanıtım Sunumundan alınmıştır._

## Oltalama Sonuçlarının Değerlendirilmesi

| Simülasyon No | Oltalama Adı | Katılımcı | Saldırı Vektörü | Toplam İpucu | İpucu Derecesi| Uyum Derecesi | Uyum Derecesi | Zorluk Derecesi | Tıklama Oranı |
| :-------------:  | :-------------: | :-------------: | :-------------: | :-------------: | :-------------: | :-----------: | :-------------: | :-------------: | :-------------: |
| 1| ABC1| 5320| Mail Link| 6| Az| 20| Yüksek| Çok Zor| %10,11|
| 2| ABC2| 5320| Mail Link| 6| Az| 22| Yüksek| Çok Zor| %8,09|
| 3| ABC3| 5320| Mail Link| 9| Biraz| 18| Yüksek| Çok Zor| %9,66|
| 4| ABC4| 5320| Mail Link| 10| Biraz| 24| Yüksek| Çok Zor| %7,52|

Oltalama testlerini yaptıkça yukarıdaki gibi bir tablo elde edebilir ve kendinize göre eklemeler yaparak analizinizi daha da zenginleştirebilirsiniz. Oltalama Bildirim Oranı, Oltalama Konusu, Hedef Kitle, Veri giriş oranları gibi birçok veri ile besleyebilirsiniz.

Uyum subjektifliği dışında gördüğümüz önemli bir eksiklik ise saldırı vektörünün hesaplamalara dahil edilmemesidir. En basit tabiriyle SMS/MMS ile yapılan bir oltalamadaki (Smishing Testi) link gönderimi ile e-posta üzerinden gönderilen linkin inandırıcılığı ve zorluğu çok farklıdır. Aynı zamanda dosya eki ile yapılan bir test sadece link ile yapılan bir mail testinden çok daha zor olacaktır. Kısacası mükemmel bir ölçek değildir ancak kurumlar için güzel bir başlangıç olduracak olgunluktadır.

## Bir Örnek Yapalım

![Image](/3.png) _Gerçek bir saldırı üzerinde deneyelim_

Yukarıdaki örnek oltalama mailinde 6 tane kolayca Gözlenebilir İpucu bulunuyor bu da ipucu derece tablomuza göre, ipucu derecisini **Az** olarak belirlememizi sağlıyor.

Uyum/Bilinirlik seviyesi için ise Turkcell çalışanına yapılmış bir oltalama simülasyonu olarak değerlendirirsek, "Bir işyeri sürecini taklit eder" (+0 puan), "iş yeri alaka düzeyi" (+2 puan), "durumlar veya olaylarla uyum sağlar” (+4 puan), “Tıklamama endişesi” (+8 puan) ve “hedeflenen eğitim konusu” (-4 Puan), kişisel olarak değerlendirdiğim Uyum Derecesi toplamı 10 puan yapıyor ve uyumluluk derece tablomuza göre dereceyi **Düşük** olarak hesaplıyoruz.

Genel test değerlendirmesi için ise “Az” Gözlenebilir İpuçları ve “Düşük” Uyum Derecesi ile tabloya bakarsak, yukarıdaki Oltalama testinin **Orta Derecede Zor” bir Oltalama testi olduğunu görüyoruz.**

## Kaynak

[^1]: First published here [Levent's Turkcell Geleceği Yazanlar](https://gelecegiyazanlar.turkcell.com.tr/blog/nist-phish-scale-oltalama-testlerinin-optimize-edilmesi).

--

- <https://academic.oup.com/cybersecurity/article/6/1/tyaa009/5905453?login=false#207409537>
- <https://csrc.nist.gov/Projects/Usable-Cybersecurity/Research-Publications#Phishing_behaviors>
- <https://www.nist.gov/news-events/news/2020/09/phish-scale-nist-developed-method-helps-it-staff-see-why-users-click>
- <https://www.nist.gov/publications/scaling-phish-advancing-nist-phish-scale>
- <https://news.ohsu.edu/2022/04/15/ohsu-statement-on-phishing-exercise>
- <https://www.theguardian.com/uk-news/2021/may/10/train-firms-worker-bonus-email-is-actually-cyber-security-test>
- <https://www.businessinsider.com/godaddy-disguised-a-phishing-email-test-as-holiday-bonus-announcement-2020-12>
