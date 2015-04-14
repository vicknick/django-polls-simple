
from django.contrib import admin
from polls.models import Choice
from polls.models import Poll

class ChoiceInline(admin.TabularInline):
	model = Choice
	extra = 3

class PollAdmin(admin.ModelAdmin):
	list_display = ('question_text','pub_date','was_published_recently')
	list_filter = ['pub_date']
	search_fields = ['question']
	fieldsets = [
		('Poll Question', {'fields':['question_text']}),
		('Date information',{'fields':['pub_date'],'classes':['collapse']}),
	]
	inlines = [ChoiceInline]
	

admin.site.register(Poll,PollAdmin)

# Register your models here.
