- **Name:** Chudakov Ilya
- **Contacts:** 
  - Telegram: [@ichudi](https://t.me/ichudi)
  - email: ilyuhi4@yandex.ru
  - Github: [ilyuhi4](https://github.com/ilyuhi4)
  - Discord: [ilyuhich](https://discordapp.com/users/900030314724880424/)
- **Work:** Backend Python Developer
  - Expirience: 
    - about 3 years Python
    - about 2 years using Django
    - about 9 months in Django Rest Framework
  - Programming languages: 
    - python3
    - basics in HTML, CSS and JavaScript
    - basics SQL
  - Frameworks and instruments:
    - Linux (complete RedHat System Administrator course)
    - git, 
    - Django, DjangoRestFramework 
    - Celery, Celerybeat, Redis (with celery)
    - Postgres
    - PyCharm
  - Now learn JavaScript to open new horizonts of web applications :)
- **Projects:**
  - CRM using Django, HTML, telebot
  - Data synchronization app with Django, Django Rest Framework to using marketplaces
  - Digital cameras (about 30k) monitioring service with Django and python
  Can't show public code from theese projects because NDA
- **Education:**
  - Saint-Peterburg State University, Faculty of applied mathematics and control processes (finished 4 courses)
  - hyperskill.org - profession "Python Developer"
  - RedHat Certified System Administrator
- **English level:** 
  - B2 (live about 6 month in Egypt)
- **Additional:** 
  - Hobbies: motorcycles travelling, freediving, psychology
  
- **Code example:**
  - Django Generic ListView with redefined some attributes and get_queryset method 
  ```
      class AdsListView(ListView):
        model = Advertisment
        template_name = "main/ad_list.html"
        context_object_name = 'ads'
        ordering = "id"
        paginate_by = 5
        extra_context = {
            'title': 'Список объявлений',
            'all_tags': all_tags
        }

        def get_queryset(self):
            if self.request.GET.get('tag'):
                tag = self.request.GET.get('tag')
                print(' Я поймал запрос: ', tag)
                queryset = Advertisment.objects.filter(tags__name=tag)
            else:
                queryset = super().get_queryset()
            return queryset
  ```
