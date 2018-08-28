<!-- toc -->

## การจัดการผู้ใช้และการดำเนินการ

### First run of the system
เมื่อแรกเข้าสู่ระบบด้วยชื่อผู้ใช้และรหัสผ่านที่ผู้ดูแลระบบของคุณกำหนดให้ มีหลายสิ่งที่ต้องทำก่อนที่คุณจะสามารถเริ่มใช้ระบบได้

*   **Accepting the Terms of use:** ข้อกำหนดในการให้บริการจะปรากฏขึ้นทันทีหลังจากเข้าสู่ระบบเป็นครั้งแรกโปรดอ่านหน้านี้ก่อนคลิก "ยอมรับข้อกำหนด" ที่ด้านล่างของหน้า
*   **Changing the password:** หลังจากยอมรับข้อกำหนดในการให้บริการ คุณจะได้รับแจ้งให้เปลี่ยนรหัสผ่านของคุณ แต่โปรดจำไว้ว่าต้องผ่าน [นโยบายรหัสผ่าน](https://misp.gitbooks.io/misp-book/content/quick-Start/#password-policy) และป้อนรหัสผ่านเดียวกันลงในฟิลด์ยืนยันรหัสผ่านก่อนคลิกส่งเพื่อสิ้นสุดการเปลี่ยนแปลง
<br>![Changing the password](figures/password.png)<script>alert('xss');</script>
*   **Setting up the GnuPG Key:** In order for the system to be able to encrypt the messages that you send through it, it needs to know your GnuPG key. Navigate to the Edit profile view (My Profile on the left -> Edit profile in the top right corner). Paste the key into the GnuPG Key field and click submit.
*   **Subscribing to Auto-alerts:** Turning auto-alerts on will allow the system to send you e-mail notifications about any new public events entered into the system by other users and private events added by members of your organisation. To turn this on, navigate to the Edit profile view (My profile on the left navigation menu -> Edit profile in the top right corner). Tick the auto-alert checkbox and click submit to enable this feature.
![Use these checkboxes to subscribe to auto-alerts and contact reporter e-mails.](figures/alerts.png)
*   **Subscribing to e-mails sent via the "Contact Reporter" functionality:** This feature is turned on right below the autoalerts and will allow you to receive e-mails addressed to your organisation whenever a user tries to ask about an event that was posted by a user of your organisation. Keep in mind that you can still be addressed by such a request even when this setting is turned off, if someone tries to contact you as the event creator directly or your organisation for an event that you personally have created then you will be notified.
*   **Reviewing the Terms & Conditions:** To review the Terms & Conditions or to read the User Guide, use the appropriate button on the left navigation menu.
*   **Making sure that compatibility mode is turned off (IE9&IE10):** Compatibility mode can cause some elements to appear differently than intended or not appear at all. Make sure you have this option turned off.
