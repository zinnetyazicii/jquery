# jQuery Event

### 1. click
  - İşlev, kullanıcı HTML öğesine tıkladığında yürütülür.
### 2. dblclick	
  - İşlev, kullanıcı HTML öğesine çift tıkladığında yürütülür:
### 3. mouseenter	
  - İmleci öğenin üzerine getirdiğimizde.
### 4. mouseleave	 	
   - İmleci öğeden kaldırdığımızda.
### 5. mousedown 
   - Kullanıcı fare düğmesine bastığında tetiklenir.
### 5. mouseup
   - Kullanıcı fare düğmesini bıraktığında tetiklenir.
### 6. hover   
   - Yöntem iki işlev alır ve ve yöntemlerinin hover()bir birleşimidir .mouseenter()mouseleave()
   - İlk işlev, fare HTML öğesine girdiğinde yürütülür ve ikinci işlev, fare HTML öğesinden ayrıldığında yürütülür
### 7. focus
   - İşlev, form alanı odaklandığında yürütülür
### 8. blur
   - İşlev, form alanı odağı kaybettiğinde yürütülür
### 9. on
   - Bir öğeye birden çok olay işleyicisi ekler
   - ` $("p").on({
  mouseenter: function(){
    $(this).css("background-color", "lightgray");
  },
  mouseleave: function(){
    $(this).css("background-color", "lightblue");
  },
  click: function(){
    $(this).css("background-color", "yellow");
  }
}); 


# jQuery Effects

### 1. hide() 
  - HTML öğelerini  gizleyebilir.
### 2. show()
  -  HTML öğelerini gösterebilirsiniz.
### 3. toggle()
  - Yöntemle bir öğeyi gizleme ve gösterme arasında da geçiş yapabilirsiniz .Gösterilen öğeler gizler ve gizli öğeler gösterilir.
### 4. fadeIn()
  - gizli bir öğede kaybolmak için kullanılır.
  -  `$(selector).fadeIn(speed,callback);`
  -  İsteğe bağlı hız parametresi, etkinin süresini belirtir. Şu değerleri alabilir: "yavaş", "hızlı" veya milisaniye.
### 5. fadeOut()
  - görünür bir öğeyi karartmak için kullanılır.
  - `$(selector).fadeOut(speed,callback);`
  - İsteğe bağlı hız parametresi, etkinin süresini belirtir. Şu değerleri alabilir: "yavaş", "hızlı" veya milisaniye.
### 6. fadeToggle()
  - yöntemi ve  fadeIn() ve fadeOut() arasında geçiş yapar
  - `$(selector).fadeToggle(speed,callback);` 
  - İsteğe bağlı hız parametresi, etkinin süresini belirtir. Şu değerleri alabilir: "yavaş", "hızlı" veya milisaniye.
### 7. fadeTo()
  - belirli bir opaklığa (0 ile 1 arasındaki değer) solmaya izin verir.
  - `$(selector).fadeTo(speed,opacity,callback);`
  - Gerekli hız parametresi, etkinin süresini belirtir. Şu değerleri alabilir: "yavaş", "hızlı" veya milisaniye.Yöntemdeki gerekli opaklık parametresi, fadeTo()belirli bir opaklığa geçişi belirtir (0 ile 1 arasındaki değer).
### 8. slideDown()
  -  bir öğeyi aşağı kaydırmak için kullanılır.
  - `$(selector).slideDown(speed,callback);` 
  - İsteğe bağlı hız parametresi, etkinin süresini belirtir. Şu değerleri alabilir: "yavaş", "hızlı" veya milisaniye.
### 9. slideUp()
  - bir öğeyi yukarı kaydırmak için kullanılır.
  - `$(selector).slideUp(speed,callback);`
  - İsteğe bağlı hız parametresi, etkinin süresini belirtir. Şu değerleri alabilir: "yavaş", "hızlı" veya milisaniye.
### 10. slideToggle()
  - slideDown() ve slideUp() arasında geçiş yapar 
  - `$(selector).slideToggle(speed,callback);`
  - İsteğe bağlı hız parametresi şu değerleri alabilir: "yavaş", "hızlı", milisaniye.
### 11.  animate()
  - özel animasyonlar oluşturmak için kullanılır.
  - `$(selector).animate({params},speed,callback);`
  - Gerekli params parametresi, canlandırılacak CSS özelliklerini tanımlar.
  - İsteğe bağlı hız parametresi, etkinin süresini belirtir. Şu değerleri alabilir: "yavaş", "hızlı" veya milisaniye.
  - İsteğe bağlı geri arama parametresi, animasyon tamamlandıktan sonra yürütülecek bir işlevdir.
  - `$("button").click(function(){
  $("div").animate({left: '250px'});
}); `
  - `$("button").click(function(){
  $("div").animate({
    left: '250px',
    height: '+=150px',
    width: '+=150px'
  });
}); `

### 12.  stop() 
  -  bir animasyonu veya efekti bitmeden durdurmak için kullanılır.
  - `(selector).stop(stopAll,goToEnd);`
  - İsteğe bağlı stopAll parametresi, animasyon kuyruğunun da temizlenip temizlenmeyeceğini belirtir. Varsayılan yanlıştır; bu, yalnızca etkin animasyonun durdurulacağı ve daha sonra sıraya alınmış animasyonların gerçekleştirilmesine izin verileceği anlamına gelir.
  - İsteğe bağlı goToEnd parametresi, geçerli animasyonun hemen tamamlanıp tamamlanmayacağını belirtir. Varsayılan yanlıştır.
  - Bu nedenle, varsayılan olarak stop()yöntem, seçili öğe üzerinde gerçekleştirilen geçerli animasyonu öldürür.
  - `$(document).ready(function(){
  $("#flip").click(function(){
    $("#panel").slideDown(5000);
  });
  $("#stop").click(function(){
    $("#panel").stop();
  });
});`
  
### 13.  Callback 
  - JavaScript ifadeleri satır satır yürütülür. Ancak efektlerle, efekt bitmese bile bir sonraki kod satırı çalıştırılabilir. Bu hatalar oluşturabilir.
  - Bunu önlemek için bir geri arama işlevi oluşturabilirsiniz.
  - Geçerli efekt bittikten sonra bir geri arama işlevi yürütülür.Tipik sözdizimi: `$( selector ).hide( hız,geri arama );`
  - `$("button").click(function(){
  $("p").hide("slow", function(){
    alert("The paragraph is now hidden");
  });
});`
### 14.  Chaining (Zincirleme)
  - Şimdiye kadar jQuery deyimlerini teker teker (birbiri ardına) yazıyorduk.Ancak, aynı eleman(lar) üzerinde birbiri ardına birden fazla jQuery komutu çalıştırmamıza izin veren zincirleme adı verilen bir teknik vardır.
  - İpucu: Bu şekilde, tarayıcıların aynı öğeyi/elemanları bir kereden fazla bulması gerekmez.
  - Bir eylemi zincirlemek için, eylemi önceki eyleme eklemeniz yeterlidir.
  - Aşağıdaki örnek css(), slideUp(), ve slideDown() yöntemlerini birlikte zincirler. "p1" öğesi önce kırmızıya döner, sonra yukarı kayar ve sonra aşağı kayar:
  - `$("#p1").css("color", "red").slideUp(2000).slideDown(2000);`
# HTML
## 1.Get

### 1.1. text()
  - Seçili öğelerin metin içeriğini ayarlar veya döndürür
  -` $("#btn1").click(function(){
  alert("Text: " + $("#test").text());
});`
### 1.2. html()
  - Seçilen öğelerin içeriğini ayarlar veya döndürür (HTML etiketleri dahil)
  - `$("#btn2").click(function(){
  alert("HTML: " + $("#test").html());
});`
### 1.3. val()
  - Form alanlarının değerini ayarlar veya döndürür.
  - `$("#btn1").click(function(){
  alert("Value: " + $("#test").val());
});`
### 1.4. attr()
  - Öznitelik değerlerini elde etmek için kullanılır.
  - `$(document).ready(function(){
  $("button").click(function(){
    alert($("#w3s").attr("href"));
  });
});`
  - `<p><a href="https://www.w3schools.com" id="w3s">W3Schools.com</a></p>` 
  - https://www.w3schools.com çıktısını veririr
## 2. Set
### 2.1 text()
 - Seçili öğelerin metin içeriğini ayarlar veya döndürür
 - `$("#btn1").click(function(){
  $("#test1").text("Hello world!");
});`
### 2.2 html()
 - Seçilen öğelerin içeriğini ayarlar veya döndürür (HTML işaretlemesi dahil)
 - `$("#btn2").click(function(){
  $("#test2").html("<b>Hello world!</b>");
});`
### 2.3 val()
 - Form alanlarının değerini ayarlar veya döndürür 
  - `$("#btn3").click(function(){
  $("#test3").val("Dolly Duck");
})`
### 2.4 attr()
  - öznitelik değerlerini ayarlamak/değiştirmek için de kullanılır.
  - `$("button").click(function(){
  $("#w3s").attr("href", "https://www.w3schools.com/jquery/");
});`
## 3. Add
### 3.1. append()
  - Seçilen öğelerin sonuna içerik ekler  ( öğenin içine içeriğin eklenmesidir )
### 3.2. prepend()
  - Seçilen öğelerin başına içerik ekler ( öğenin içine içeriğin eklenmesidir )
### 3.3. after()
  - Seçilen öğelerden sonra içerik ekler ( öğenin dışına içeriğin eklenmesidir )
### 3.4. before()
  - Seçili öğelerden önce içerik ekler  ( öğenin dışına içeriğin eklenmesidir )
## 4. Remove Elements/Content
### 4.1. remove()
  - Seçili öğeyi (ve onun alt öğelerini) kaldırır
### 4.2. empty()
  - Seçili öğeden alt öğeleri kaldırır.Seçili öğe kaldırılmaz. içerik silinir
## 5. Get and Set CSS Classes
### 5.1. addClass()
  - Seçili öğelere bir veya daha fazla sınıf ekler
### 5.2. removeClass()
  - Seçili öğelerden bir veya daha fazla sınıfı kaldırır
### 5.3. toggleClass()
  - Seçili öğelerden sınıf ekleme/çıkarma arasında geçiş yapar
  - `$("button").click(function(){
  $("h1, h2, p").toggleClass("blue");
});`
### 5.4. css()
  - Stil niteliğini ayarlar veya döndürür
  - Belirtilen bir CSS özelliğinin değerini döndürmek için aşağıdaki sözdizimini kullanın
  - `css("propertyname"); ( $("p").css("background-color"); )` ( İLK eşleşen öğenin arka plan rengi değerini döndürür)
  - elirtilen bir CSS özelliğini ayarlamak için aşağıdaki sözdizimini kullanın:
  -`css("propertyname","value");`
  - `$("p").css("background-color", "yellow");`
  - *Birden Çok CSS Özelliği Ayarla*
  - `css({"propertyname":"value","propertyname":"value",...});`
  - eşleşen TÜM öğeler için bir arka plan rengi ve bir yazı tipi boyutu ayarlayacaktır:
  - `$("p").css({"background-color": "yellow", "font-size": "200%"});`
## 6. Dimensions(Hacim-Boyut)
![w3schools](https://www.w3schools.com/jquery/img_jquerydim.gif)

### 6.1. width()
  - bir öğenin genişliğini ayarlar veya döndürür (padding, border ve margin hariç).
### 6.2. height()
  - bir öğenin yüksekliğini ayarlar veya döndürür (padding, border vemargin hariç).
### 6.3. innerWidth()
  - bir öğenin genişliğini döndürür (padding içerir).
### 6.4. innerHeight()
  - bir öğenin yüksekliğini döndürür (padding içerir). 
### 6.5. outerWidth()
  - bir öğenin genişliğini döndürür (padding ve border içerir).
### 6.6. outerHeight()
  - bir öğenin yüksekliğini döndürür (padding ve border içerir).
### 6.7. outerWidth(true)
  - bir öğenin genişliğini döndürür (padding, border ve margin içerir).
### 6.8. outerHeight(true) 
  - bir öğenin yüksekliğini döndürür (padding, border ve margin içerir).
  - `$(document).ready(function(){
  $("button").click(function(){
    var txt = "";
    txt += "Document width/height: " + $(document).width();
    txt += "x" + $(document).height() + "\n";
    txt += "Window width/height: " + $(window).width();
    txt += "x" + $(window).height();
    alert(txt);
  });
});`
# Traversing (Gezinme)
## 1. parent()
  - seçilen öğenin doğrudan üst öğesini döndürür.
## 2. parents()
  - belgenin kök öğesine kadar seçili öğenin tüm üst öğelerini döndürür .<html>
## 3. parentsUntil()
  - verilen iki bağımsız değişken arasındaki tüm üst öğeleri döndürür.
  - Aşağıdaki örnek, a <span>ile bir <div>öğe arasındaki tüm üst öğeleri döndürür:
  - `$(document).ready(function(){
  $("span").parentsUntil("div");
});`
## 4. children()
  - seçilen öğenin tüm doğrudan alt öğelerini döndürür.
  - her bir öğenin doğrudan çocukları olan tüm öğeleri döndürür
  - `<div><p><p></p></p></div> ` 2 p de child dır
## 5. find()
  - seçilen öğenin alt öğelerini son alt öğeye kadar döndürür.
  - seçilen öğenin alt öğelerini son alt öğeye kadar döndürür.
  - torunları olan tüm öğeleri döndürür
## 6. siblings()
  -  seçilen öğenin tüm kardeş öğelerini döndürür.
## 7. next()
  - seçilen öğenin bir sonraki kardeş öğesini döndürür.
## 8. nextAll()
  - seçilen öğenin sonraki tüm kardeş öğelerini döndürür.
## 9. nextUntil()
  - verilen iki bağımsız değişken arasındaki sonraki tüm kardeş öğeleri döndürür.
## 10. prev()
  - seçilen öğenin bir önceki kardeş öğesini döndürür.
## 11. prevAll()
  - seçilen öğenin önceki tüm kardeş öğelerini döndürür.
## 12. prevUntil()
  - verilen iki bağımsız değişken arasından önceki tüm kardeş öğeleri döndürür.
## 13. first()
  -  belirtilen öğelerin ilk öğesini döndürür.
## 14. last()
  - belirtilen öğelerin son öğesini döndürür.
## 15. eq()
  - seçilen öğelerin belirli bir dizin numarasına sahip bir öğe döndürür.
  - Dizin numaraları 0'dan başlar, bu nedenle ilk öğe 1 değil 0 dizin numarasına sahip olacaktır. Aşağıdaki örnek ikinci <p>öğeyi seçer (dizin numarası 1)
  - `$(document).ready(function(){
  $("p").eq(1);
});`
## 16. filter() 
  - bir ölçüt belirlemenizi sağlar. Kriterlerle eşleşmeyen öğeler seçimden çıkarılır ve eşleşen öğeler döndürülür.
  - `$(document).ready(function(){
  $("p").filter(".intro");
});`
## 17. not()
  -  ölçütlerle eşleşmeyen tüm öğeleri döndürür.
  - İpucu: Yöntem not(), öğesinin tam tersidir filter().
  - Aşağıdaki örnek, <p>"intro" sınıf adına sahip olmayan tüm öğeleri döndürür
  - `$(document).ready(function(){
  $("p").not(".intro");
});`
# AJAX
## 1. load()
  - yöntemi basit ama güçlü bir AJAX yöntemidir.
  - bir sunucudan veri yükler ve döndürülen verileri seçilen öğeye yerleştirir.
  - `$(selector).load(URL,data,callback);`
  - Gerekli URL parametresi, yüklemek istediğiniz URL'yi belirtir.
  - İsteğe bağlı veri parametresi, istekle birlikte gönderilecek bir dizi sorgu dizesi anahtar/değer çifti belirtir.
  - İsteğe bağlı geri çağırma parametresi, yöntem tamamlandıktan sonra yürütülecek bir işlevin adıdır .
  - Aşağıdaki örnek, "demo_test.txt" dosyasının içeriğini belirli bir <div>öğeye yükler
  - `$("#div1").load("demo_test.txt");`
  - Aşağıdaki örnek, "demo_test.txt" dosyasının içindeki id="p1" öğesinin içeriğini belirli bir <div>öğeye yükler
  - `$("#div1").load("demo_test.txt #p1");`
  - load() İsteğe bağlı geri arama parametresi, yöntem tamamlandığında çalıştırılacak bir geri arama işlevini belirtir . Geri arama işlevi farklı parametrelere sahip olabilir:
      - responseTxt- arama başarılı olursa ortaya çıkan içeriği içerir
      - statusTxt- aramanın durumunu içerir
      - xhr- XMLHttpRequest nesnesini içerir
  - Aşağıdaki örnek, load() yöntemi tamamlandıktan sonra bir uyarı kutusu görüntüler. Yöntem başarılı olursa, load()"Harici içerik başarıyla yüklendi!" mesajını görüntüler ve başarısız olursa bir hata mesajı görüntüler:
  - `$("button").click(function(){
  $("#div1").load("demo_test.txt", function(responseTxt, statusTxt, xhr){
    if(statusTxt == "success")
      alert("External content loaded successfully!");
    if(statusTxt == "error")
      alert("Error: " + xhr.status + ": " + xhr.statusText);
  });
});`
## 2. $.get()
  - sunucudan bir HTTP GET isteği ile veri ister.
  - `$.get(URL,callback);`
  - Aşağıdaki örnek $.get(), sunucudaki bir dosyadan veri almak için yöntemi kullanır:
  - `$("button").click(function(){
  $.get("demo_test.asp", function(data, status){
    alert("Data: " + data + "\nStatus: " + status);
  });
});`
## 3. $.post()
  -  bir HTTP POST isteği kullanarak sunucudan veri ister.
  - `$.post(URL,data,callback);`
  - Gerekli URL parametresi, talep etmek istediğiniz URL'yi belirtir.
  - İsteğe bağlı veri parametresi, istekle birlikte gönderilecek bazı verileri belirtir.
  - İsteğe bağlı geri arama parametresi, istek başarılı olursa yürütülecek işlevin adıdır.
  - Aşağıdaki örnek $.post(), istekle birlikte bazı verileri göndermek için yöntemi kullanır:
  - `$("button").click(function(){
  $.post("demo_test_post.asp",
  {
    name: "Donald Duck",
    city: "Duckburg"
  },
  function(data, status){
    alert("Data: " + data + "\nStatus: " + status);
  });
});`
# Misc
### 1. noConflict()
  - diğer komut dosyalarının kullanabilmesi için $ kısayol tanımlayıcısındaki bekletmeyi serbest bırakır.
  - `$.noConflict();
