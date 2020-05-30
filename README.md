# KPI-presentaion

Python -> requirements.txt

Authorization:

admin - admin_main@mail.ru / 1234

user1 - user2@mail.ru / ca4hjzlmsq

user2 - user3@mail.ru / asd123asd

Base KPI project contatins 30 indicators for 25 managers.
Short version contatins indicators from main 4 groups - value, percent, turnover, variable.

Value indicator = Sum(rows)

Percent indicator = Sum(numerator rows) / Sum(denominator rows)

Turnover indicator = Avr(12month numerator rows) / Avr(12month denominator rows)

Variable indicator = Sum(fixed rows) + (Sum(variable rows) * Revenue implementation %)


Users are divided into three types:

Manager - has access only to own dashboard page and indicator page from his indicator list

Director - has access for all urls of all users, but doesn't have own dashboard page

Director/Manager - has access for all urls of all users, and has own dashboard page


To set current period use CurrentPeriod model.

On dashboard page implementation calculate as YTD slice on current period.
On indicator page it is possible to form table with YDT or by month data.
Also on indicator page possible to form forecast data. In this case until current period will be Actual data, after Forecast data.

##################################################

branch #1
Celery block added.
Mongoengine block added.

Create simple celery task for logging form queries from indicator page.


branch #3
Weekly beat task that update database data.


##################################################


branch #2
Dajngo REST block added.

Allow to get detail indicator information by url

host:port/api/indicator/<int:id>-<int:year>/
127.0.0.1:8000/api/indicator/3-2019/


##################################################

branch #4

Cache block added.
For dashboard app cache page for 1 week.
For indicator app cache only large controller object

