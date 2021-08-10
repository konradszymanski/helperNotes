# helperNotes

### css only for firefox
```
@-moz-document url-prefix() {  
 select.boost-pfs-filter-top-sorting-select {  
   text-indent: 5px!important;  
  }  
}  
``` 
### style by URL in liquid
```
{% if request.path contains '/pages/reviews' %}  
    <style>  
      h1 {  
      display: none;  
      }  
    </style>  
{% endif %}  
```
### style css using JavaScript
```
  <script>
    const accordionContent = document.querySelector('.shogun-accordion-wrapper');
    const header1 = document.getElementsByTagName("h1")[1];
    
    function hideFAQ() {
     accordionContent.style.display = "none";
     header1.style.display = "none";
}
    function showFAQ() {
  	accordionContent.style.display = "block";
  	header1.style.display = "block" 
}
   window.onload = () => {
  		myMutationObserver = window.MutationObserver || window.WebKitMutationObserver;
  var watchdog = new myMutationObserver(function (mutations, observer) {
   
    if (document.URL.includes("page=")) {
      hideFAQ();
    } else {
      showFAQ();
    }
  });
  watchdog.observe(document.getElementById("PageContainer"), {
    subtree: true,
    childList: true,
  });
};
  </script>
  
  ////// SPECIFIC URL FOR CSS EDITING PART 2 with updates to typeerrors \
     <script>
    const accordionContent = document.querySelector('.shogun-accordion-wrapper');
    const header1 = document.getElementsByTagName("h1")[1];
    const shogunParagraph = document.querySelector('.shg-row')
    
    function hideFAQ() {
	 shogunParagraph.style.display = "none";
      
      if (  accordionContent == null){
         
      } else {
         accordionContent.style.display = "none";
      }
      
      if (  header1 == null){
            
      } else {
     	 header1.style.display = "none";
      }
 
   
     console.log('hide')
}
    function showFAQ() {
      if (  accordionContent == null){
         
      } else {
         accordionContent.style.display = "block";
      }
      if (  accordionContent == null){
         
      } else {
         header1.style.display = "block";
      }
//  	accordionContent.style.display = "block";
//  	header1.style.display = "block";
    shogunParagraph.style.display = "flex";
      console.log('show')
}
   window.onload = () => {
 	myMutationObserver = window.MutationObserver || window.WebKitMutationObserver;
  	var watchdog = new myMutationObserver(function (mutations, observer) {
   
    if (document.URL.includes("page=")) {
      hideFAQ();
    } else {
      showFAQ();
    }
  });
  watchdog.observe(document.getElementById("PageContainer"), {
    subtree: true,
    childList: true,
  });
};
  </script>
  ```
  ### change attributes to scripts example
  ```
  <!-- EDIT INSTA, NUMBER OF PHOTOS ON DIFFERENT SCREEN SIZE -- START -->
  <script id='instaScript' src="https://showcase.abovemarket.com/embed/gallery/19994" data-gallery-id="19994" async></script>
  <script>  
    let valueInsta;
    const instaScript = document.getElementById('instaScript')
    window.innerWidth < 740 ? instaScript.setAttribute('data-force-limit', 3): instaScript.setAttribute('data-force-limit', 5)
  </script>
  ```
 <!-- EDIT INSTA, NUMBER OF PHOTOS ON DIFFERENT SCREEN SIZE -- END -->  
 
 ### node express
```
const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => {
  res.send('Hello World!')
})

app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`)
})
```
### change background color, react
```
import React, { useState } from 'react';

const colorNames = ['Aquamarine', 'BlueViolet', 'Chartreuse', 'CornflowerBlue', 'Thistle', 'SpringGreen', 'SaddleBrown', 'PapayaWhip', 'MistyRose'];

export default function ColorPicker() {
  const [color, setColor] = useState('Tomato');

 const divStyle = {backgroundColor: color};

  return (
    <div style={divStyle}>
      <p>Selected color: {color}</p>
      {colorNames.map((colorName)=>(
        <button 
          onClick={() => setColor(colorName)} 
          key={colorName}>
       	     {colorName}
      	</button>
      ))}
    </div>
  );
}
```
### line through not centered
```
.element{
	background-image: linear-gradient(transparent 1.2ex, black 1.2ex, black 1.4ex, transparent 1.4ex);
}
```

### add attribute to all anchors on the page
```
let links = document.getElementsByTagName('a');
	for(let aa=0; aa<links.length; aa++) 
          {
             links[aa].setAttribute("rel", "noopener")
          }
```
### react cheat sheet
https://dev.to/buddhadebchhetri/react-cheatsheets-5978
