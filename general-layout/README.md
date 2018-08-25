<!-- Nothing else matters -->

## มุมมองทั่วไป

### เมนูหลัก

#### มุมมองผู้ใช้งาน
![This is the main menu that will be accessible from all of the views. In some instances, some additional buttons that will appear on top of these when a view provides it.](figures/MenuBarUser.jpg)<br>
เมนูนี้มีฟังก์ชันหลักทั้งหมดของแอปพลิเคชันเป็นชุดเมนูแบบเลื่อนลง ซึ่งประกอบไปด้วยฟังก์ชันย่อยๆ ที่ถูกจัดเป็นหมวดหมู่ดังต่อไปนี้

*   **Home button:** ปุ่มนี้จะกลับไปยังหน้าจอเริ่มต้นของแอ็พพลิเคชัน
*   **Event Actions:** เมนูของเหตุการณ์ ช่วยให้สามารถเข้าถึงฟังก์ชันทั้งหมดที่เกี่ยวข้องกับการสร้าง แก้ไข ลบ แผยแพร่ ค้นหา และแสดงเหตุการณ์และแอ็ตทริบิวต์.
*   **Input Filters:** ตัวกรองการนำเข้าข้อมูล เป็นส่วนที่จะบอกว่าข้อมูลอะไรจะนำเข้าได้ หรือจะนำเข้าข้อมูลได้อย่างไร<br>
นอกเหนือจากการตรวจสอบความถูกต้องเบื้องต้นของการระบุแอตทริบิวต์ตามแต่ละประเภทแล้ว ผู้ดูแลระบบยังสามารถกำหนดรูปแบบของ Regex เพื่อใช้ในการเปลี่ยนแปลงข้อมูล หรือปิดกั้นค่าบางอย่างในการส่งออกข้อมูล ผู้ใช้งานทั่วไปสามารถเข้ามาดูได้ว่าผู้ดูแลระบบ ได้กำหนดค่าเหล่านั้นไว้เช่นไร
*   **Global Actions:** เมนูนี้ช่วยให้คุณเข้าถึงข้อมูลเกี่ยวกับ MISP และอินสแตนซ์นี้ คุณสามารถดูและแก้ไขโปรไฟล์ของคุณเองดูคู่มืออ่านข่าวหรือข้อกำหนดในการให้บริการอีกครั้งดูรายชื่อองค์กรที่ใช้งานได้ในกรณีนี้และสร้างฮิสโตแกรมของการมีส่วนร่วมตามประเภทแอตทริบิวต์
เมนูนี้จะให้ข้อมูลเกี่ยวกับข้อมูลที่เกี่ยวกับแอปพลิเคชัน โดยผู้ใช้งานสามารถดู แก้ไขข้อมูลของผู้ใช้เอง ดูคู่มือ อ่านข่าว หรือข้อกำหนดการใช้งาน ข้อมูลหน่วยงานที่เกี่ยวข้อง และรูปแบบแอ็ตทริบิวต์
*   **Discussions:** ไปยังหัวข้อการสนทนา.

#### มุมมองผู้ดูแล
![Some additional buttons that will appear on top of these when a view provides it.](figures/MenuBarAdmin.jpg)
*   **Home button:** ปุ่มนี้จะกลับไปยังหน้าจอเริ่มต้นของแอ็พพลิเคชัน

*   **Event Actions:** เมนูของเหตุการณ์ ช่วยให้สามารถเข้าถึงฟังก์ชันทั้งหมดที่เกี่ยวข้องกับการสร้าง แก้ไข ลบ แผยแพร่ ค้นหา และแสดงเหตุการณ์และแอ็ตทริบิวต์

*   **Input Filters:** ตัวกรองการนำเข้าข้อมูล เป็นส่วนที่จะบอกว่าข้อมูลอะไรจะนำเข้าได้ หรือจะนำเข้าข้อมูลได้อย่างไร<br>
นอกเหนือจากการตรวจสอบความถูกต้องเบื้องต้นของการระบุแอตทริบิวต์ตามแต่ละประเภทแล้ว ผู้ดูแลระบบยังสามารถกำหนดรูปแบบของ Regex เพื่อใช้ในการเปลี่ยนแปลงข้อมูล หรือปิดกั้นค่าบางอย่างในการส่งออกข้อมูล ผู้ใช้งานทั่วไปสามารถเข้ามาดูได้ว่าผู้ดูแลระบบ ได้กำหนดค่าเหล่านั้นไว้เช่นไร

