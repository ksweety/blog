# ***Kahlil Williams Blog***
### Hello! Welcome to my blog I will be showing you **COOL** things!

In this blog I will be talking about how I became to be the best coder and entrepreneur that I have become. 

## ***Some cool facts about me before we start:***

- I love playing Basketball
- I love playing Video Games




<ul>
    {% for post in site.posts %}
    <li>
    <a href= "/blog{{ post.url }}"> {{post.title}}</a>
    </li>
    {% endfor %}
</ul>