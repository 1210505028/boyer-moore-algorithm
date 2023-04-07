# boyer-moore-algorithm
## Nedir Ve Niçin Kullanılır?
**Boyer-Moore algoritması**, bir metin içinde belirli bir deseni arama algoritmasıdır. Bu algoritma, 1977'de Robert S. Boyer ve J Strother Moore tarafından geliştirilmiştir. **Boyer-Moore algoritması**, diğer arama algoritmalarından farklı olarak, desenin sağdan sola doğru tarama yaparak karşılaştırma yapmasını sağlar. Bu, metindeki harf sayısını azaltarak, arama süresini kısaltır. Ayrıca, Boyer-Moore algoritması, aranan desende tekrar eden karakterler olduğunda, bu tekrar eden karakterleri baz alarak aramayı hızlandırır. Bu algoritma, özellikle büyük metin dosyalarında veya internet tarayıcılarında kullanılan bir arama algoritmasıdır. Ancak, belirli durumlarda diğer algoritmalardan daha yavaş çalışabilir. 

**Boyer-Moore algoritması**, önceden işlem yapılan iki tabloya dayanır: önek tablosu (bad character table) ve sonek tablosu (good suffix table). Bu tablolar, desenin farklı parçalarının metindeki eşleşme durumlarını önceden hesaplar. Algoritma, desenin son karakteriyle metindeki karakterleri karşılaştırarak ilerler ve uyumsuzluk durumunda tablolardan elde ettiği bilgileri kullanarak ileri atlayarak tekrar arama yapar. 

En iyi, en kötü ve ortalama çalışma sınırları, desen ve metin uzunluğuna ve desen içerisindeki karakterlerin benzersizliğine bağlıdır.

**En iyi durumda**, Boyer-Moore algoritması O(n/m) zaman karmaşıklığına sahip olabilir. Bu durumda, metindeki her karakter eşleşme olacak ve desenin sonuna kadar arama yapmak gerekmez.

**En kötü durumda** Boyer-Moore algoritmasının zaman karmaşıklığı O(mn)'dir, burada m desenin uzunluğunu, n ise metnin uzunluğunu temsil eder. En kötü durum senaryosunda, desenin metindeki her karakterle eşleşmediği durumlarda kötü karakter önek tablosu (bad character table) sayesinde deseni metindeki karakterle hizalayarak atlayarak aramaya devam eder. Ancak, metindeki her karakter desenin son karakteri olursa, her seferinde sadece bir karakter atlanır ve bu durumda da sonek tablosu (good suffix table) kullanılarak arama hızlandırılır.Bu nedenle, Boyer-Moore algoritması, diğer desen eşleştirme algoritmalarından daha hızlı çalışır ve özellikle uzun metinler üzerinde yüksek performans gösterir.

**Ortalama durumda**, Boyer-Moore algoritmasının zaman karmaşıklığı O(n+m) olarak tahmin edilir. Ancak, desendeki benzersiz karakterlerin sayısı ve desenin uzunluğu gibi faktörlere bağlı olarak değişebilir.

Matematiksel ve asimptotik analizler yaparak, en iyi durumda n/m, en kötü durumda nm ve ortalama durumda n+m karmaşıklığına sahip olan Boyer-Moore algoritmasının çalışma sınırları belirlenebilir. <br/><br/>
<img src="https://github.com/1210505028/boyer-moore-algorithm/blob/main/boyer-moore.png" width="auto">

