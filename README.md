1. Clone this repo
2. To install the package, use pip (you already installed it, right?):

python -m pip install --user django-polls/dist/django-polls-0.1.tar.gz
Update mysite/settings.py to point to the new module name:

INSTALLED_APPS = [
    "django_polls.apps.PollsConfig",
    ...,
]
Update mysite/urls.py to point to the new module name:

urlpatterns = [
    path("polls/", include("django_polls.urls")),
    ...,
]
Run the development server to confirm the project continues to work.
