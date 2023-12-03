
# ریجکس‌های پر کاربرد

در این ریپوزیتوری مجموعه‌ای از پرکاربردترین ریجکس‌های مصرفی در وب ایرانی لیست شده است

* **همکاری در آپدیت ریپوزیتوری**! لطفا برای همکاری ایشو مربوطه را مطالعه کنید

## لیست ریجکس‌ها

<details dir="rtl">
    <summary>بررسی ایمیل</summary>
    <br>
    ایمیل صحیح قبول میکند
    <br>
    نمونه صحیح: majidh1@live.com, a@b.com
    <br>
    <br>

```js
^[\w-\.]+@([\w-]+\.)+[\w-]{2,4}$
```
</details>

<details dir="rtl">
    <summary>شماره موبایل ایران</summary>
    <br>
    

<details dir="rtl">
    <summary>شماره موبایل ایران - داخلی</summary>
    <br>
    شماره موبایل صحیح قبول میکند و با 09 شروع میشود
    <br>
    نمونه صحیح: 09012345678, 09121234567
    <br>
    <br>

```js
^09\d{9}$
```
</details>


<details dir="rtl">
    <summary>شماره موبایل ایران - خارجی</summary>
    <br>
    شماره موبایل صحیح قبول میکند و با +989 شروع میشود
    <br>
    نمونه صحیح: +989012345678, +989121234567
    <br>
    <br>

```js
^\+989\d{9}$
```
</details>


<details dir="rtl">
    <summary>شماره موبایل ایران - داخلی یا خارجی</summary>
    <br>
    شماره موبایل صحیح قبول میکند و یا با +98 شروع میشود یا با 0
    <br>
    نمونه صحیح: +989012345678, 09351234567
    <br>
    <br>

```js
^(\+98|0)?9\d{9}$
```
</details>

</details>
    
<details dir="rtl">
    <summary>بررسی کد پستی</summary>
    <br>
    کدپستی شامل 10 رقم میباشد فقط اعداد قابل قبول است
    <br>
    نمونه صحیح: 6317836531, 5614793457, 3715659319
    <br>
    <br>

```js
\b(?!(\d)\1{3})[13-9]{4}[1346-9][013-9]{5}\b
```
</details>

<details dir="rtl">
    <summary>بررسی تاریخ شمسی</summary>
    <br>
    تاریخ شمسی صحیح قبول میکند و بین اعداد / هست این regex سال‌های غیر مرسوم را پوشش نمیدهد
    <br>
    نمونه صحیح: 1371/10/08, 1471/12/29, 1271/01/01, 1571/05/11, 1329/08/25
    <br>
    <br>

```js
^1[2-5]\d{2}/((0[1-6]/((3[0-1])|([1-2][0-9])|(0[1-9])))|((1[0-2]|(0[7-9]))/(30|([1-2][0-9])|(0[1-9]))))$
```
</details>

<details dir="rtl">
    <summary>بررسی کد ملی</summary>
    <br>
    کد ملی 10 رقمی و فقط عدد قبول میکند به دلیل داشتن الگوریتم در کد ملی با ریجکس به تهنایی نمی‌توان کد ملی را اعتبار سنجی کرد برای بررسی صحیح بودن کد ملی از <a href="https://github.com/majidh1/iranianNationalCode/blob/main/src/iranianNationalCodeValidator.js">این ریپو</a> میتوانید استفاده کنید
    <br>
    نمونه صحیح: 0011234554, 2569871231
    <br>
    <br>

```js
^[0-9]{10}$
```
</details>

<details dir="rtl">
    <summary>فقط حروف فارسی</summary>
    <br>
    حروف فارسی قبول میکند شامل تمامی کاراتر‌های قابل استفاده در متون فارسی
    <br>
    نمونه صحیح: سلام, ضصثقفغعهخحجچچچچچچچچچچچپگکمنتالبیسشظطزرذدئوريالًٌٍـآۀَُِّءأإؤژية
    <br>
    <br>

```js
^[\u0600-\u06FF\s]+$
```
</details>

<details dir="rtl">
    <summary>فقط اعداد فارسی</summary>
    <br>
    فقط اعداد فارسی قبول میکند
    <br>
    نمونه صحیح: ۰۱۲۳۴۵۶۷۸۹, ۹۵۹۱۲۰۰۰۰۶۳۳
    <br>
    <br>

```js
^[۰۱۲۳۴۵۶۷۸۹]+$
```
</details>

<details dir="rtl">
    <summary>آدرس سایت - URL</summary>
    <br>
    یک آدرس سایت معتبر قبول میکند
    <br>
    نمونه صحیح: https://stackoverflow.com/, http://stackoverflow.com, http://google.com/test, https://github.blog
    <br>
    <br>

```js
https?://(www\.)?[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)
```
</details>

