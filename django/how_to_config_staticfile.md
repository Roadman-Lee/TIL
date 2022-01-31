rootfile/urls.py

```python
from django.contrib import admin
from django.urls import path
from django.conf.urls import include
from django.views.generic import RedirectView 
from django.conf import settings
from django.conf.urls.static import static

urlpatterns = [
    path('admin/', admin.site.urls),
    path('blog/', include('blog.urls')),
    path("", RedirectView.as_view(url="/blog/", permanant=True)),  # 사이트 주소로만 치고 들어왔을때 /blog/로 redirection 시켜준다
] + static(settings.STATIC_URL, document_root=settings.STATIC_ROOT) # static(정적)파일들을 처리할 수 있도로 해주는 셋팅
```

rootfile/settings.py

```python
import os

BASE_DIR = Path(__file__).resolve().parent.parent # code 상단에 입력

STATIC_URL = '/static/'
STATICFILES_DIRS = [
    os.path.join(BASE_DIR, 'static'),  # base_dir은 rootfile
]
```