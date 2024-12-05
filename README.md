# Proxy Packet Redirector for Free Fire

هذا سكريبت هو وكيل SOCKS5 مكتوب بلغة C++، يتم استخدامه لإعادة توجيه حزم البيانات التي تبدأ بالقيمة `0x1200` (بصيغة Hex) وتكرارها. تم تصميم هذا المشروع ليعمل مع لعبة **Free Fire** باستخدام تطبيق **PcapDroid** لالتقاط الحزم وإعادة توجيهها.

---

## المميزات
1. **دعم SOCKS5 Proxy**:
   - يدعم المصادقة باستخدام اسم مستخدم وكلمة مرور.
   - يقوم بإعادة توجيه الحزم بين العميل والخادم.

2. **معالجة الحزم**:
   - يراقب الحزم التي تبدأ بالقيمة `0x1200`، يسجلها ويعيد إرسالها.

3. **التكامل مع لعبة Free Fire**:
   - يمكن استخدامه لتحليل الحزم القادمة من اللعبة أو تحسين الشبكة.

4. **التكامل مع PcapDroid**:
   - يعمل مع تطبيق **PcapDroid** على جهاز الأندرويد لالتقاط وإعادة توجيه الحزم عبر الوكيل.

---

## المتطلبات
- [termux](https://play.google.com/store/apps/details?id=com.termux) (لتشغيل السكريبت). 
- [PcapDroid](https://play.google.com/store/apps/details?id=com.emanuelef.remote_capture) (لتوجيه حزم الشبكة من جهاز الأندرويد إلى الوكيل).

---

## خطوات التشغيل

### إفتح تطبيق termux
1. تثبيت الأدوات اللازمة:
    ```bash
    apt install clang
 2. استنساخ المستودع:
    ```bash
    cd && git clone https://github.com/UltraV5/Spam.git
3. الانتقال إلى مجلد المشروع:
    ```bash
    cd Spam
4. تشغيل السكريبت:
    ```bash
    chmod    +x spam && ./spam
5. أثناء تشغيل السكريبت ومعالجة البيانات، قد تظهر السجلات التالية:

    ```arduino
    Handling new client
    Client authenticated
    Connection established with 192.168.1.10:8080
    Client to Server (8080): 1200aabbccdd
    Server to Client (8080): 1200ffee1122
    Connection closed
