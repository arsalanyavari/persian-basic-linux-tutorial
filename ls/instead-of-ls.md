---
description: یه چیز بهتر جای ls
---

# instead of ls

<p align="right">خب ls خیلی پر کاربرده و هیچ سرور و سیستم لینوکسی نیست که شما بخواین باهاش کار کنین ولی ls نداشته باشه اما من خودم عمدتا از این دستور استفاده نمیکنم و بجاش از چیز دیگه‌ای که در ادامه میگم استفاده میکنم خب اگه اصولا دوست دارین ترمینالتون خوشگل موشگل باشه میتونین دستور logo-ls رو نصب کنین و ازش استفاده کنین. جدای از خوشگلی تفیرات ریپازیتوری گیت رو هم با ls گرفتن بهتون میگه که واسه من به شخصه خیلی کاربردیه. لینک ریپازیتوری گیت‌هابشون <a href="https://github.com/Yash-Handa/logo-ls">https://github.com/Yash-Handa/logo-ls</a> هستش که تقریبا کامل گفته چیکار کنین ولی مختصرا بخوام بگم؛ اول باید ترمینالتون از یه سری کاراکترای یونیکد پشتیبانی کنه پس لازمه که یه سری فونت رو توی سیستمتون نصب کنین و بعدش اون فونت رو برای ترمینالتون تنظیم کنین (شاید بعدا درباره‌ی این هم یه توضیحاتی نوشتم). برای نصب فونت هم بهتره برین سراغ nerd font که آدرس گیت‌هابشون باز <a href="https://github.com/ryanoasis/nerd-fonts">https://github.com/ryanoasis/nerd-fonts</a> هستش و من خودم شخصا از mononoki استفاده میکنم که میتونین توی این آدرس فایلای فونتشو بردارین <a href="https://github.com/arsalanyavari/.config/tree/main/Mononoki">https://github.com/arsalanyavari/.config/tree/main/Mononoki</a>​​خب همه چیز آمادست فقط کافیه جای ls بنویسین logo-ls تا خروجی‌ای قشنگی رو ببینین :)خروجی کامند logo-lsخب شاید بگین این دستور طولانیه و من حالشو ندارم این همه بنویسم همون ls ساده‌تره و بهتره؛ توی بخش آخر ls در مورد alias یه صحبت کوچیکی کردم. شما میتونین فایل کانفیگ شلی که استفاده میکنین رو باز کنین و یه alias بهش اضافه کنین؛ در ادامه توضیح میدم چطوری logo-ls رو جایگزین ls کنین.​اول از همه بگم که دستور <a href="https://app.gitbook.com/o/-MTqoLPzo_CMrdsCxnCk/s/-Mccftr9v7IOXR7VhlXs/sudo">sudo</a> رو در ادامه میخونین ولی چون اینجا قراره ازش استفاده کنین اگه بدونین هم خوبه؛ خب راهکار اول اینه که وقتی دارین نصبش میکنین به‌جای اینکه <code>sudo cp logo-ls /usr/local/bin</code> بزنین دستور <code>sudo cp logo-ls /usr/local/bin/ls</code> رو وارد کنین ولی با این کار کلا ls رو دیگه از دست میدین و دیگه ندارینش و یه روز ممکنه عجیب بهش نیاز داشته باشین پس اصلا اصلا این کارو نکنین ⚠️راهکار دوم که آدم‌وار تره اینه که توی شلی که دارین برین logo-ls رو جایگزین ls کنین که هروقتم نخواستین برش میدارین...</p>

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-Mccftr9v7IOXR7VhlXs%2Fuploads%2FgolwR6iAq8fmLplPx6EA%2Fimage.png?alt=media&#x26;token=3b7e1c1b-e295-47d2-8c3b-8afc17e0751a" alt=""><figcaption></figcaption></figure>

<p align="right">ابتدا لازمه بزنین <code>echo $SHELL</code> بعد که دیدین شلتون چیه متناظر باهاش فایل کانفیگشو باز کنین؛ اگه دارین قدم به قدم با این پیش میاین باید شلتون bash باشه ینی خروجی مطابق تصویر پایین باشه:</p>

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-Mccftr9v7IOXR7VhlXs%2Fuploads%2FJeXbx2qY8dLq6yLeXXiF%2Fimage.png?alt=media&#x26;token=6d2ccfbd-f53b-4d5b-bc43-38b1fa7c390b" alt=""><figcaption></figcaption></figure>

<p align="right">خب بعد از اینکه شلتون رو دیدین، میریم سراغ باز کردن فایل کانفیگش... مثلا فایل کانفیگ bahs فایلیه به اسم bashrc. که توی مسیر هوم‌تون قرار داره. توی دستور <a href="https://app.gitbook.com/o/-MTqoLPzo_CMrdsCxnCk/s/-Mccftr9v7IOXR7VhlXs/cd">cd</a> در مورد relative آدرس‌ها صحبت کردیم شما کافیه توی ترمینال یا خارج از اون توی یکی از آدرسای زیر این فایل رو با یه ادیتور باز کنین <code>bashr./~</code> یا <code>home/$USER/.bashrc/</code> (جای USER$ باید یوزرنیمتون رو بذارین).</p>

<p align="right">بعد از اینکه این فایل رو باز کردین خط زیر رو به انتهای این فایل اضافه کنین و سیوش کنین و ببندینش</p>

`alias ls="logo-ls"`

<p align="right">در آخر هم لازمه اگه ترمینالتون بازه (فقط یک‌بار) دستور <code>source ~/.bashrc</code> رو وارد کنین. میتونین هم تا زمان بعدی روشن خاموش کردن سیستمتون صبر کنین که کار هوشمندانه‌ای نیست پس همین دستور رو وارد کنین.</p>

<p align="right">از الان به بعد هروقت بزنین ls بجاش logo-ls اجرا میشه. اگه یه روزم خواستین به هر دلیلی برش دارین کافیه همین خط رو پاک کنین و دوباره دستور <code>source ~/.bashrc</code> رو بزنین.</p>
