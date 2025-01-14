# Software Engineering Lab Team (SELT) - Webpage

### The `Software Engineering Lab` course - Assignment 1

Sharif University of Technology - Fall 2024

---

+ **Mohammad Moshtaghifar**

    + **Student ID**: 99109047

    + **Email**: mhmmoshtaghi@gmail.com

+ **Mehrad Milanloo**

    + **Student ID**: 99105775

    + **Email**: milanloomehrad@gmail.com

+ **Hasti Karimi**

    + **Student ID**: 99105656

    + **Email**: hastikarimi2002@gmail.com


## Description

This repository contains static front-end files for the Software Engineering Lab Team (SELT) webpage. The webpage is available [here](https://mehradmilan.github.io/index.html).

## Details of Implementation

یک وب پیچ زدیم. برنچ مستر protected بود و در نتیجه برای مرج شدن باید کسی pull request را approve و سپس مرج می‌کرد. اجازه‌ی کامیت مستقیم روی مستر را هم هیچ کدام از کانتریبیوترها نداشتند.

هر کسی تمایل به زدن فیکس یا فیچری داشت مطابق آن یک برنچ از مستر می‌گرفت و development را روی آن انجام می‌داد و سپس پول ریکوئست ایجاد می‌کرد.

یکبار دو برنچ مستقل یک پارامتر از `style.css` را تغییر دادند و در نتیجه موقع مرج دومین برنچ دچار کانفلیکت شدیم و بار دیگر دو برنچ مستقل عکس‌های متفاوتی برای پروژه انتخاب کرده بودند که دوباره دچار کانفلیکت شده و آن را رفع و سپس مرج کردیم.

وب‌پیج ما متشکل از یک صفحه خانه، پروژه‌ها، درباره‌ی ما، و ارتباط با ماست که هر کدام از این صفحات به طور مستقل داخل یک فایل html داخل فولدر src پیاده سازی شده‌اند و استایلشان توسط فایل `style.css` مشخص می‌شود.

## Theory Questions

1.
پوشه‌ی
`.git`
 یک پوشه مخفی است که در زمان شروع یک پروژه‌ی گیت در مسیر اصلی پروژه ایجاد می‌شود. این پوشه شامل تمام اطلاعات و داده‌های مورد نیاز برای مدیریت نسخه‌های پروژه است و به گیت اجازه می‌دهد تا تاریخچه‌ی تغییرات فایل‌ها، شاخه‌ها، تعویض نسخه‌ها، و اطلاعات دیگر را نگهداری کند.

+ محتوای پوشه `.git` شامل:

  + پوشه‌ی `objects`: شامل تمامی اشیا مانند کامیت‌ها، شاخه‌ها، و فایل‌های ذخیره شده در تاریخچه است.
  + پوشه‌ی `refs`: شامل اطلاعات شاخه‌ها و تگ‌های پروژه می‌شود.
  + فایل `HEAD`: شاخه فعلی که روی آن کار می‌شود را نشان می‌دهد.
  + پوشه‌ی `config`: تنظیمات پروژه مانند آدرس‌های ریموت و پیکربندی‌های محلی.
  + فایل‌های `index` و `logs`: ذخیره‌ی تغییرات انجام شده در شاخه‌ها و تاریخچه‌ی کامیت‌ها.

+ نحوه‌ی ایجاد پوشه `.git`

برای ایجاد پوشه‌ی `.git` و شروع یک مخزن گیت در پوشه‌ی پروژه، می‌توان از دستور زیر استفاده کرد:

```bash
git init
```

این دستور پوشه‌ی `.git` را ایجاد کرده و پروژه را به یک مخزن گیت تبدیل می‌کند تا گیت بتواند تغییرات را دنبال کند.
همچنین با ساختن مخزن از گیت، این پوشه به‌صورت خودکار ایجاد می‌شود.
<!-- </div> -->

2.
atomic commit
نوعی کامیت است که در آن فقط یک کار مشخص انجام شده است؛ برای مثال در آن می‌تواند یک فیچر پیاده‌سازی شده باشد یا یک باگ رفع شده باشد.
یک atomic pull request یک تغییر کوچک است در کد که به صورت مستقل قابلیت تست و ریویو شدن را دارد.
<!-- </div> -->

3.
+ Fetch
  + دستور `git fetch` اطلاعات جدید را از مخزن اصلی (remote) دریافت می‌کند و آن‌ها را به مخزن محلی می‌آورد، اما تغییرات را با شاخه‌های محلی ادغام نمی‌کند. این دستور به شما امکان می‌دهد از تغییرات در مخزن اصلی مطلع شوید، بدون اینکه این تغییرات روی کد محلی شما اعمال شوند.
  + معمولاً از این دستور استفاده می‌شود تا ابتدا تغییرات را مشاهده کنید و بعد تصمیم بگیرید که آیا می‌خواهید آن‌ها را با مخزن محلی خود ادغام کنید یا خیر.
+ Pull
  + دستور `git pull` ترکیبی از `fetch` و `merge` است. این دستور تغییرات جدید از مخزن اصلی را دریافت کرده و آن‌ها را با شاخه فعلی محلی شما ادغام می‌کند.
  + با `git pull`، نیازی به اجرای جداگانه `fetch` و سپس `merge` نیست؛ تغییرات بلافاصله به شاخه فعلی شما اضافه می‌شوند.
+ Merge
  + دستور `git merge` برای ترکیب تغییرات دو شاخه استفاده می‌شود. این دستور تغییرات یک شاخه دیگر را به شاخه فعلی شما اضافه می‌کند.
  + در صورتی که هر دو شاخه تغییراتی داشته باشند، Git سعی می‌کند آن‌ها را ادغام کند. اگر کانفلیکتی وجود داشته باشد (یعنی بخش‌های مختلف کد در هر دو شاخه تغییر کرده باشند)، باید کانفلیکت‌ها را به صورت دستی حل کنید.
+ Rebase
  + دستور `git rebase` راه دیگری برای ادغام تغییرات است که با هدف تمیزتر نگه داشتن تاریخچه استفاده می‌شود. این دستور تغییرات شاخه فعلی شما را به بالای تغییرات شاخه هدف انتقال می‌دهد.
  + در `rebase،` برخلاف `merge` که یک commit ادغام (merge commit) ایجاد می‌کند، تمام commitها به‌ترتیب روی شاخه جدید اعمال می‌شوند، و تاریخچه‌ای یکدست و خطی ایجاد می‌شود.
+ Cherry-Pick
  + دستور `git cherry-pick` به شما اجازه می‌دهد تا یک یا چند commit خاص از یک شاخه دیگر را به شاخه فعلی خود اضافه کنید، بدون اینکه تمام تغییرات آن شاخه را ادغام کنید.
  + این دستور برای مواقعی کاربرد دارد که می‌خواهید فقط برخی از commitها را از یک شاخه دیگر به شاخه خود اضافه کنید، نه تمام تغییرات آن شاخه را.
<!-- </div> -->

4.
+ دستور 
`reset`
  برای بازگرداندن 
  HEAD
  به یک کامیت قبلی استفاده می‌شود و می‌تواند در ایندکس و در صورت لزوم دایرکتوری کاری را هم تغییر دهد.

+ دستور `revert`
 یک کامیت جدید ایجاد می‌کند که تغییرات یک کامیت مشخص را معکوس می‌کند، بدون اینکه history را حذف کند.

+ دستور `restore` برای بازگردانی فایل‌ها به یک کامیت مشخص یا به شاخه فعلی استفاده می‌شود. از این دستور برای بازگرداندن تغییرات در فایل‌ها به حالت اولیه استفاده می‌شود.

+ دستور `switch` برای تغییر به یک branch دیگر یا ایجاد و سوئیچ به شاخه جدید استفاده می‌شود.

+ دستور `checkout` هم برای سوئیچ کردن به یک شاخه دیگر یا بازیابی فایل‌های خاص استفاده می‌شود. هر چند این دستور نسبت به دستور سوییچ قدیمی‌تر است و کاربردهای دیگری هم علاوه بر جابه‌جایی بین شاخه‌ها دارد.

5.
در گیت، مرحله‌ی 
**stage**
 یا 
 **index**
  به مرحله‌ای گفته می‌شود که فایل‌های پروژه قبل از اینکه به‌صورت نهایی به مخزن اضافه شوند، در آن قرار می‌گیرند. به عبارتی دیگر، فایل‌هایی که به مرحله‌ی stage اضافه می‌شوند، آماده‌ی کامیت شدن هستند. این مرحله به ما اجازه می‌دهد تا به‌صورت انتخابی فایل‌ها و تغییراتی که می‌خواهیم کامیت کنیم را تعیین کنیم.

با استفاده از دستور *add* می‌توانیم فایل یا فایل‌هایی را به stage اضافه کنیم:

```bash
git add <filename>
```

+ دستور `stash`

دستور `git stash` به ما اجازه می‌دهد تا تغییرات محلی‌ای که هنوز کامیت نشده‌اند را به‌طور موقت ذخیره کنیم و سپس شاخه را به حالت قبلی بازگردانیم. این دستور زمانی مفید است که می‌خواهیم بدون کامیت کردن تغییرات، به شاخه‌ی دیگری سوئیچ کنیم یا تغییرات را کنار بگذاریم.

6.
در گیت، 
**snapshot**
به تصویری کامل از تمام فایل‌های پروژه در لحظه‌ای خاص اشاره دارد. هر commit در واقع یک snapshot از وضعیت پروژه در آن زمان است، نه فقط تغییرات (diffs) نسبت به کامیت قبلی. این ویژگی باعث می‌شود گیت بتواند هر کامیت را به‌طور مستقل ذخیره کند و به راحتی به هر نسخه بازگردد. تفاوت بین snapshotها از طریق محاسبه تغییرات بین درخت‌های پروژه انجام می‌شود.

7.
تفاوت بین 
**Local Repository**
و
**Remote Repository**
در گیت به این صورت است که:

1. **Local Repository**: مخزنی است که روی سیستم شخصی ما قرار دارد و تغییرات به‌صورت محلی ذخیره می‌شود.

2. **Remote Repository**: مخزنی است که روی سرور یا فضای ابری مانند `GitHub` یا `GitLab` قرار دارد و از طریق اینترنت می‌توان به آن دسترسی داشت. این مخزن به‌صورت مشترک بین چندین کاربر استفاده می‌شود و تغییرات اعمال شده در آن توسط کاربران دیگر قابل مشاهده است.
