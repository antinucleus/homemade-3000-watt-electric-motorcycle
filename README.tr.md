[![en](https://img.shields.io/badge/Readme-en-blue.svg)](https://github.com/antinucleus/homemade-3000-watt-electric-motorcycle/blob/master/README.md)

# El Yapımı 3000 Watt Elektrikli Motor

> Bu doküman, 2024 Ağustos-Eylül aylarında yaptığım 3000 watt elektrikli motorun genel özetini içermektedir. İlerleyen süreçte dökümana daha detaylı bilgiler eklenecektir.

<h4 align="center">
  Proje Özeti Videosu
</h4>

<div align="center">
  <a href="https://www.youtube.com/watch?v=YHWjSGBKVd8">
    <img src="https://img.youtube.com/vi/YHWjSGBKVd8/0.jpg" width="400" />
  <a/>
</div>


## Giriş

Önceden elektrikli ve benzinli motorlar kullanmıştım. Benzinli motorların fiyatları yüksek olduğu için elektrikli ve gücü 3000 watt olan motorları araştırmaya başladım. 3000 watt elektrikli motor fiyatları 1.500$ ile 2.500$ arasında değişiyordu.

Elektrikli motor fiyatları da yüksek olduğundan, 3000 watt gücünde bir elektrikli motoru kendim yapıp yapamayacağımı düşündüm ve kabaca bir maliyet hesaplaması yaptım.Hesabıma göre, motorun tasarımı ve el işçiliği bana ait olacak şekilde maliyet
yaklaşık 750$ civarında olacaktı. Hem kendimi geliştirmek hem de fikirlerimin sonuca ulaştığında hissettiğim mutluluk beni motive etti ve motoru yapma kararı aldım.  Birkaç başlık altında süreci genel olarak anlatacağım.

## Tasarım Aşaması

Motorun tasarım kısmında ana odağım motor şasesi oldu. Bu kısmı en basit haliyle, belirli bir yükü taşıyacak ve piyasada bulunan malzemeleri kullanabileceğim şekilde tasarlayıp, geri kalan yerleri üzerine ekleyerek gittim. Sadece şase tasarımı
üzerine yoğunlaştımdan koltuk, ayna, far, sinyal, yan ayak gibi parçalar için tasarım yapmadım.

Yaklaşık 10 gün kadar tasarım ile uğraştıktan sonra 3 farklı model çıkardım. İlk modeli kaynak yapma açısından daha kolay olacağını düşündüğüm kutu profiller ile tasarladım. Ancak göze hoş gelmediği için tamamlamadım ve diğer tasarımlarda
boru profil ile devam ettim.Son tasarıma karar verdikten sonra, piyasada bulabileceğim boru profil et kalınlıklarına göre seçim yaptım ve boru profillere ne kadar yük bineceğini hesapladım. 

### Mekanik

- Tasarımı boru profillerle yaptığım için, profillere büküm vermek adına iki seçeneğim vardı. İlki, büküm yerlerini dirseklerle birleştirip birbirine kaynatmak, diğeri ise tasarıma uygun şekilde boruları bir boru bükümcüsüne büktürmekti.
  İlk seçenek zahmetli olacağı için boruları tasarıma uygun olarak büktürdüm.

- Direksiyon mili için, şasede kullandığım borulara göre et kalınlığı daha fazla olan bir boru profil seçtim. Direksiyon miline bağlanacak gidonu furş takımıyla sabitlemem gerekiyordu. Bu nedenle, direksiyon miline, istediğim ölçülere ve
  furş takımı somununun dişlerine uygun şekilde dış diş açtırdım.

- Motorun arka tekerleği için seçtiğim elektrik motorunun jant ebatına uygun bir ön takım almam gerekiyordu. Bu parçayı sıfır almak yerine, hurdacılardan temin etmeyi tercih ettim.

### Elektronik

- Bu aşamada öncelikle piyasada 3000 watt gücündeki elektrik motorlarını (bu tür motorlar "Hub Motor" olarak adlandırılır) ve bu motorlara uygun hub motor sürücülerini araştırdım. Hub motoru buldum ancak Türkiye'de satılan sürücüler,
  3000 watt hub motorun ihtiyaçlarını karşılayacak özellikte olmadığı için, sürücüyü Çin'den sipariş ettim (gümrük yönetmeliği güncellemesinden önce).

- Bu motor sürücüsü, 48 - 72 Volt aralığında çalışabildiği için, sistemi 72 Volt ile sürülecek şekilde yapılandırdım. Bunun için 6 adet 12V - 24 Ah akü kullandım. Ayrıca, motorda 12V ile çalışacak bileşenler için bir
  72V - 12V düşürücü (DC/DC converter) tercih ettim.

- Hız ve akü seviyesi göstergesi için ESP32, 1.44 inç OLED ekran ve akü seviyesini ölçmek amacıyla bir voltaj bölücü devresi kullandım.

- Motor sinyalleri normalde sinyal flaşörü ile analog olarak kontrol edilebilirdi. Ancak motor için kullandığım sinyaller yüksek watt çektiğinden ve ESP32'yi zaten sistemde kullanacağım için, sinyalleri bir röle yardımıyla kontrol ettim.

### Yazılım

- Voltaj bölücü devreden gelen verilerle akü seviyesini göstermek ve sinyalleri kontrol etmek için gerekli kodun yazılması. Buna ek olarak, sistemi geliştirmek adına motorun uzaktan kontrol edilmesi ve konum takibi gibi özellikler eklemeyi
  planlıyorum.


## Yapım Aşaması

- Büktürdüğüm boru profilleri kaynatıp şaseyi 4 gün içinde tamamladıktan sonra, motor sürücüsünü ve aküleri bağlayarak gece vakti bir deneme sürüşü yaptım. Heyecan verici bir sürüştü çünkü en temel ekipmanlardan olan fren ve far yoktu.
  Sürüşten önce bunun hesabını yapmamıştım ama motor, tahminimin çok üzerinde bir ivmelenme ile hızlanıyordu. Bu ivmelenmenin sebebi olarak, hub motor gücü, sürücünün sağlayabildiği maksimum akım değeri ve şasenin yalnızca iskelet olarak
  yapılmış olması gibi sebepler sayılabilir. Dört günde tamamlanan iskelet, motorun %20'si bile değildi. Asıl uğraş bu aşamadan sonra başladı. Sonraki aşamalarda uzun ve yorucu olan, ama kısaca özetleyeceğim adımlar şunlardı:

  - Direksiyon milinin açısının yeniden verilmesi
  - Gerekli yerlere sac ekleme
  - Yan ayak yapımı
  - Arka fren teli sabitleme aparatı yapımı
  - Oturma minderi yapımı
  - Arka kasa sabitleme yeri yapımı
  - Elektrik tesisatının çekilmesi (Oldukça zahmetli bir işlem)
  - Sinyal, far, stoplar, korna ve aynaların eklenmesi
  - Yan destek ayakları
  - Sürücü için sırt dayama yapılması
  - Arka çamurluk sabitleme aparatı yapımı
  - Akü muhafazası
  - Ön disklerin temizlenmesi, hidrolik hortumunun yenilenmesi, fren kollarının takılması
  - Boyama


## Yapım Aşamasındaki Hatalar

- Direksiyon milini tutan destek parçasını yatayda 60 derece açıyla tasarlamıştım. Ancak bunu yaparken, yatayda 60 derece yerine 45 derece açı bırakacak şekilde parçayı kestim. Aradaki 15 derecelik fark nedeniyle, hem motor çok uzun olmuştu
  hem de tümsek veya çukurlardan geçerken yükün çoğu, ön amortisör yerine direksiyon milinin bağlı olduğu parçaya biniyor ve şaseyi esnetiyordu. Direksiyon milinin duruşu, chopper motorlarının direksiyon milleri gibi olmuştu; sürüşü zevkliydi
  ama güvenilir değildi. Bu yüzden direksiyon milini tutan parçayı kesip, milin yatayda 60 derece olmasını sağlayacak parça ile yeniden kaynattım.

- Tasarımı yaparken, ön takımın amortisörünü tamamen modellemek yerine, onu temsil eden bir şekil eklemiştim. Ancak, 60 derece eğimle direksiyon milini tutacak olan demiri kaynattığım için, direksiyon milini yerine takınca şasedeki orta desteğe
  lastik değmeye başladı. Orta destek demirini kesip içe almama rağmen bu mesafeyi kurtarmadı, bu yüzden ön takımı ters olarak taktım. İlerleyen süreçte bu durum, ön çamurluğu eklememi engelledi.

- Motor tasarımında hesaba katmadığım bir diğer konu ise motorun uzunluğu oldu. Standard motorlardan 30 cm daha uzun olduğu için, arka fren kampanasına gidecek tellerin uzunluğu yetmedi. Bu yüzden standart fren telinden daha uzun fren telini
  oraya uygun olacak şekilde keserek o kısmı tamamladım.

- Sürücünün arkasına yaslanabilmesi için amortisörlü bir sırt dayama ekledim. Sonraki aşamada bagajın üzerine koltuk süngerlerini yerleştirdim, ancak süngerlerin kalınlığı fazla olduğu için bagaj tam olarak açılıp kapanmıyordu. Bu yüzden
  sırt dayamayı işlevsiz bırakmak zorunda kaldım.

- Ön kısımda ise sürücünün ayak koyduğu yerin biraz daha geniş olması gerekiyordu.

## Son Durum

Zamanım kalmadığı için tamamlanmayan kısımlar;

- Motorun şu an ön kısmı açık ve oradan çıkan tüm kablolar dağınık olduğu için, buranın kapatılması gerekiyor.
- Oturma kısmının yan kapakları yok, bu kısımların da kapatılması gerekli.
- Ekranda motor hızının gösterilmesi.
- Ön takımı ters taktığım için standart ön çamurluklar uygun olmuyor. Bu yüzden 3D yazıcı ile ön çamurluk basılması gerekiyor.
- Belki ilerleyen zamanlarda, koltuk süngerinin dikdörtgen yerine daha estetik bir şekilde yapılması ve sırt dayamanın tekrar işlev kazanması düşünülebilir.
- Geri vitesle hareket ederken, motorun kendi şaftı etrafında dönüp kablosunu dolamaması için arka salıncak koluna aks kilitleme pulunun sabitlenmesi gerekiyor.
