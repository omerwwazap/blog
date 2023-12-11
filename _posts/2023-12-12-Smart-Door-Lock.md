---
layout: post
title: "[TR] Apartman Giriş Kapılarındaki Güvenlik Sorunları ve Şifrelerin Anlamlı Dünyası"
date: 2023-12-11 01:53 +0200
categories: [Cyber Security, Malware]
tags: [English, Reverse Engineer]     # TAG names should always be lowercase
img_path: /images/2023SmartDoorLock
image:
  path: /0.png
  alt: Bing AI Image Creator (Typo Burglar to Burger)
---

Türkiye'de apartman dış kapı şifreleri genellikle basit ve tahmin edilmesi kolay sayılardan oluşuyor. Bu durum, tahmin edileceği üzere büyük problemler yaratıyor.

En popüler şifreler arasında 1453, 1923, 0571, 1881, 1234, 2580, yer alıyor. Bu şifreler genellikle tarihi, dini veya kültürel anlamlar taşıyor. Örneğin, 1453 İstanbul'un Fethinin, 1923 Cumhuriyet'in İlanının, 1071 Malazgirt Meydan Muharebesinin, 0571 Hz. Muhammed'in doğum yılının gibi konuları simgeliyor.

## Popüler Apartman Kapı Şifreleri

|        Yıllar        | **Anlamları**                                                        | **Not**                        |
|:--------------------:|----------------------------------------------------------------------|--------------------------------|
|       **1453**       | İstanbul'un Fethi'nin                                                | En Sık Görülen Şifrelerdendir. |
|       **2023**       | Cumhuriyet'in 100. yılının                                           |                                |
|       **1071**       | Malazgirt Meydan Muharebesi'nin gerçekleştiği yıl                    |                                |
|       **0571**       | Hz. Muhammed'in doğum yılıdır                                        |                                |
|       **2071**       | Türklerin Anadolu'ya gelişin bininci yılı                            |                                |
|       **1881**       | Mustafa Kemal Atatürk'ün doğum yılıdır                               | En Sık Görülen Şifrelerdendir. |
|       **1919**       | Milli mücadelenin ilk adımlarının atıldığı dönem                     |                                |
|       **1920**       | Türkiye Cumhuriyeti'nin temellerinin atıldığı yıldır                 |                                |
|       **1234**       | Basit ve kolayca hatırlanabilir bir şifre                            | En Sık Görülen Şifrelerdendir. |
|       **1299**       | Osmanlı Devleti'nin kuruluş yılı                                     |                                |
|       **2580**       | 1234 yapmak istemediği için key pad'de üstten alta yazılan şifredir  | En Sık Görülen Şifrelerdendir. |
|       **5789**       | Pad üstünde üçgen çizme, Android cihazlardaki kaydırma şifreler gibi |                                |
|       **3698**       | Pad üstünde, Android cihazlardan,  ters L dir                        |                                |
| **8181, 2323, 6161** | Şehirlerin plaklarıdır                                               |                                |
|       **1923**       | Türkiye Cumhuriyeti'nin kuruluş yılı                                 | En Sık Görülen Şifrelerdendir. |
|       **1938**       | Mustafa Kemal Atatürk'ün vefat ettiği yıl                            |                                |

### Ek Bilgiler

- **İzmir**: 1881 ve 1938'dir muhtemelen
- **Ankara**: Normal şifreler olmuyorsa 1402 denenebilir.
- **Trabzon**: 6161 genelde çalışır.
- Eğer 5 veya 6 haneli şifre isteniyor ise, **00[şifre] ve 99[şifre]** olabilir.

Bunların hiç birisi olmadıysa çok çok nadir bir durumdasınız demektir. Ancak hala şansınız var.

- Şehrin plaka kodu + apartman ya da ev sahibinin memleketinin plaka kodu.
- Bunların hiçbiri olmaz ise, binanın yapım yılı olabilir.

## Master Şifrelerin Varsayılan Olarak Bırakılması

Apartman dış kapı şifrelerinin güvenliğini daha da düşüren bir faktör ise master şifrelerin varsayılan olarak bırakılması. Master şifre, apartman yöneticisinin veya apartman sakinlerinin şifrelerini değiştirmelerine olanak tanıyan bir şifredir.

