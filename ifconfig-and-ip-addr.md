---
description: برای نشان دادن و تغیر مقادیر آنها
---

# ifconfig & ip addr

خب توی ویندوز باید میرفتیم به control panel بعدش قسمت نتورک آدپتر و شبکه مورد نظر رو انتخاب و ...

_**تذکر مهم: اگه اینارو درست نفهمیدین پنیک نکنین. درس شبکه‌های کامپیوتری رو که پاس کنین یا درمورد شبکه بخونین یا سرچ کنین براون خیلی اوکی و ایزی خواهد بود (هرچند ک چیز عجیب غریبی نیستن واقعا)**_

خب توی لینوکس مثلا میخوای ببینی کارت شبکه وایرلست آیپی ای که بهش اختصاص داده شده از طرف سیستمت چنده خب کافیه یکی از دوتا دستور بالا رو بزنی (( معادل ifconfig توی cmd ویندوز ipconfig عه اسمش))

![نکته قایل توجه اینه که باید اسم کارت شبکتو بدونی  چون ممکنه چنتا (حداقل دوتا) داشته باشی](<.gitbook/assets/image (4) (1).png>)

خب الان مثلا آیپی داخلی سیستم من 172.18.52.59 عه :))

خب اینو میشه عوض کرد با فرمت زیر

ifconfig \<interface\_name> \<ip\_address> netmask \<netmask\_address>

مثللا از من اینطوری میشه

> ifconfig eth0 172.18.52.85 netmask 255.255.240.0
>
> دو نکته که باید دقت کنین اینه که تو همون رنج باید آیپی بدین
>
> و نکته دوم اینکه جای netmask میتونستین / بذارین و بصورت دسیمال عدد نتمسک رو مینوشتین👇
>
> ifconfig eth0 172.18.52.69/20

خب این کامن ifconfig واسه آپ یا داوون کردن کارت شبکه ام استفاده میشه با فرمت های زیر

ifconfig eth0 up معدلش=> ifup eth0

ifconfig eth0 down معدلش=> ifdown eth0

و به عنوان حسن ختام کلامم با فرمت زیر هم میشه مک آدرس رو عوض کرد \[ بله درست شنیدین مک آدرس ]

ifconfig eth0 hw ether AA:BB:CC:DD:EE:FF

خب تا جایی ک میدونم این کارارو با ip addr هم میشه کرد و اون جدید تر و قوی تر طوره و خب اینجا صرفا میخواستم بدونین از اینکارا سمت کامند لاین هم میشه انجام داد و روزی که گیر کردین با سرج کردن سریع کامندو میبینین و باهاش آشنایین و ازش استفاده میکنین :)) بیشتر خواستین بدونین منوالشون رو بخونین یا سرچ کنین =)
