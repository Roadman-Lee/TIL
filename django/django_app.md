## django app 

### <u>재사용성</u>을 목적으로한 파이썬 팩키지   
- 재사용성을 목적으로 둔 것이 아니라면, 하나의 장고 앱에서 현재 프로젝트의 거의 도느 기능을 구현해도 무방하다.    
- 앱을 하나의 작은 서비스로 봐도 무방하닼.    

### 하나의 앱이름은 현재 프로젝트 상에서 <u>유일</u>해야한다.   

### 새롭게 생선한 장고앱이나 외부 라이브러리 형태의 장고앱은 <u>필히 `settings.INSTALLED_APPS`에 등록</u>을 시켜줘야만 장고앱으로서 대접을 받는다.
- 앱의 `URLConf`를 제외한 부분(모델, 템플릿, static 등)들이 자동으로 등록된다.