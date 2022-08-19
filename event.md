# Event

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
   - Bir öğeye birden çok olay işleyicisi ekleyin :
   - $("p").on({
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
