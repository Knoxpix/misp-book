## รับอินสแตนซ์ MISP ของคุณเอง

ความตั้งใจของบทนี้คือการสนับสนุนคุณในการเริ่มใช้งานอินสแตนซ์ MISP ของคุณเอง

### MISP Virtual Machine

CIRCL ดูแล image ของ VM MISP ล่าสุด.

เป็นวิธีการที่ง่ายที่สุด, เหมาะสำหรับการทดลองใช้งานและสนับสนุนการฝึกอบรม

The images is updated on a regular base. You should frequently re-visit the online resources to get the latest versions including bug fixes and new features.

#### MISP VM Download

ในการรับเครื่อง VM MISP เวอร์ชั่นล่าสุดรวมทั้งเอกสารการฝึกอบรมทั้งหมดที่มีอยู่คือ [MISP training materials page](https://www.circl.lu/services/misp-training-materials/ "MISP training materials page") บนเว็บไซต์ CIRCL

1. เข้า [CIRCL homepage](https://www.circl.lu/ "CIRCL homepage")
2. ไปที่ [Training area](https://www.circl.lu/services/training/ "Training area")
3. คลิก [MISP Malware Information Sharing Platform - Threat Sharing](https://www.circl.lu/services/training/#misp-malware-information-sharing-platform-threat-sharing "Malware Information Sharing Platform")
4. ไปที่ลิงค์ [Training materials freely available](https://www.circl.lu/services/misp-training-materials/ "MISP training materials page")

ดาวน์โหลด VM และตรวจสอบ SHA512 fingerprint.

#### การนำเข้า

ใน VirtualBox ไปที่ "Import Appliance..." เพื่อที่จะนำเข้า VM.

![Import Appliance...](figures/importApp.png)

คำแนะนำในคู่มือฉบับนี้ครอบคลุม VirtualBox เท่านั้น ถ้าคุณต้องการโซลูชันเสมือนอื่นเช่น VMWare คุณสามารถหาคำแนะนำอย่างรวดเร็วใน [MISP training materials page](https://www.circl.lu/services/misp-training-materials/ "MISP training materials page").

#### MISP VM Credentials

MISP ได้รับการกำหนดค่าล่วงหน้าเพื่อให้สามารถเข้าถึงได้บนที่อยู่ IP ส่วนตัว **192.168.56.50** ทาง SSH. GUI สามารถเข้าถึงได้โดย [http://192.168.56.50/](http://192.168.56.50/).

คุณควรมีอินเทอร์เฟซสองตัวในคอนฟิกูเรชัน VirtualBox \(NAT และโฮสต์เท่านั้น\) นอกจากนี้คุณยังสามารถกำหนดค่าการเข้าถึงอินสแตนซ์ของ MISP ได้ด้วยการทำ port forward บนอินเทอร์เฟซ NAT

MISP credentials:

* **GUI Admin:** admin@admin.test:admin  \(เป็นบัญชีผู้ดูแลไซต์ที่มีสิทธิ์เต็มรูปแบบคุณสามารถสร้างผู้ใช้รายอื่นได้\)
* **Shell/SSH:** misp : Password1234

#### Potential issues

ในระหว่างการฝึกอบรมสดเราพบว่าในบางกรณีผู้ใช้บางรายไม่สามารถเข้าถึงเครื่องเสมือนผ่านเครือข่ายเสมือนได้

การตรวจสอบบางอย่างพบว่าเหตุการณ์นี้เกิดขึ้นกับผู้ใช้ที่มี VirtualBox อยู่แล้วและมีอะแดปเตอร์ **Host-only** ที่กำหนดไว้ล่วงหน้าอย่างน้อยหนึ่งตัว

MISP ได้รับการกำหนดค่าไว้ล่วงหน้าเพื่อใช้ตัวแปลงเฉพาะโฮสต์กับอะแดปเตอร์ชื่อ vboxnet0

![Host-only Adapter vboxnet0](figures/host-only-1.png)

ถ้า VirtualBox นี้ถูกครอบครองอยู่แล้วให้ลองต่ออะแดปเตอร์เครือข่ายกับเครือข่าย Host-only ที่มีอยู่ถัดไป

![Host-only Adapter vboxnet0](figures/host-only-2.png)

