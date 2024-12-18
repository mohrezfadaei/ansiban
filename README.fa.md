# انسی‌بان

**انسی‌بان** ابزاری مبتنی بر انسیبل است که به شما کمک می‌کند به‌سرعت و به‌راحتی [مرزبان](https://github.com/Gozargah/Marzban) را آماده و مستقر کنید.

## زبان‌های موجود

- [فارسی (Persian)](README.fa.md) ✅
- [English](https://github.com/mohrezfadaei/ansiban)
- [中文 (Chinese)](README.ch.md)

## شروع سریع

برای شروع با انسی‌بان، مراحل زیر را دنبال کنید:

### ۱. به‌روزرسانی فایل اینونتوری

فایل اینونتوری [`hosts.ini`](inventory/hosts.ini) را ویرایش کنید تا پیکربندی‌های مستر و نود خود را اضافه کنید:

- **نام‌های نود**: می‌توانید نام نودها (مثلاً `node1`، `node2`، `node3`) را به نام‌های دلخواه مانند `germany1` تغییر دهید. (اختیاری)
- **`ansible_host`**: آدرس IP سرور خود را برای اتصال از طریق SSH تنظیم کنید. (ضروری)
- **`ansible_user`**: نام کاربری که برای دسترسی به سرور از طریق SSH استفاده می‌کنید را مشخص کنید. (ضروری)
- **`ansible_ssh_private_key_file`**: مسیر کلید خصوصی SSH خود را برای دسترسی به سرورها وارد کنید. (ضروری)

### ۲. تنظیم متغیرهای مستر

فایل [`master.yml`](group_vars/master.yml) را ویرایش کنید تا پیکربندی دلخواه خود برای استقرار مرزبان را اعمال کنید:

- **`marzban_subscription_subdomain`**: این متغیر باید زیردامنه پنل مرزبان شما باشد (فقط قسمت زیردامنه و نه کل دامنه). (ضروری)

    > مثال:
    >
    > ✅ `sub`
    >
    > ❌ `sub.mydomain.com`

- **`marzban_domain`**: نام دامنه موردنظر برای استقرار مرزبان را مشخص کنید (مثلاً `mydomain.com`). (ضروری)
- **`marzban_sub_profile_title`**: عنوان سازمان یا زیربخش خود را تنظیم کنید. (اختیاری)
- **`db_general_password`**: رمز عبور پایگاه داده MySQL خود را وارد کنید. (ضروری)

## تشکر و قدردانی

تشکر ویژه از خالقان پروژه [مرزبان](https://github.com/Gozargah/Marzban) که این ابزار الهام‌گرفته از پروژه متن‌باز آن‌ها است.

همچنین از جامعه انسیبل به خاطر مستندات عالی و پشتیبانی‌شان که در توسعه **انسی‌بان** بسیار تأثیرگذار بوده است، قدردانی می‌کنیم.

## لایسنس

این پروژه تحت مجوز آپاچی، نسخه ۲.۰ منتشر شده است.
