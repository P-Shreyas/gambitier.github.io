---		 
layout: default		
---		
 <!-- Section   <span class="icon fa-rocket"></span> -->		
 <section>		
 	<header class="major">		
 		<h2>Recent Posts</h2>		
 	</header>		
 <div class="posts">		
 {% for post in site.posts limit:6 %}		
		<article>
			<header>
				<h3>{{ post.title }}</h3>
				<h6><time datetime="{{ post.date | date_to_xmlschema }}" class="by-line">{{ post.date | date_to_string }}</time></h6>
			</header>
			<p>{{ post.content | strip_html | truncatewords:50 }}</p>
			 <ul class="actions">
				 <li><a href="{% if site.baseurl == "/" %}{{ post.url }}{% else %}{{ post.url | prepend: site.baseurl }}{% endif %}" class="button">More</a></li>
			 </ul>	
		 </article>
 {% endfor %}		
 </div>		
 	<hr>	<br>	
 	<ul class="actions vertical">		
 		<li>		
 	    <a href="/archive/index.html" class="button fit">Load More Posts</a> 		
 		</li>		
 	</ul>		
 </section>   			
