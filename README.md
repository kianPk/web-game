
کانواس (Canvas) در HTML5 یک عنصر گرافیکی است که امکان رسم تصاویر و انجام عملیات گرافیکی در محیط وب را فراهم می‌کند. این عنصر به توسعه‌دهندگان اجازه می‌دهد تا به صورت دینامیک و با استفاده از زبان‌های برنامه‌نویسی مانند JavaScript، تصاویر و گرافیک‌های پیچیده‌تر را ایجاد و کنترل کنند.

نحوه عملکرد کانواس:
ایجاد کانواس:
در HTML، شما یک عنصر کانواس با استفاده از تگ <canvas> ایجاد می‌کنید و به آن یک شناسه (ID) می‌دهید تا بتوانید به وسیله JavaScript به آن دسترسی پیدا کنید.

html
Copy code
<canvas id="myCanvas" width="500" height="300"></canvas>
دریافت مرجع کانواس:
در JavaScript، شما با استفاده از متد getContext می‌توانید یک مرجع به کانواس را دریافت کنید. این مرجع امکان کنترل تصاویر و عملیات گرافیکی را فراهم می‌کند.

javascript
Copy code
const canvas = document.getElementById('myCanvas');
const ctx = canvas.getContext('2d');
در اینجا، ctx یک متغیر است که به عنوان مرجع کانواس (context) عمل می‌کند.

رسم شکل‌ها:
شما می‌توانید با استفاده از متدهای fillRect، strokeRect و arc و سایر متدهای مربوط به context، اشکال مختلفی را روی کانواس رسم کنید.

javascript
Copy code
// مثال: رسم یک مستطیل
ctx.fillStyle = 'red';
ctx.fillRect(50, 50, 100, 75);

// مثال: رسم یک دایره
ctx.beginPath();
ctx.arc(200, 150, 50, 0, 2 * Math.PI);
ctx.fillStyle = 'blue';
ctx.fill();
ctx.closePath();
تغییر وضعیت کانواس:
شما می‌توانید با استفاده از متدهای clearRect و .clearRect و سایر متدهای مربوط به context، محتوای کنواس را پاک کنید یا ویژگی‌های گرافیکی را تغییر دهید.

javascript
Copy code
// پاک کردن کل کانواس
ctx.clearRect(0, 0, canvas.width, canvas.height);
تعامل با رویدادها:
کانواس به شما امکان می‌دهد به رویدادهای ماوس و کیبورد واکنش نشان دهید. می‌توانید با استفاده از متدهای addEventListener و دیگر متدها، به وقوع این رویدادها پاسخ دهید.

javascript
Copy code
canvas.addEventListener('click', function(event) {
  // عملیاتی که باید در پاسخ به کلیک انجام شود
});
با استفاده از این مبانی، شما می‌توانید بازی‌های گرافیکی و برنامه‌های تعاملی زیبا را با استفاده از کانواس ایجاد کنید.
