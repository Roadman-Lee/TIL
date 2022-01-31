rootfile/settings.py

```python
import os

BASE_DIR = Path(__file__).resolve().parent.parent # code 상단에 입력

STATIC_URL = '/static/'
STATICFILES_DIRS = [
    os.path.join(BASE_DIR, 'static'),  # base_dir은 rootfile
]
```