*   **Global Actions:** เมนูนี้ช่วยให้คุณเข้าถึงข้อมูลเกี่ยวกับ MISP และอินสแตนซ์นี้ คุณสามารถดูและแก้ไขโปรไฟล์ของคุณเองดูคู่มืออ่านข่าวหรือข้อกำหนดในการให้บริการอีกครั้งดูรายชื่อองค์กรที่ใช้งานได้ในกรณีนี้และสร้างฮิสโตแกรมของการมีส่วนร่วมตามประเภทแอตทริบิวต์

*   **Sync Actions:** ด้วยสิทธิของผู้ดูแล จะแสดงรายการระบบที่ได้ทำการเชื่อมโยงไว้กับเครือข่ายที่อนุญาตให้ส่งหรือรับข้อมูลแลกเปลี่ยนซึ่งกันและกัน

*   **Administration:** ผู้ดูแลสามารถเพิ่ม แก้ไข ลบบัญชีผู้ใช้ หรือบทบาทหน้าที่ บทบาทหน้าที่เป็นตัวกำหนดให้ว่าผู้ใช้งาน สามารถเข้าถึงการทำงานใดได้บ้าง 
ผู้ดูแลระบบยังสามารถเข้าถึงข้อมูลการติดต่อ ตั้งรหัสผ่านผู้ใช้งานใหม่ หรือสร้างช่องทางการติดต่อปลอดภัยผ่านอีเมล์ที่เข้ารหัส

*   **Audit:** ในกรณีที่มีสิทธิตรวจสอบ จะสามารถดูบันทึึกเหตุการณ์ในองค์กรนั้น ๆ หรือถ้าเป็นผู้ดูแลระบบ จะสามารถดูบันทึกเหตุการณ์ทั้งหมดได้ หรือค้นหาเหตุการณ์เพื่อเจาะจงสิ่งที่ต้องการค้นหา

*   **Log out:** ออกจากระบบ.

### รายการในชุดเมนูแบบเลื่อนลง

##### Event actions

![List Event Actions](figures/EventActions.jpg)
*   **List Events:** 
แสดงเหตุการณ์ทั้งหมดในระบบโดยไม่มีการกรองความเป็นส่วนตัวหรือหน่วยงานใด สามารถเพิ่ม แก้ไข ลบ เผยแพร่ หรือดูรายละเอียดของแต่ละเหตุการณ์ได้ที่เมนูนี้

*   **Add Event:** อนุญาตให้กรอกแบบฟอร์มการสร้างกิจกรรม และสร้างอ็อบเจ็กต์เหตุการณ์ ก่อนจะเริ่มต้นเพิ่มแอตทริบิวต์

*   **List Attributes:** แสดงรายการแอตทริบิวต์ทั้งหมดโดยไม่มีการกรองความเป็นส่วนตัวหรือหน่วยงานใด สามารถเพิ่ม แก้ไข ลบ เผยแพร่ หรือดูรายละเอียดของแต่ละแอตทริบิวต์ได้ที่ส่วนนี้

*   **Search Attributes:** ส่วนค้นหาแอตทริบิวต์ตามเงื่อนไขที่ต้องการ

*   **View Proposals:** แสดงคำขอที่มีสิทธิในการเข้าถึง.

*   **Events with proposals:** แสดงเหตุการณ์ทั้งหมดที่ถูกสร้างโดยหน่วยงานที่สังกัดที่คำขอยังไม่ถูกพิจารณา

*   **List Tags:** แสดงรายการแท็กทั้งหมดที่สร้างขึ้นโดยผู้ใช้ที่มีสิทธิ์ในการสร้างแท็ก

*   **Add Tag:** สร้างแท็กใหม่

*   **List Templates:** แสดงรายการต้นแบบที่สร้างขึ้นโดยผู้ใช้ที่มีสิทธิ์ในการสร้าง

*   **Add Template:** สร้างต้นแบบ

*   **Export:** ส่งออกข้อมูลที่สามารถเข้าถึงได้ในรูปแบบต่างๆ

