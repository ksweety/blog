# Kahlil Drippy Blog

Hello, *welcome* to my **blog**  

 
 
 

![Professional photo of me](/assets/IMG_7711.jpg)  
<ul> 
   {% for post in site.posts %} 
   <li>
   <a href= "/blog{{ post.url }}" {{post.title}}></a>
   </li>
   {% endfor %}
   </ul>
