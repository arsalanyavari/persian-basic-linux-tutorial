---
description: برای صفحه صفحه کردن
---

# less & more

خب قبل تر که منوال رو گفتیم اگه منوال یک کامند رو دیده باشین دیدن که صفحه به صفحس و با q ازش خارج میشین و...

خب بعضی وقتا مثلا خروجی کتمند کت یا خروجی ای که روی استاندارد اوت پوتتون \(standard output\) قرار میگیره خیلی زیاده و مثلا کلی باید اسکرول کنین تا به اول برسین یا حتی از بافر ترمینالتون بیشتره و مثلا دیگه اولشو نمیتونین ببینین یا به هر دلیل دیگه ای دوست دارین صفحه به صفحه نشونتون بده

خب اینجا جای cat بنویس less یا more یا اگه کت نمیکنی و مثلا خروجی یه دستور رو میخوای صفحه بندی کنی مثل ls بعد از دستورت این کاراکتر رو بزار " \| " \(\(با شیفت بالای اینتره\)\) و بعدش بنویس less یا more             خب اینم یه مثال 👇👇

```text
# less /var/log/pacman.log
# ls /etc | less
```

جلوتر در مورد " \| " بیشتر حرف میزنیم که اصن چی هست و چرا هست و اینا \(میتونی ام سرچ کنی اسمش pipeline عه😅😅\)

یه جمله معروفی هست که میگه less is more اقا فلسفه نچینیم جای more از less استفاده کنین دلیلشم میتونین سرچ کنین 👇👇

 **Similar to more, less command allows you to view the contents of a file and navigate through file. The main difference between more and less is that less command is faster because it does not load the entire file at once and allows navigation though file using page up/down keys.**

اینم تعابیر یه بنده خدا دیگست 👇👇

**more**

`more` is an old utility. When the text passed to it is too large to fit on one screen, it pages it. You can scroll down but not up.

Some systems hardlink `more` to `less`, providing users with a strange hybrid of the two programs that looks like `more` and quits at the end of the file like `more` but has some `less` features such as backwards scrolling. This is a result of `less`'s `more` compatibility mode. You can enable this compatibility mode temporarily with `LESS_IS_MORE=1 less ...`.

`more` passes raw escape sequences by default. Escape sequences tell your terminal which colors to display.

**less**

`less` was written by a man who was fed up with `more`'s inability to scroll backwards through a file. He turned `less` into an open source project and over time, various individuals added new features to it. `less` is massive now. That's why some small embedded systems have `more` but not `less`. For comparison, `less`'s source is over 27000 lines long. `more` implementations are generally only a little over 2000 lines long.

In order to get `less` to pass raw escape sequences, you have to pass it the `-r` flag. You can also tell it to only pass ANSI escape characters by passing it the `-R` flag

_See `less` FAQs for more details:_ [_http://www.greenwoodsoftware.com/less/faq.html_](http://www.greenwoodsoftware.com/less/faq.html)



خب از هر چه بگذریم سخن دوست خوش تر است ...

تو کامند less آپشن  N- کارش اینه کنار خط ها شماره میزاره و من زیاد ازش استفاده کردم

یه آپشن دیگه اینکه وقتی q میزنی و از صفحه ها میای بیرون خودکار ترمینالت رو clear میکنه؛ اگه خواستی محتوا بمونه از آپشن X- استفاده کن

خب مثل همیشه بیشترر خواستی بدونی سرچ یا منوال خوانی :\)\)



