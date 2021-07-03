# Building a commment system for the blog #blog-development 

### Roadmap to create a comment system

1. Create a model to save the comments.  
2. Create a form to submit comments and validate the input data.  
3. Add a view that processes the form and saves the new comment to the database.  
4. Edit the post detail template to display the list of comments and the form to add a new comment.

#### Building a Comment Model

```python
class Comment(models.Model):
	post = models.ForeignKey(Post,on_delete=models.CASCADE,related_name='comments')
	name = models.CharFieldi(max_length=80)
	email = models.EmailField()
	body = models.TextField()
	created_on = models.DateTimeField(auto_now_add=True)
	active = models.BooleanField(default=False)
	
	class Meta: 
		ordering = ['created_on']

	def __str__(self):
		return 'Comment {} by {}'.format(self.body, self.name)
```

1. The comment model we have Foreign key relation that establishes a many-to-one relationship with the Post model, since every comment will be made on the post.
2. Then we have an `active` boolean field that is set to False to prevent spam we will manually allow all the comments posted.

#### Adding models in admin.py for Administration


```python

from django.contrib import admin 
from .models import Post, Comment
@admin.register(Comment)
class CommentAdmin(admin.ModelAdmin): 
	list_display = ('name', 'body', 'post', 'created_on', 'active') 
	list_filter = ('active', 'created_on') 
	search_fields = ('name', 'email', 'body') 
	actions = ['approve_comments'] 
	def approve_comments(self, request, queryset): 
		queryset.update(active=True)

```