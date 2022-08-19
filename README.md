# jquery

* # jQuery Event

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


* # jQuery Effects

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
* # HTML








`
* ![w3schools](https://media-exp1.licdn.com/dms/image/C4D0BAQHF7HLEYX6LSQ/company-logo_200_200/0/1607800000814?e=2147483647&v=beta&t=GKHAiWXada76R0r6gBhEGAr_3bVZjJPZmPDd5gdsLPM)
* Bakınız : [w3schools](https://www.w3schools.com/jquery/jquery_events.asp)
