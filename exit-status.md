---
description: >-
  هر برنامه‌ای که اجرا می‌شود پس از اتمام یک کد بر میگردونه که به عنوان exit
  code شناخته می‌شه و بر این اساس میتونیم مطمئن بشیم که برنامه درست اجرا شده یا
  به خطا خورده و اگر خطا داشته چه نوع خطایی داشته
---

# Exit status

<p align="right">دیدین بعضی وقتا یه کامند رو اشتباه میزنین و بعدش تو صفحه ترمینالتون بهتون یه اروری میده؟ مثل عکس زیر</p>

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption><p>خروجیای اشتباه کامند</p></figcaption></figure>

<p align="right">خب بعد از اینکه یه کامند اجرا شد میتونین ببینین چه عددی برگردونده؛ اگه کامند ?$ echo رو بزنین بهتون اگزیت کد دستور قبلی رو برمیگردونه.</p>

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption><p>تو عکس بالا بار اول اگزیت کد برنامه‌ی yes که با ctrl+c لغو شده رو میبنیم و بعدش هم دفعه دوم اگزیت کد همون ?$ echo اولی که اجرا شده رو نشون میده</p></figcaption></figure>

<p align="right">خب تنها چیزی که لازم میدونم بهش اشاره کنم و بدونین اینه که اگه اگزیت‌کد صفر بود ینی درست اجرا شده و هر چیز بجز آن یعنی برنامه حین اجرا به اروری خورده که هر عدد متناظر یک اروره پس لازمه برین بخونین ببینین اگه چه عددی برگردونده شد به چه معنیه... یه سری کدای مهم رو براتون اوردم:</p>

| معنی کد عدد به انگلیسی                                 | معنی عدد کد به فارسی                                     | عدد کد |
| ------------------------------------------------------ | -------------------------------------------------------- | ------ |
| Success                                                | موفقیت                                                   | 0      |
| General error                                          | خطای عمومی                                               | 1      |
| Misuse of shell builtins (e.g., invalid options, etc.) | استفاده نادرست از ساختارهای شل (مثالا گزینه‌های نامعتبر) | 2      |
| Command invoked cannot execute                         | کامند نمی‌تواند اجرا شود                                 | 126    |
| "command not found" error                              | خطای "command not found".                                | 127    |
| Invalid argument to exit                               | آرگومان برای خروج نامعتبره                               | 128    |
| Script terminated by ctrl+c                            | اسکریپت توسط ctrl+c خاتمه یافته                          | 130    |
| Exit status out of range                               | خروج از وضعیت خارج از محدوده                             | 255    |

<p align="right">نکته: اگزیت‌کد یقینا عددی بین 0 تا 255 خواهد بود</p>

<details>

<summary>چگونه خودمون برنامه‌ای بنویسیم که اگزیت‌کدی متفاوت تولید کنه؟</summary>

<p align="right">کد پایین به زبان پایتون نوشته شده که یه ورودی از شما میگیره و با همون ورودی اگزیت میکنه</p>

```python
#!/usr/bin/env python
from sys import exit
def main():
    n = int(input("Enter a number to specify exit code: "))%256
    exit(n)


if __name__ == "__main__":
    main()
```

<p align="right">کد بعدی هم به زبان c نوشته شده.</p>

```c
#include <stdio.h>

int main(void)
{
    int n = 0;
    printf("Enter a number to specify exit code: ");
    scanf("%d", &n);
    n%=256;
    return n;
}
```

<p align="right">کد بعدی هم به زبان bash نوشته شده.</p>

```bash
#!/bin/bash

echo "Enter a number to specify exit code: "
read n

exit $n
```

<p align="right">من با این سه تا زبان اوکیم و اینها و میشه گفت تو هر زبان برنامه‌نویسی و اسکریپت‌نویسی چنین چیزی هست و شما با توجه به منطق برنامتون میتونین مشخص کنین که چطور کار کنه.</p>

</details>

