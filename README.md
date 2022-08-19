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










`
* ![w3schools](https://media-exp1.licdn.com/dms/image/C4D0BAQHF7HLEYX6LSQ/company-logo_200_200/0/1607800000814?e=2147483647&v=beta&t=GKHAiWXada76R0r6gBhEGAr_3bVZjJPZmPDd5gdsLPM)
* Bakınız : [w3schools](https://www.w3schools.com/jquery/jquery_events.asp)