Türkiye'de birçok apartmanda master şifrelerin varsayılan olarak bırakıldığı düşünüyorum. Eğer Ekşi Sözlük, Teknoloji Forumları ve Twitter a bakarsanız bunun gerçekten büyük bir sorun olduğunu görebilirsiniz. Bu durum, hırsızların apartmanın master şifresini bularak, apartmanın şifresini bile bilmeden binaya girmesini olanak tanıyor.

### Popüler Master Şifreleri

|      **Şifreler**     |              **Marka**             |
|:---------------------:|:----------------------------------:|
| #*654321 /  #654321#  |                Genel               |
|  #*123456 /  #123456# |                Genel               |
|         66688*        |         Kale Geçiş Kontrol         |
|        *999999#       | Generic RFID/Şifre Kapıları (P110) |
|       *#223344#       |                  -                 |
|        #*654321       |              netelsan              |

**"*"** ve **"#"** kullanımı markaya göre değişmektedir.

## Alınabilecek Önemler - DÜZENLENECEK

Apartman dış kapılarının güvenliğini artırmak için alınabilecek bazı önlemler şunlardır:

- **Master şifreler değiştirilmelidir**. Master şifreler değiştirilirken, basit ve tahmin edilmesi kolay sayılar kullanılmamalıdır.
- **RFID/NFC Teknolojileri**. Akıllı kartlar veya cep telefonları aracılığıyla erişim sağlayan sistemler, şifrelerin zayıflıklarını ortadan kaldırabilir. Ancak burada başka sorunlar ortaya çıkıyor.
  - Müthiş bir Youtube kanalı olan [Lock Picking Lawyer](https://www.youtube.com/@lockpickinglawyer/search?query=keypad) hesabını açıp "KeyPad" aratıp bir kaç video izleyin.

- Tavsiye Edilen ama bence işe yaramayan bir yöntem var.
  - *Her daire için özel şifreler belirlenmelidir*. Bunun efektif olmasının nedeni birisinin yukarı bahsettiğim bilindik şifrelerden birisini kullanma ihtimali %100.

Şifre kullanımının kötü kullanımı bu cihazları tasarlayan şirketler tarafından bilinmektedir. Bu sebep ile bu şifreler ile dalga geçen reklamlar görülebilir.
[Resim]

## Problem Sadece Dış Kapılar Değil

Bu şifreler sadece bina/ev kapıları için değil Kurum, Kuruluş ve Hastane gibi bina içerisinde bulanan kapılar için de geçerlidir.

Bakınız Twitter'dan örnekler (embedded postlar Twitter X olduğundan beri yavaş yükleniyor),

- <blockquote class="twitter-tweet"><p lang="tr" dir="ltr">Hastanede böyle bi kapı görürseniz tereddütsüz 1453’ü tuşlayabilirsiniz, kapı açılmadıysa yanlış tuşa basmışsınızdır tekrar 1453’ü deneyin... <a href="https://t.co/8W45tijXU0">pic.twitter.com/8W45tijXU0</a></p>&mdash; Mehmet Batuhan Örs (@mbatuhanors) <a href="https://twitter.com/mbatuhanors/status/1257379949331300353?ref_src=twsrc%5Etfw">May 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
- <blockquote class="twitter-tweet"><p lang="tr" dir="ltr">Hmm düzcedeyiz bilin bakalım kapı şifresi ne? 🤔 <a href="https://t.co/T1MhtuFPlY">pic.twitter.com/T1MhtuFPlY</a></p>&mdash; Düzce Muhtarı (@duzcemuhtari) <a href="https://twitter.com/duzcemuhtari/status/1186037456275214337?ref_src=twsrc%5Etfw">October 20, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## Bonus - Komik Marka Paylaşımı

![Image](2.png) _multitek_elektronik_

## Sonuç

Apartman dış kapıları, hırsızlar için kolay bir hedeftir. Bu riskleri azaltmak için, apartman sakinlerinin ve yöneticilerinin daha dikkatli olması gerekir. Bu önlemlerin alınması, apartmanların güvenliğini önemli ölçüde artırabilir.

Kısacası, aşağıdaki noktalara dikkat edilmeli

- Apartman dış kapı şifreleriniz basit ve tahmin edilmesi kolay sayılardan oluşmamalıdır.
- Master şifreler kesinlikle değiştirilmelidir.
- Her daire için özel şifreler belirlenebilir.

Note: Banner prompt for Bing AI Image Creator: A burger with arms as a french-fry is using an apartments keypad to enter the entrance code to the building. a random password at an apartment entrance. on the entrance keypad.