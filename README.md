# gRAB GDTOT Cookie
Browser's Console code to Grab Cookie from File Sharer Site GDTOT

First You have to Login then you can simply run this code in your browser's console(ctrl+shift+j).  
    
It'll automatically get copied in Your Notepad.
You'll get both Crypt and Cookie, Use according to your need.
 
```
javascript:(function () {
 const input = document.createElement('input');
 COOKIE = JSON.parse(JSON.stringify({cookie : document.cookie}));
 input.value = COOKIE['cookie'].split('crypt=')[1];
 document.body.appendChild(input);
 input.focus();
 input.select();
 var result = document.execCommand('copy');
 document.body.removeChild(input);
  if(result)
    alert('Crypt copied to clipboard');
  else
    prompt('Failed to copy Crypt. Manually copy below Crypt\n\n', input.value);
})();
```
