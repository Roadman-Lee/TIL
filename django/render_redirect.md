`render`(*request*, *template_name*, *context=None*, *content_type=None*, *status=None*, *using=None*)**

### **필수 인수 [¶](https://docs.djangoproject.com/en/4.0/topics/http/shortcuts/#required-arguments)**

`request`이 응답을 생성하는 데 사용되는 요청 개체입니다.
`template_name`사용할 템플릿의 전체 이름 또는 템플릿 이름의 순서입니다. 시퀀스가 주어지면 존재하는 첫 번째 템플릿이 사용됩니다.

### **선택적 인수 [¶](https://docs.djangoproject.com/en/4.0/topics/http/shortcuts/#optional-arguments)**

`context`**템플릿 컨텍스트에 추가할 값의 사전입니다. 기본적으로 이것은 빈 사전입니다. 사전의 값이 호출 가능한 경우 뷰는 템플릿을 렌더링하기 직전에 이를 호출합니다.
`content_type`**결과 문서에 사용할 MIME 유형입니다. 기본값은 `'text/html'`입니다.
`status`**응답의 상태 코드입니다. 기본값은 `200`입니다.
`using`**템플릿을 로드 하는 **`[NAME](https://docs.djangoproject.com/en/4.0/ref/settings/#std:setting-TEMPLATES-NAME)`**데 사용할 템플릿 엔진입니다.

기본적으로 request 개체를 받아서, template_name 을 받아서 html 을 뿌려주는 역활을 하지만, 선택적 인수를 받아서 받아진 정보와 함께 html에 뿌려줄 수 있다.

`redirect`(*to*, **args*, *permanent=False*, ***kwargs*)[¶](https://docs.djangoproject.com/en/4.0/topics/http/shortcuts/#django.shortcuts.redirect)**

전달된 인수에 대한 적절한 URL을 반환합니다 .
기본적으로 임시 리디렉션을 실행합니다. 
`permanent=True`**영구 리디렉션을 발행하기 위해 전달 합니다.