jQuery(document).ready(function(){
  jQuery("button").click(function(){
    jQuery("p").text("jQuery is still working!");
  });
});`
  - Kendi kısayolunuzu da çok kolay bir şekilde oluşturabilirsiniz. Yöntem noConflict(), daha sonra kullanmak üzere bir değişkene kaydedebileceğiniz jQuery'ye bir başvuru döndürür. İşte bir örnek:
  - `var jq = $.noConflict();
jq(document).ready(function(){
  jq("button").click(function(){
    jq("p").text("jQuery is still working!");
  });
});`
### 2. Filtreleme
  -  Giriş alanının değeriyle eşleşen herhangi bir metin değeri olup olmadığını kontrol etmek için her tablo satırında döngü yapmak için jQuery kullanıyoruz. Yöntem , aramayla eşleşmeyen toggle()satırı ( ) gizler . Metni küçük harfe dönüştürmek için DOM yöntemini kullanırız, bu da aramanın büyük/küçük harfe duyarlı olmamasını sağlar (aramada "john", "John" ve hatta "JOHN" kullanımına izin verir) display:none.toLowerCase()
  - tablo filtrele (myInput id listeye tabloya vb verilebilir.)
  - `$(document).ready(function(){
  $("#myInput").on("keyup", function() {
    var value = $(this).val().toLowerCase();
    $("#myTable tr").filter(function() {
      $(this).toggle($(this).text().toLowerCase().indexOf(value) > -1)
    });
  });
});`
<table>
<tr>
    <td>Sıra</td>
    <td>Selector</td>
    <td>Örnek</td>
    <td>Açıklama</td>
</tr>
<tr>
    <td>1</td>
    <td>*</td>
    <td>$("*")</td>
    <td>Tüm Elementler</td>

</tr>
<tr>
    <td>2</td>
    <td>#id</td>
    <td>$("#lastname")</td>
    <td>Idsi lastname olan Elementler</td>

</tr>
<tr>
    <td>3</td>
    <td>.class</td>
    <td>$(".intro")</td>
    <td>classı intro olan tüm Elementler</td>

</tr>
<tr>
    <td>4</td>
    <td>.class,.class</td>
    <td>$(".intro,.demo")</td>
    <td>classı intro veya demo olan tüm Elementler</td>

</tr>
<tr>
    <td>5</td>
    <td>"p"</td>
    <td>$("p")</td>
    <td>Tüm p öğeleri</td>

</tr>
<tr>
    <td>6</td>
    <td>el1,el2,el3</td>
    <td>$("h1,div,p")</td>
    <td>Tüm h1,div ve p elementleri</td>

</tr>
<tr>
  <td>7</td>
  <td>:last	</td>$
  <td>("p:last")</td>
  <td>son p elemanı</tr>

</tr>
<tr>
  <td>8</td>
  <td>:even</td>	
  <td>$("tr:even")</td>
  <td>tüm çift indeksli tr elementleri </tr>
</tr>
<tr>
  <td>9</td>
  <td>:odd</td>	
  <td>$("tr:odd")</td>
  <td>tüm tek indeksli tr elementleri</tr>

</tr> 
<tr>
  <td>10</td>
  <td>:first-child</td>
  <td>$("p:first-child")</td>	
  <td>Ebeveynlerinin ilk çocuğu olan tüm p öğeleri</td>

</tr>
<tr>
  <td>11</td>
  <td>:first-of-type</td>
  <td>$("p:first-of-type")</td>	
  <td>Ebeveynlerinin ilk p öğesi olan tüm p öğeleri</td>

</tr>
<tr>
  <td>12</td>
  <td>:last-child</td>
  <td>$("p:last-child")</td>	
  <td>Ebeveynlerinin son çocuğu olan tüm p öğeleri</td>

</tr>
<tr>
  <td>13</td>
  <td>:last-of-type</td>
  <td>$("p:last-of-type")</td>	
  <td>Ebeveynlerinin son p öğesi olan tüm p öğeleri</td>

</tr>
<tr>
  <td>14</td>
  <td>:nth-child(n)</td>
  <td>$("p:nth-child(2)")</td>	
  <td>Ebeveynlerinin 2. çocuğu olan tüm p öğeleri</td>

</tr>
<tr>
  <td>15</td>
  <td>:nth-last-child(n)</td>
  <td>$("p:nth-last-child(2)")</td>	
  <td>Son çocuktan itibaren ebeveyninin 2. çocuğu olan tüm p öğeleri</td>

</tr>
<tr>
  <td>16</td>
  <td>:nth-of-type(n)</td>
  <td>$("p:nth-of-type(2)")</td>	
  <td>Ebeveynlerinin 2. p öğesi olan tüm p öğeleri</td>

</tr>
<tr>
  <td>17</td>
  <td>:nth-last-of-type(n)</td>
  <td>$("p:nth-last-of-type(2)")</td>	
  <td>Son çocuktan itibaren ebeveyninin 2. p öğesi olan tüm p öğeleri</td>

</tr>
<tr>
  <td>18</td>
  <td>:only-child</td>
  <td>$("p:only-child")</td>	
  <td>Ebeveynlerinin tek çocuğu olan tüm p öğeleri</td>

</tr>
<tr>
  <td>19</td>
  <td>:only-of-type</td>
  <td>$("p:only-of-type")</td>		
  <td>Kendi türünde ebeveyninin tek çocuğu olan tüm p öğeleri</td>

</tr>
 	 	 	 
<tr>
  <td>20</td>
  <td>parent > child</td>
  <td>$("div > p")</td>
  <td>Bir div öğesinin doğrudan çocuğu olan tüm p öğeleri</td>
</tr>
<tr>
  <td>21</td>
  <td>parent descendant</td>
  <td>$("div p")</td>
  <td>Bir div öğesinin soyundan gelen tüm p öğeleri</td>
</tr>
<tr>
  <td>22</td>
  <td>element + next</td>
 <td>$("div + p")</td>
 <td>Her div öğesinin yanındaki p öğesi</td>
</tr>
<tr>
  <td>23</td>
  <td>element ~ siblings</td>
  <td>$("div ~ p")</td>
  <td>div öğesinden sonra görünen tüm p öğeleri</td>
</tr>
 	 	 
<tr>
  <td>24</td>
  <td>:eq(index)</td>
  <td>$("ul li:eq(3)")</td>
  <td>Listedeki dördüncü öğe (dizin 0'dan başlar)</td>
</tr>
<tr>
  <td>25</td>
  <td>:gt(no)</td>
  <td>$("ul li:gt(3)")</td>
  <td>3'ten büyük bir dizine sahip öğeleri listeleyin</td>
</tr>
<tr>
  <td>26</td>
  <td>:lt(no)</td>
 <td>$("ul li:lt(3)")</td>
 <td>3'ten küçük bir dizine sahip öğeleri listeleyin</td>
</tr>
<tr>
  <td>27</td>
  <td>:not(selector)</td>
  <td>$("input:not(:empty)")</td>
  <td>Boş olmayan tüm girdi öğeleri</td>
</tr>
 	 	 
<tr>
  <td>28</td>
  <td>:header</td>
  <td>$(":header")</td>
  <td>Tüm başlık öğeleri h1, h2 ...</td>
</tr>
<tr>
  <td>29</td>
  <td>:animated</td>
  <td>$(":animated")</td>
  <td>Tüm animasyonlu öğeler</td>
</tr>
<tr>
  <td>30</td>
  <td>:focus</td>
  <td>$(":focus")</td>
  <td>Şu anda odaklanmış olan öğe</td>
</tr>
<tr>
  <td>31</td>
  <td>:contains(text)</td>
  <td>$(":contains('Hello')")</td>
  <td>"Merhaba" metnini içeren tüm öğeler</td>
</tr>
<tr>
  <td>32</td>
  <td>:has(selector)</td>
 <td>$("div:has(p)")</td>
 <td>p öğesine sahip tüm div öğeleri</td>
</tr>
<tr>
  <td>33</td>
  <td>:empty</td>
  <td>$(":empty")</td>
  <td>Boş olan tüm elemanlar</td>
</tr>
<tr>
  <td>34</td>
  <td>:parent</td>
  <td>$(":parent")</td>
  <td>Başka bir öğenin ebeveyni olan tüm öğeler</td>
</tr>
<tr>
  <td>35</td>
  <td>:hidden</td>
  <td>$("p:hidden")</td>
  <td>Tüm gizli p öğeleri</td>
</tr>
<tr>
  <td>36</td>
  <td>:visible</td>
  <td>$("table:visible")</td>
  <td>Tüm görünür tablolar</td>
</tr>
<tr>
  <td>37</td>
  <td>:root</td>
  <td>$(":root")</td>
  <td>Belgenin kök öğesi</td>
</tr>
<tr>
  <td>38</td>
  <td>:lang(language)</td>
  <td>$("p:lang(de)")</td>
  <td>"de" ile başlayan bir lang öznitelik değerine sahip tüm p öğeleri</td>
</tr>
<tr>
  <td>39</td>
  <td>[attribute]<td>
  <td>$("p:lang(de)")</td>
  <td>"de" ile başlayan bir lang öznitelik değerine sahip tüm p öğeleri</td>
</tr>
</table> 	 
<table>
<tr>
  <td>39</td>
  <td>[attribute]<td>
  <td>$("[href]")</td>
  <td>Bir href özniteliğine sahip tüm öğeler</td>
</tr>
<tr>
  <td>40</td>
  <td>[attribute=value]<td>
  <td>	$("[href='default.htm']")	</td>
  <td>"default.htm" değerine eşit bir href öznitelik değerine sahip tüm öğeler</td>
</tr>
<tr>
  <td>41</td>
  <td>[attribute!=value]<td>
  <td>	$("[href!='default.htm']")</td>
  <td>	"default.htm" değerine eşit olmayan bir href öznitelik değerine sahip tüm öğeler</td>
</tr>
<tr>
<td>40</td>
<td>[attribute$=value]<td>
<td>$("[href$='.jpg']")	</td>
<td>".jpg" ile biten bir href öznitelik değerine sahip tüm öğeler</td>
</tr>
<tr>
<td>40</td>
<td>[attribute|=value]<td>
<td>$("[title|='Tomorrow']")</td>
<td>	Başlık öznitelik değeri "Tomorrow"a eşit olan veya "Tomorrow" ile başlayan ve ardından kısa çizgi gelen tüm öğeler</td>
</tr>
<tr>
<td>40</td>
<td>[attribute^=value]<td>
<td>	$("[title^='Tom']")</td>
<td> "Tom" ile başlayan bir başlık özelliği değerine sahip tüm öğeler</td>
</tr>
<tr>
<td>40</td>
<td>[attribute~=value]<td>
<td>$("[title~='hello']")	</td>
<td>Belirli "hello" kelimesini içeren bir başlık öznitelik değerine sahip tüm öğeler</td>
</tr>
<tr>
<td>40</td>
<td>[attribute*=value]<td>
<td>	$("[title*='hello']")</td>
<td>	"hello" kelimesini içeren başlık özelliği değerine sahip tüm öğeler</td>
</tr>
 	 	 
:input	$(":input")	Tüm input elementleri
:text	$(":text")	 type="text" olan tüm input elementleri
:password	$(":password")	type="password" olan tüm input elementleri
:radio	$(":radio") type="radio" olan tüm input elementleri
:checkbox	$(":checkbox")	 type="checkbox" olan tüm input elementleri
:submit	$(":submit")	type="submit" olan tüm input elementleri
:reset	$(":reset")	type="reset" olan tüm input elementleri
:button	$(":button")	type="button" olan tüm input elementleri
:image	$(":image")	type="image" olan tüm input elementleri
:file	$(":file")	type="file" olan tüm input elementleri
:enabled	$(":enabled")	Tüm enabled input elementleri
:disabled	$(":disabled")	Tüm disabled input elementleri
:selected	$(":selected")	Tüm selected input elementleri
:checked	$(":checked")	Tüm checked input elementleri
 </table>	








`
* ![w3schools](https://media-exp1.licdn.com/dms/image/C4D0BAQHF7HLEYX6LSQ/company-logo_200_200/0/1607800000814?e=2147483647&v=beta&t=GKHAiWXada76R0r6gBhEGAr_3bVZjJPZmPDd5gdsLPM)
* Bakınız : [w3schools](https://www.w3schools.com/jquery/jquery_events.asp)
