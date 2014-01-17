JQuery.waitElement
==================
Wait Element exist and be visible on the screen to execute a function. Case timeout, executes a "fail function"
#[Example]
```javascript
  $(document).ready(function(){
          $("body").append("Creating...");
          setTimeout(function(){
              $("body").append("<div class='box'></div>");
          },5000);
          $("div").waitElement(function(){
              $("body").append("Created.");
          });
          $("a").waitElement(function(){
              $("body").append("a element");
          },function(){
              $("body").append("Element 'a' not found");
          },10)
      }
  );
```
