---
layout: post
title: "[TR] OSINT – Açık Kaynak İstihbarata Giriş - 1"
date: 2023-01-08 12:00 +0200
categories: [OSINT, Geolocation]
tags: [Turkish]     # TAG names should always be lowercase
img_path: /images/2023OSINT1
image:
  path: /1.webp
---

# OSINT – Açık Kaynak İstihbarata Giriş - 1 [^1]

*OSINT, genellikle gazetecilerden ve güvenlik camiasında duyacağınız bir tabirdir. Gazeteciler ve güvenlik uzmanları için temel bir beceri ve düşünme metodolojidir. Peki OSINT nedir?*

**O**pen **S**ource **Int**elligence (OSINT), dilimize Açık Kaynak İstihbaratı olarak çevrilir. "Açık Kaynak" kısmı, kamuya açık bilgileri ifade eder ve "istihbarat" kısmı ise, hedef hakkında belirli kalıplar ve profiller oluşturabileceğimiz bilgiler ve bu bilgiler arasındaki ilişkileri bulmayı ifade eder. OSINT çok geniş bir alandır ve uygulamanın birçok farklı yolu vardır. **Bu seri OSINT’in teknik veya siber güvenlik alanlarından değil. OSINT’in ne olduğundan, metodolojisinden ve kullanım alanlardan bahsedecektir.** Serinin devamında Geolocation ve Chronolocation gibi özel alanlarından bahsedecektir.

OSINT, en temelde bir istihbarat toplama yöntemidir. Belirli bir istihbarat gereksinimini ele almak amacıyla bir kitle için zamanında toplanan, kullanılan ve kamuya açık bilgilerden üretilen istihbarat elde etme yönetimidir. OSINT aynı zamanda bir üst başlıktır ve birçok alt dalı vardır. İstihbarat toplama yönetimlerinin en bilineni olmakla beraber bireysel olarak uygulanabilirliğini en yüksek alanlardan birisidir. Çoğunlukla aşağıdaki diğer istihbarat toplama yöntemleri ile beraber görebilirsiniz.

- **GEOINT** - Coğrafi konum istihbaratı. Uydu ve hava fotoğrafları kullanılarak elde edilen istihbarat.
- **SIGINT** - Sinyal istihbaratı - Sinyallerin ile elde edilen istihbarat.
- **CTI / CYBINT** - Siber istihbarat, Siber dünyadan elde edilen istihbarat.
- **SOCMINT** - Sosyal Medya İstihbaratı, Sosyal Medyada paylaşılan bilgi, fotoğraf ve konum gibi Sosyal Medyada olan her şeyden elde edilen istihbarat türüdür.

## Neden OSINT Yapılır ve Hangi Kaynaklar Kullanılır?

İnsanların ve kurumların OSINT’i kullanıyor olmasının birçok nedeni olabilir; dolandırıcılık, hack’leme, içerik doğrulama (görsel, video, olay vb.) bilgi edinme, marka koruma ve güncel durum takibi gibi legal veya illegal olan pek çok konu hakkında kullanabilirsiniz. Ayrıca aynı zamanda görece daha basit konular içinde kullanabilirsiniz.

- İşe görüşmeleri öncesi işverenler veya iş başvurusu yapanlar, karşı taraf hakkında bilgi edinmek için kullanabilir.
- Aldığınız üründe bir sorun olması durumunda şirketi yöneticilerinin iletişim bilgilerini bulmak için kullanabilir.
- Siber suçlar, tehditler ve Siber güvenlik faaliyetleri hakkında bilgi edinmek için kullanabilir.
- Kayıp insanları veya kayıp aile üyelerini bulmak için kullanabilir.
- Pentesting gibi siber güvenlik alanlarında hedef hakkında bilgi toplamak için kullanabilir.

Anlayacağınız üzere OSINT birçok farklı alanda kullanılabilmektedir. Kısacası halka açık kaynaklar ile birer araştırma yapmış iseniz OSINT’ın **O**pen **S**ource araştırma kısmını yapıyorsunuz demektir.  Genel olarak **OS**INT kaynaklarına bu örnekleri de verebiliriz,

