<style> 
 @import url(https://fonts.googleapis.com/css?family=Katibeh);
 div, p, h1, h2 {
   font-family: 'Katibeh', cursive;
   direction: rtl;
 }
</style>

<h1> فونت‌های وب </h1>
<p>
ایجاد و بهبود فونت‌های وب در سال‌های اخیر کیفیت و گوناگونی را در طراحی‌های وب به همراه داشته است. تا پیش از آن، طراحان مجبور به استفاده از فونت‌های استاندارد که در هر کامپیوتری موجود است بودند و در صورتی که می‌خواستند فونت خاصی در قسمتی استفاده شود باید آن را در فوتوشاپ طراحی کرده و به صورت عکس در صفحه‌ی وب قرار می‌دادند. اما با فونت‌های وب می‌توان از هزاران فونت که در سرورهای مبتنی بر وب قرار دارند استفاده نمود و آن‌ها را روی مرورگر رایانه‌ی کاربر بارگیری کرد. بدین ترتیب شرکت‌های مختلف می‌توانند از فونت‌هایی که با برند آن‌ها سازگاری دارد استفاده کنند، خوانایی افزایش می‌یابد، تنوع در طراحی و شکل ظاهری وب‌سایت‌ها به وجود می‌آید، در دستگاه‌ها با رزولوشن‌های مختلف مانند موبایل و لپ‌تاپ و …  صفحه‌ی وب می‌تواند ظاهر یک شکل داشته باشد و … به علاوه با گسترش استفاده از این فونت‌ها، بهینه‌سازی آن‌ها انجام می‌گیرد و سربار را نیز کاهش می‌دهند. مثال فونت‌های وب، فونت‌های گوگل و font-awesome است.
</p>
<h1> بهینه‌سازی Font Awesome </h1>
<p>
در این بین Font Awesome در بیش از ۷۳ میلیون وب‌سایت استفاده می‌شود بنابراین هر بایت آن نیز می‌تواند تاثیر به‌سزایی در حجم ترافیک مصرفی داشته‌باشد. از جمله بهینه‌سازی‌هایی که می‌توان بر روی این فونتِ‌وب اعمال کرد، به مواردی اشاره می‌کنیم. 
به عنوان اولین مورد، می‌توان شاخص units-per-em را در این مجموعه‌فونت کاهش داد.  
یکی از واحدهای اندازه‌گیری سایز فونت در css، واحد em است. مربع em به مربعی گفته می‌شود که هر ضلع آن ۱ em است. در font-face، پارامتری به نام units-per-em وجود دارد که مقدار آن تعیین می‌کند هر مربع em، به چند واحد تقسیم شود. برای مثال اگر units-per-em برابر ۲۰۴۸ باشد، و سایز فونت 16px در font-face داده شده‌باشد، یعنی هر پیکسل از یک شبکه‌ی ۱۲۸*۱۲۸ ایجاد شده است که جزئیات زیادی را به نمایش خواهد گذاشت. (2048/16 = 128) 
مقدار پیش‌فرض units-per-em برای Font Awesome برابر ۱۷۹۲ است که اگر آن را تا ۲۵۶ کاهش دهیم هیچ تغییر محسوسی در ظاهر فونت‌ها ایجاد نمی‌شود اما همین تغییر ۱۵ کیلوبایت از حجم فایل فونت می‌کاهد.
</p>
![differences!](https://pixelambacht.nl/img/font-awesome-fixed/fa-unitsperem.gif)
<p>
مورد دوم، حذف کدهای اضافه از فایل است. ابزارهایی که فونت‌ها را می‌سازند، بخش‌هایی را به آن اضافه می‌کنند که عموما به کار نمی‌آیند. برای مثال می‌توان با حذف جداول قدیمی و از هر جدول داده‌های بی‌استفاده، تا ۹ کیلوبایت از حجم فایل کاست. 


سومین مورد آن است که فقط تعدادی دستگاه قدیمی اندروید نیاز دارند با فرمت‌های OTF یا TTF کارکنند و مرورگرها از فرمت‌های WOFF و WOFF2 پشتیبانی می‌کنند پس عملا در فونت‌های‌ وب‌ بی‌استفاده اند. با فشرده‌سازی فایل TTF کنونی با ابزار <a href="https://github.com/bramstein/sfnt2woff-zopfli">zopfli</a>، و ساخت فایل‌های WOFF و WOFF2 به ترتیب ۲۶ و ۱۸ کیلوبایت از حجم فایل کاسته می‌شود.

به عنوان آخرین مورد و شاید بهترین راه بهینه‌سازی، می‌توان به حذف آیکون‌های بلااستفاده اشاره کرد. برای پروژه با توجه به آیکون‌های مورد نیاز می توان از زیرمجموعه‌ای از ۶۷۵ آیکون آن استفاده نمود که بهبود قابل توجهی ایجاد خواهد کرد.
با فرض آن که روزانه ۱۰۰۰نفر از این ۷۳میلیون وب‌سایت بازدید کنند که در مرورگر آن‌ها فایل‌های ایستا ذخیره نشده‌است، و فایل فونت را تا ۲۶ کیلوبایت بهینه کرده باشیم، در صرفه‌جویی به عدد ۲ ترابایت خواهیم رسید:
</p>
73,000,000 sites × 1,000 visitors × 26 kilobytes = 1,898 terabytes
<h1> تحلیل </h1>
<p>

</p>

You can use the [editor on GitHub](https://github.com/mhadadi/research/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# ۲ترابایت صرفه‌جویی روزانه در اینترنت
##  با بهینه‌سازی font-aweome
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/mhadadi/research/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
