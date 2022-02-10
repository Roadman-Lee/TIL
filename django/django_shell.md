## shell?

가장 겉(외부)에 있는 단단한 “껍데기”를 의미한다.
즉, 가장 바깥쪽에서 사용자와 시스템이 서로 소통 할 수 있는 곳을 의미한다.

shell은 명령어 줄 인터페이스(CLI: Command-Line interface)방식과 GUI(Graphica User Interface) 방식 두 가지를 일반적으로 제공한다.

## django shell?

장고 프로젝트 설정이 로딩된 파이썬 쉘
일반 파이썬 쉘을 통해서는 장고 프로젝트 환경에 접근 불가
프로젝트 내의 각종 모듈 패키지를 활용하기 위해서는 장고 shell를 통해서 접근해야한다.
터미널에 아래와 같이 입력하여 들어가면 파이썬 인터프리터가 실행 된다.

```python
$ python manage.py shell
```

## django shell 왜 쓰는걸까?

여러가지 이유로 쓰이겠지만, 코린이인 나의 입장에서 shell 을 사용함으로써 model의 데이타를 추가, 저장하거나 저장되어 있는 데이터를 꺼내고 싶을때 django shell에서 먼저 입력해보고 그 입력한 코드를 그대로 [model.py](http://model.py) 에 붙여 넣는다.

## django shell puls?

장고 쉘을 사용하면 실행할 때마다 model을 다시 입력해줘야하는 번거로움이 있다.

그 번거로움을 덜기위해서 djago shell plus를 쓴다.

```python
$ pip install django-extensions
```

settings.py 내 INSTALLED_APPS에 `django_extensions` 추가 (장고 익스텐션은 장고 app 구조로 되어있어서 현재 프로젝트 내에서 해당 앱을 활성화시켜야 한다)

```python
INSTALLED_APPS = [
'django_extensions',
]
```

```python
$ python3 manage.py shell_plus
```

익스텐션 앱을 설치하면 shell_plus 사용가능, 필요한 모델을 자동 import 해줘서 편리함