- Kütüphanelerdeki kitaplar, gazeteler, dergiler ve halka açık belgeler.
- Devlet kurumları ve özel kuruluşların halka açık veri tabanları ve bilgileri.
- Televizyon, radyo ve çevrimiçi haber arşivleri.
- Facebook, Tiktok, Instagram, Twitter ve LinkedIn gibi sosyal medya platformları.
- Clearnet'in erişilebilen tüm alanları ("normal" internet).
- Darknet'in erişilebilen tüm alanları (Tor veya I2P kullanımı).

Yukarıda vermiş olduğum örneklere göre, OSINT kapsamı, araştırma hedefiniz ile teması olmayan araştırma türleri olarak gözükmektedir ama araştırmalarımızda bu her zaman mümkün değildir. Bu sebeple OSINT araştırmaları iki tür olarak kabul edilir.

- **Pasif Toplama** – Bu yöntem istihbarat toplarken en çok kullanılan türdür, yaptığınız keşif ve araştırmalar hedef’ten bağımsız ve hedeften habersiz yapılmaktadır.
- **Aktif Toplama** - Bu yöntemde bilgi toplamak istediğiniz hedef ile doğrudan etkileşime girersiniz, bu sebep ile de hedef, keşif ve araştırma sürecinizden haberdar olabilir.

## Peki Ne OSINT Değildir?

OSINT çoğunlukla **pasif** ve **her zaman yasalara** uygun yapılan bir araştırma türüdür. Bir araştırma yasaları çiğnemeyi veya erişmenize izin verilmeyen bilgilere erişmeyi gerektiriyorsa, bu OSINT kapsamında değildir. Casus yazılım kullanımı gibi siber saldırılar ve polis arama emri olmadan yürütülen herhangi bir casusluk, dünyanın hemen hemen her yerinde son derece yasa dışıdır. Bunlar kesinlikle OSINT değildir.

Diğer bir konu ise OS**INT** (**Int**elligence) normal bir araştırmadan farklıdır. “Bunu Google ile bulabilirim” gibi bir yaklaşım OSINT’in **Int**elligence başlığını karşılamaz. OSINT, belirli bir birey veya grup tarafından verilen, belirli bir kararı desteklemek amacıyla yapılan analitik bir çalışmadır. Açık kaynak bilgileri bulduktan sonra anlamlı bir veri ve bilgi ortaya çıkartmalıdır. Veri bilimcilerin ham veriyi (raw data) işledikten sonra çıkan anlamlı verileri gibi bir süreci vardır, çalışma sonunda veri anlamlı bir veri olur. (Cooked Data)

## OSINT Kaynakları ve Metodolojisi

OSINT’ın konsept olarak ne olduğunu ve olmadığını anladığımıza göre OSINT içerisindeki başlıkları, kaynakları ve kullanım alanlarına basit örnekler ile bakalım.

### Metodoloji

Izleyeceğimiz yol her ne kadar yaptığınız araştırmaya göre değişiklik gösterse de temelde 4 ana soruyu cevaplayarak ilerleyebilirsiniz.

- Ne biliyorum?
  - Bildiklerini anlat, tarif et ve listele.
- Bildiklerim ne anlama geliyor?
- Neyi bilmem gerekiyor?
- Nasıl bulabilirim

### OSINT Kaynakları

Yapmak istediğiniz araştırma kapsamına ve hedefinize göre değişiklik gösterse de en çok kullanacağınız veriler/bilgiler şunlardır,

- Metadata
- Social Media
- Online Topluluklar/ Forumlar
- Email Adresleri
- Usernames
- Kişi Arama Motorları
- Telefon Numaraları
- Online Haritalar

### OSINT Araçları

OSINT uygularken her ne kadar araçlara ihtiyacınız olmasa da bazı durumlarda özel siteler veya araçsız ilerleyemezsiniz. Bazen de gerçekten işinizi kolaylaştırabilen araçlar vardır. Kullanabileceğiniz araçların listesini tutan birkaç örnek,

