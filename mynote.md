# Django 筆記
#### 1. 取得 template code:
	from django.template.loader import render_to_string
#### 2. 輸出資料表 > models.py:
	$ python manange.py inspectdb [table] > model.py
#### 3. templates filter :
	-templatetags
	|- __init__.py
	|- myfilter.py
	
	myfilter.py:
	from django.template.defaulttags import register
	@register.filter
	def filter():
	    '''code'''
	    return something
	
	template 裡加上 {% myfilter %}
	呼叫 filter 方法: {{ parameter1|function name:parameter2 }}
