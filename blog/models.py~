"""models for question application"""

from django.utils.translation import ugettext_lazy as _
from django.db import models
from django.conf import settings
from django.utils import timezone

class Question(models.Model):

    """Class representing a question."""

    title = models.CharField(max_length=100, null=False, blank=False)

    private = models.BooleanField(default=False)

    user_id = models.ForeignKey(settings.AUTH_USER_MODEL,related_name='questions')


class Answer(models.Model):

    """Class representing an answer."""

    body = models.TextField(null=False,blank=False)

    question = models.ForeignKey(Question, related_name='answers')

    user_id = models.ForeignKey(settings.AUTH_USER_MODEL,related_name='given_answers')

class Tenant(models.Model):

    """Class representing a tenant."""

    name = models.CharField(max_length=50, null=False, blank=False)

    api_key = models.CharField(max_length=200,null=False, blank=False)

    def __str__(self):
        return self.name

class Request(models.Model):

    """Class representing an api request."""

    tenant = models.ForeignKey(Tenant, related_name='requests')

    url = models.CharField(max_length=100, null=False, blank=False)

    requested_on = models.DateTimeField(default=timezone.now)

    requested_by = models.ForeignKey(settings.AUTH_USER_MODEL,related_name='requests')

 
