# How to add Pagination in Django

today i learned two ways how to add Pagination in Django
this allows you instant pagination using built in django library

put your pagination codes inside your views.py

```Python
from django.views.generic import ListView
from django.core.paginator import Paginator, EmptyPage,PageNotAnInteger

def journal_post_list(request):
    o_list = JournalPost.published.all()
    paginator = Paginator(o_list,3)
    page = request.GET.get('page')
    try:
        jposts = paginator.page(page)
    except PageNotAnInteger:
        jposts = paginator.page(1)
    except EmptyPage:
        jposts = paginator.page(paginator.num_pages)
    return render(request,'journal/post/list.html',{'page':page,'posts':jposts})

```

o_list contains data from your model, then the next line after
that means paginate that list into 3s, meaning 3 objects per page.

for shorter code, use a class instead, just inherit from ListView class
set the models (context_object_name), set paginate_by, and template_name
and your good to go. (error checking not included)

```Python
from django.views.generic import ListView

class PostListView(ListView):
    queryset = JournalPost.published.all()
    context_object_name = 'jposts'
    paginate_by = 3
    template_name = 'blog/post/list.html'

```
