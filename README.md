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
