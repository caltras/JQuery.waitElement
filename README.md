JQuery.waitElement
==================
Wait Element exist and be visible on the screen to execute a function. Case timeout, executes a "fail function"

$(**_selector_**).waitElement(_[fn,fnFail,time]_)

1. **fn**: function, "sucess function" (optional)
2. **fnFail**: function, "fail function" (optional) 
3. **time**: number "seconds", (default "30s")

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

MIT License
