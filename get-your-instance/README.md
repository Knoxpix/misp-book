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

#### Import Appliance

In VirtualBox use the "Import Appliance..." functionality to import the virtual machine.

![Import Appliance...](figures/importApp.png)

The instructions in this manual covers VirtualBox only. If you prefer another virtualization solution like VMWare you can find some quick instruction on the [MISP training materials page](https://www.circl.lu/services/misp-training-materials/ "MISP training materials page").

#### MISP VM Credentials

The MISP image is pre-configured to be reachable on the private IP address **192.168.56.50** by SSH. The GUI is reachable by [http://192.168.56.50/](http://192.168.56.50/).

You should have two interfaces on your VirtualBox configuration \(NAT and host-only\). You can also configure access to the MISP instance by doing port forwarding on the NAT interface.

MISP credentials:

* **GUI Admin:** admin@admin.test:admin  \(it's the site admin account with full rights, feel free to create other users\)
* **Shell/SSH:** misp : Password1234

#### Potential issues

During life trainings we see in rare cases that some users could not reach the virtual machine over the virtual network.

Some investigations discover that this always happens with user whom already had VirtualBox in use before and had already one or more **Host-only Adapter** configured in advance.

The MISP image is pre-configured to use **Host-only Adapter** with the Name **vboxnet0**.

![Host-only Adapter vboxnet0](figures/host-only-1.png)

If this is already occupied by previous VirtualBox projects, try to attach the network adapter to the next available **Host-only** network.

![Host-only Adapter vboxnet0](figures/host-only-2.png)

