---
description: برای نشان دادن سایز هر المان در کنار آن
---

# ls -s

وقتی میخواین از یه پوشه ls بگیرین و در لحظه ببینین سایز هر فایل هم چقدره فقط کافیه از آپشن s- استفاده کنین.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>خروجی ls -s. قسمت‌های قرمز همان سایز فایل‌ها هستند</p></figcaption></figure>

دو نکته وجود داره؛ اول اینکه این سایز‌ها به بایت (Byte) هستند و خب برای ما خوندنشون راحت نیست پس میتونین از آپشن h- که در ادامه توضیحش میدم استفاده کنین. نکته‌ی دوم هم اینه که سایز دایرکتوری‌ها معمولا 4 بایت نوشته میشه پس اینو حواستون باشه.

فرمت بلند آپشن s- هم size-- هست؛ یعنی میتونین به شکل زیر هم بنویسین:

```
ls --size
```