*   **Automation:** ถ้ามี authentication key access, you สามารถดูวิธีใช้คีย์เพื่อใช้อินเทอร์เฟซ REST สำหรับระบบอัตโนมัติได้

##### Input filters

![Input filters](figures/InputFilter.png)

*   **Import Regexp:** You can view the Regular Expression rules, which modify the data that can be entered into the system. This can and should be used to help filter out personal information from automatic imports (such as removing the username from windows file paths), having unified representation for certain common values for easier correlation or simply standardizing certain input. It is also possible to block certain values from being inserted. As a site administrator or a user with regex permission, you can also edit these rules.

*   **Signature Whitelist:** You can view the whitelist rules, which contains the values that are blocked from being used for exports and automation on this instance. Site administrators have access to editing this list.

*  **List Warninglists:**
MISP warninglists are lists of well-known indicators that can be associated to potential false positives, errors or mistakes. The warning lists are integrated in MISP to display an info/warning box at the event and attribute level.

##### Global Actions


![Global Actions](figures/GlobalActions.png)

*   **News:** Read about the latest news regarding the MISP system

*   **My Profile:** Manage your user account.

*   **Dashboard:** allow you to see your Notifications of Proposals, Events with proposals and Delegation request. Your can see the last changes since your last visit, as Events updates and Events publications.

*   **Members List:** View the number of users per organization and get some statistics about the currently stored attributes.

*   **Organizations:** View the organizations having a presence on this instance, with some useful informations as contact's name.

*   **Role Permissions:** You can view the role permissions here.

*  **List Sharing Groups:** You can view the list of existing Sharing Groups who you or your organization have access.

*  **Add Sharing Group:** You can create a sharing group.

*   **User Guide:** A link to this user guide.

*   **Statistics:** View a series of statistics about the users and the data on this instance.


##### Sync Actions


![Sync Actions](figures/SyncActions.png)

*   **List Servers:** Connect your MISP instance to other instances, or view and modify the currently established connections.
<!-- Fix provided by elhoim -->
It may be that you have an Error Message in the page (if you enabled debug or site_admin_debug settings). An example of error message:

![Error message](figures/pb-list-server.png)

An easy first step to make most of them go away is to use the clean cache feature on the server settings menu, diagnostics tab.

![cleanscript](figures/cleanscript1.png)

You must then scroll down the page.

![cleanscript](figures/cleanscript2.png)


*  **List Feeds:** Follow the RSS feeds of other organization or CERTs worldwide.  

##### Administration

![Administration](figures/Administration.png)

*   **List Users:** View, modify or delete the currently registered users.

*   **New User:** Create an account for a new user for your organisation. Site administrators can create users for any organisation.

*  **Contact Users:** You can use this view to send messages to your current or future users or send them a temporary password.

When adding a new user to the system, or when you want to manually reset the password for a user, just use the "Send temporary password" setting.

After selecting the action, choose who the target of the e-mails should be (all users, a single user or a user not yet in the system).

You can then specify (if eligible) what the e-mail address of the target is (for existing users you can choose from a dropdown menu).

In the case of a new user, you can specify the future user's GnuPG key, to send his/her new key in an encrypted e-mail.

The system will automatically generate a message for you, but it is also possible to write a custom message if you tick the check-box, but don't worry about assigning a temporary password manually, the system will do that for you, right after your custom message.

*  **List Organizations:** View the organizations having a presence on this instance, with some useful informations.

*  **Add Organization:**

*   **List Roles:** List, modify or delete currently existing roles.

*   **Add Role:** Create a new role group for the users of this instance, controlling their privileges to create, modify, delete and to publish events and to access certain features such as the logs or automation.

*   **Administrative Tools:** Various tools, upgrade scripts that can help a site-admin run the instance.

*   **Server Settings:** Set up and diagnose your MISP installation.

*   **Jobs:** View the background jobs and their progress

*   **Scheduled Tasks:** Schedule the pre-defined tasks for your instance (this currently includes export caching, server pull and server push).

##### Audit

![Audit](figures/Audit.png)
*   **List Logs:** View the logs of the instance.
*   **Search Logs:** Search the logs by various attributes.

##### Discussions

*   **List Discussions:** List all of the discussion threads.
*   **Start Discussion:** Create a new discussion thread.

### The left bar

This bar changes based on each page-group. The blue selection shows you what page you are on.
