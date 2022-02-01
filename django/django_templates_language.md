- `linebreaksbr`
    
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
    
- base.html 확장
    
    base.html
    
    ```python
    <body>
        <div class="page-header">
            <h1><a href="/">Django Girls Blog</a></h1>
        </div>
        <div class="content container">
            <div class="row">
                <div class="col-md-8">
                    {% block content %} # block content 범위 시작
                    {% endblock %} # block content 범위 끝
                </div>
            </div>
        </div>
    </body>
    ```
    
    `block`을 만듬.
    템플릿 태그 `{% block %}`으로 HTML 내에 들어갈 수 있는 공간을 만들었다. 
    `base.html`을 확장해 다른 템플릿에도 가져다 쓸 수 있게 한 것.
    
    content.html
    
    ```python
    {% extends 'blog/base.html' %} # base.html 확장
    
    {% block content %} # block content 시작
        {% for post in posts %}
            <div class="post">
                <div class="date">
                    {{ post.published_date }}
                </div>
                <h1><a href="">{{ post.title }}</a></h1>
                <p>{{ post.text|linebreaksbr }}</p>
            </div>
        {% endfor %}
    {% endblock %} # block content 끝
    ```