- [OSINT Framework](https://osintframework.com/)
  - Insanların ücretsiz OSINT kaynakları bulmasına yardımcı olmak için kurulmuş bir site.
- [Awesome OSINT - Github](https://github.com/jivoi/awesome-osint)
  - Açık kaynak istihbarat araçları ve kaynaklarının derlenmiş bir listesi.
- Bu bağlantı koleksiyonları
  - [The Ultimate OSINT Collection](https://start.me/p/DPYPMz/the-ultimate-osint-collection)
  - [SANS OSINT Summit 2022](https://start.me/p/1kBrw9/sans-osint-2022)
  - [NCSO Resources](https://start.me/p/BnrMKd/01-ncso)
  - [FAROS OSINT Rresources](https://start.me/p/1kvvxN/faros-osint-resources)

Bu koleksiyonlar birçok bağlantı içeriyor ve birçoğu muhtemelen karşınıza çıkmış olsa da içerisinde niş ve daha az bilinen siteleri bulabileceğiniz güzel listeler barındırıyor.

## OSINT Kullanım Alanları ve Örnekleri

Şu ana kadar OSINT’in ne kadar büyük bir alanı kapsadığını ve önemini anlamışsınızdır. Aynı şekilde devletler ve özel kurumlarda bunun farkındadır. Bu sebep ile de özel departmanlar ve birimler kurmuştur. Neredeyse tüm G20 ülkelerinin OSINT özelinde bilinen bir kurumu, departmanı veya birimi vardır.

Özel kurumlardan örnek vermek gerekirse, en güzel örnek Walt Disney şirketidir. Disney’in Küresel Güvenlik Departmanını vardır ve içerinde Küresel İstihbarat ve Tehdit Analizi birimi bulunur. Burada savaşlar, deniz yetki alanları, jeopolitik ve itibar riskleri, uluslararası terörizm, aktivizm, kültürel eğilimler ve siber güvenlik konularında araştırmalar yapar. Bulguları ile Disney Cruise Gemileri ve Disneyland başta olmak üzere tüm şirkete risk ve fırsatlar için yönlendirmeler sunar.

Bu tür kullanımların dışında genelde Gazeteciler, Araştırmacılar ve Güvenlik Uzmanları tardından farkı amaçlar için de kullanır. Bakmanızı tavsiye ettiğim kısa bir liste,

- [Case Studies - bellingcat](https://www.bellingcat.com/category/resources/case-studies/)
- [Krebs on Security](https://krebsonsecurity.com/)
- [NixIntel](https://nixintel.info/)
- [Offensive OSINT](https://www.offensiveosint.io/)
- [OSINT Curious](https://osintcurio.us/)
- [Secjuice](https://www.secjuice.com/)
- [Open Source Int](https://www.osintme.com/index.php/category/open-source-intelligence/)
- [Attack Surface – SwordSec](https://swordsec.com/attack-surface/)
- [Sector035](https://sector035.nl)

OSINT’in ne olduğunu, neden yapıldığını, kimler tarafından yapıldığı ve nasıl yapıldığı hakkında genel bir fikir sahibi olmuşsunuzdur. Toparlamak gerekirse OSINT, açık kaynaklardan elde edilebilecek her türlü bilgiyi kapsar. Bu bilginin elde edilmesinde ise herhangi bir tür casusluk veya illegal yöntemleri kullanılmaz.

## Kaynak[^2]

- <https://medium.com/@leventd/quiztime-random-osint-challenge-11-abc5ea122597>
- <https://www.bellingcat.com/resources/2021/11/09/first-steps-to-getting-started-in-open-source-research/>
- <https://www.irongeek.com/i.php?page=videos/circlecitycon2018/circle-city-con-50-304-a-very-particular-set-of-skills-geolocation-techniques-for-osint-and-investigation-chris-kindig>
- <https://www.ohchr.org/Documents/Publications/OHCHR_BerkeleyProtocol.pdf>
- <https://sector035.nl/articles>
- <https://www.osintdojo.com/resources/>
- <https://nixintel.info/osint/20-questions-quiztime-25th-november-2019/>
- <https://www.uk-osint.net/>
- <https://infosecwriteups.com/>

[^1]: First published here [Levent's Turkcell Geleceği Yazanlar](https://gelecegiyazanlar.turkcell.com.tr/blog/osint-acik-kaynak-istihbarata-giris-1).
[^2]: [Banner Resim kaynağı](https://www.infinitumit.com.tr/osint-nedir-en-yaygin-kullanilan-osint-araclari/)