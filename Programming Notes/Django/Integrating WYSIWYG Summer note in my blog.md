## Integrating WYSIWYG Summer note in my blog #blog-development 

A WYSIWYG (pronounced “wiz-ee-wig”). 
WYSIWYG stands for **WHAT YOU SEE IS  WHAT YOU GET** 

#### Installation and setup
- `pipenv install django-summernote` 
- Add it to the installation apps.
- `path('summernote/', include('django_summernote.urls')),` to mysite urls.py.
- Make a folder named media in the root of the project and add these two lines in settings.py
	- `MEDIA_URL = '/media/' `
	- `MEDIA_ROOT = os.path.join(BASE_DIR, 'media/')`
- Similarly you can apply the editor to the forms 

```python
from django_summernote.widgets import SummernoteWidget, SummernoteInplaceWidget 
# Apply summernote to specific fields. 
class SomeForm(forms.Form): foo = forms.CharField(widget=SummernoteWidget()) 
# instead of forms.Textarea
```
