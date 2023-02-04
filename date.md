---
description: ساعت و تاریخ و روز هفاه و این مدل چیزا تو ترمینالمان
---

# date

خب از اسمشم معلومه چیکار میکنه. کافیه ترمینالت رو باز کنی و بنویسی date

با فرمت روبرو میتونی خروجی غیر الان بگیری ازش "date --date=" string مثلا👇👇

![](<.gitbook/assets/image (10) (1).png>)

حتی میتونی مثلا بنویسی "date --date="nov 5 2000 ((تاریخ تولدمه 😂😂))

حتی مقدار string رو میتونی با مقادیر next fri یا روزای دیگه یا حتی tomorrow یا yesterday و هر چیز با مفهوم دیگه ای جایگزین کنی

میشه حتی فرمتش رو هم عوض کرد مثلا "date "+%A %B %d %T %D که خب منواش رو بخونین و ببینین دیگه ایناها این لیستش که از منوالش کپی کردم👇👇 (( نشینین اینارو مثل خنگولا حفظ کنینا😐😂! قرار نیس اینارو حفظ باشین منم نیستم؛ بر اساس نیازتون منوال رو باز میکنین و میبینین چی مال چیه و ازش استفاده میکنین. فقط کافیه که بدونین این کامند همچین قدرتی داره وفلان))

```
   FORMAT controls the output.  Interpreted sequences are:

   %%     a literal %

   %a     locale's abbreviated weekday name (e.g., Sun)

   %A     locale's full weekday name (e.g., Sunday)

   %b     locale's abbreviated month name (e.g., Jan)

   %B     locale's full month name (e.g., January)

   %c     locale's date and time (e.g., Thu Mar  3 23:05:25 2005)

   %C     century; like %Y, except omit last two digits (e.g., 20)

   %d     day of month (e.g., 01)

   %D     date; same as %m/%d/%y

   %e     day of month, space padded; same as %_d

   %F     full date; like %+4Y-%m-%d

   %g     last two digits of year of ISO week number (see %G)

   %G     year of ISO week number (see %V); normally useful only with %V

   %h     same as %b

   %H     hour (00..23)

   %I     hour (01..12)

   %j     day of year (001..366)

   %k     hour, space padded ( 0..23); same as %_H

   %l     hour, space padded ( 1..12); same as %_I

   %m     month (01..12)

   %M     minute (00..59)

   %n     a newline

   %N     nanoseconds (000000000..999999999)

   %p     locale's equivalent of either AM or PM; blank if not known

   %P     like %p, but lower case

   %q     quarter of year (1..4)

   %r     locale's 12-hour clock time (e.g., 11:11:04 PM)

   %R     24-hour hour and minute; same as %H:%M

   %s     seconds since 1970-01-01 00:00:00 UTC

   %S     second (00..60)

   %t     a tab

   %T     time; same as %H:%M:%S

   %u     day of week (1..7); 1 is Monday

   %U     week number of year, with Sunday as first day of week (00..53)

   %V     ISO week number, with Monday as first day of week (01..53)

   %w     day of week (0..6); 0 is Sunday

   %W     week number of year, with Monday as first day of week (00..53)

   %x     locale's date representation (e.g., 12/31/99)

   %X     locale's time representation (e.g., 23:13:48)

   %y     last two digits of year (00..99)

   %Y     year

   %z     +hhmm numeric time zone (e.g., -0400)

   %:z    +hh:mm numeric time zone (e.g., -04:00)

   %::z   +hh:mm:ss numeric time zone (e.g., -04:00:00)

   %:::z  numeric time zone with : to necessary precision (e.g., -04, +05:30)

   %Z     alphabetic time zone abbreviation (e.g., EDT)

   By default, date pads numeric fields with zeroes.
   The following optional flags may follow '%':
```

برخلاف میل باطنیم اینجا زیاد شلوغ شد و این وظیفه خودتون بود که [منوال ](man-help.md)رو باز کنین و نگاش کنین ول میخوام عدات کنین که اره اقا نه تنها من بلکه حتی خود لینوس توروالدز هم منوال کامندارو میخونه. اصلا حدیث داریم منوال را ساختند که مورد استفاده قرار گیرد باشد که رستگار شوید :))
