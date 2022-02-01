```python
{% for post in posts %}
	<div>
		<p>published: {{ post.published_date }}</p>
		<h1><a href="">{{ post.title }}</a></h1>
		<p>{{ post.text|linebreaksbr }}</p>
	</div>
{% endfor %}
```

`linebreaksbr` : 블로그 글 텍스트에서 행이 바뀌면 문단으로 변환하도록 하라는 의미입니다.
행바뀜을 문단으로 변환하는 필터를 적용한다는 표현을 쓰기도 합니다.