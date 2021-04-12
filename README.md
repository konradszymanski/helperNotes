# helperNotes

//ONLY FOR FIREFOX CSS\
@-moz-document url-prefix() {  
 select.boost-pfs-filter-top-sorting-select {  
   text-indent: 5px!important;  
  }  
}  
  
////// URL Liquid\
{% if request.path contains '/pages/reviews' %}  
    <style>  
      h1 {  
      display: none;  
      }  
    </style>  
{% endif %}  


////// SPECIFIC URL FOR CSS EDITING 
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
