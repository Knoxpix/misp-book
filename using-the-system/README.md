<!-- toc -->

## การใช้งานระบบ

### การสร้างเหตุการณ์:

ขั้นตอนการเข้าสร้างเหตุการณ์สามารถแบ่งออกเป็น 3 ขั้นตอนคือการสร้างเหตุการณ์เองโดยการสร้างแอ็ตทริบิวต์
และสิ่งที่แนบมาและเผยแพร่.

ในขั้นตอนแรกนี้คุณจะสร้างกิจกรรมพื้นฐานโดยไม่มีแอตทริบิวต์ที่แท้จริง แต่เก็บข้อมูลทั่วไปเช่นคำอธิบายเวลาและระดับความเสี่ยงของเหตุการณ์ เมื่อต้องการเริ่มสร้างกิจกรรมให้คลิกที่ปุ่มกิจกรรมใหม่ทางด้านซ้ายและกรอกแบบฟอร์มที่คุณนำเสนอ ต้องกรอกข้อมูลต่อไปนี้:

![Fill this form out to create a skeleton event, before proceeding to populate it with attributes and attachments.](figures/add_event.png)

*   **Date:** วันที่เหตุการณ์เกิดขึ้น เพียงแค่คลิกฟิลด์นี้และตัวเลือกวันที่จะปรากฏขึ้นซึ่งคุณสามารถเลือกวันที่ที่ต้องการได้.
*   **Distribution:** การตั้งค่านี้จะควบคุมผู้ที่จะสามารถมองเห็นกิจกรรมนี้ได้เมื่อได้รับการเผยแพร่และในที่สุดเมื่อดึงออก นอกเหนือจากความสามารถในการกำหนดว่าผู้ใช้ใดในเซิร์ฟเวอร์นี้จะได้รับอนุญาตให้ดูกิจกรรมระบบจะควบคุมว่าเหตุการณ์จะถูกซิงโครไนซ์กับเซิร์ฟเวอร์เครื่องอื่นหรือไม่ การแจกแจงจะสืบทอดโดยแอตทริบิวต์: การตั้งค่าที่เข้มงวดมากที่สุดจะชนะ มีตัวเลือกดังต่อไปนี้:
  *   **Your organization only:** การตั้งค่านี้จะอนุญาตเฉพาะสมาชิกในองค์กรของคุณเท่านั้นที่จะเห็นสิ่งนี้ คุณสามารถดึงสมาชิกอื่นในองค์กรของคุณออกจากองค์กรของคุณได้เฉพาะองค์กรของคุณเท่านั้นที่สามารถดูได้ กิจกรรมที่มีการตั้งค่านี้จะไม่ถูกซิงโครไนซ์.
      
      Upon push: do not push. Upon pull : pull.
  *   **This Community-only:** ผู้ใช้ที่เป็นส่วนหนึ่งของกลุ่มองค์กร MISP ของคุณจะสามารถดูกิจกรรมได้ ซึ่งรวมถึงองค์กรของคุณองค์กรในเซิร์ฟเวอร์ MISP นี้และองค์กรที่ใช้เซิร์ฟเวอร์ MISP ที่ซิงค์กับเซิร์ฟเวอร์นี้ องค์กรอื่นที่เชื่อมต่อกับเซิร์ฟเวอร์ที่เชื่อมโยงกันเหล่านี้จะถูก จำกัด ไม่ให้เข้าร่วมกิจกรรม.
  
      Upon push: do not push. Upon pull: pull and downgrade to Your organization only.
  *   **Connected communities:** ผู้ใช้ที่เป็นส่วนหนึ่งของชุมชน MISP ของคุณจะสามารถดูกิจกรรมได้ ซึ่งรวมถึงองค์กรทั้งหมดในเซิร์ฟเวอร์ MISP นี้องค์กรทั้งหมดบนเซิร์ฟเวอร์ MISP ที่ซิงโครไนซ์กับเซิร์ฟเวอร์นี้และองค์กรโฮสติ้งของเซิร์ฟเวอร์ที่เชื่อมต่อกับเซิร์ฟเวอร์ที่กล่าวถึงข้างต้น (โดยทั่วไปเซิร์ฟเวอร์ใดก็ตามที่อยู่ห่างจากเซิร์ฟเวอร์นี้ 2 ช่วง) องค์กรอื่นที่เชื่อมต่อกับเซิร์ฟเวอร์ที่เชื่อมโยงซึ่งอยู่ห่างจากที่นี่ไป 2 ช่วง จะถูก จำกัด ให้เห็นเหตุการณ์
      Upon push: downgrade to This Community only and push. Upon pull: pull and downgrade to This Community only.
  *   **All communities:** ซึ่งจะเป็นการแบ่งปันเหตุการณ์กับชุมชน MISP ทั้งหมดทำให้สามารถเผยแพร่กิจกรรมได้อย่างเสรีจากเซิร์ฟเวอร์เครื่องหนึ่งไปยังอีก.
      Upon push: push. Upon pull: pull.
  *   **Sharing group:** กิจกรรมนี้จะแชร์กิจกรรมกับกลุ่มการแชร์ที่กำหนดไว้ ซึ่งรวมถึงเฉพาะองค์กรที่กำหนดไว้ในกลุ่มการแชร์ การกระจายสามารถเป็นแบบโลคัลและแบบไขว้กันขึ้นอยู่กับนิยามของกลุ่มการแชร์ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแชร์กลุ่มโปรดดูที่ส่วนกลุ่มการแชร์.
*   **Threat Level:** ฟิลด์นี้แสดงถึงระดับความเสี่ยงของเหตุการณ์ เหตุการณ์สามารถแบ่งได้เป็น 3 ประเภทภัยคุกคามที่แตกต่างกัน (ต่ำ, ปานกลาง, สูง) ฟิลด์นี้สามารถเลือกให้เป็นแบบไม่ระบุได้ มี 3 ตัวเลือกดังนี้:
  *  **Low:** มัลแวร์มวลทั่วไป.
  *  **Medium:** ภัยคุกคามแบบถาวรขั้นสูง (APT)
  *  **High:** APTs ที่ซับซ้อนและการโจมตี 0day.
*   **Analysis:** แสดงถึงขั้นตอนปัจจุบันของการวิเคราะห์สำหรับเหตุการณ์โดยมีตัวเลือกที่เป็นไปได้ดังต่อไปนี้:
  *  **Initial:** การวิเคราะห์เพิ่งเริ่มต้น
  *  **Ongoing:** การวิเคราะห์กำลังดำเนินการอยู่
  *  **Completed:** การวิเคราะห์เสร็จสมบูรณ์
*   **Event Description:** ช่องข้อมูลซึ่งมัลแวร์ / เหตุการณ์จะได้รับคำอธิบายสั้น ๆ โดยเริ่มจากการอ้างอิงภายใน ฟิลด์นี้ควรสั้นและกระชับมากที่สุดคำอธิบายโดยละเอียดจะเกิดขึ้นจากแอตทริบิวต์ในขั้นตอนต่อไปของการสร้างกิจกรรม โปรดทราบว่าระบบจะแทนที่สตริงข้อความที่ตรวจพบโดยอัตโนมัติซึ่งตรงกับรายการนิพจน์ทั่วไปที่ผู้ดูแลเซิร์ฟเวอร์ของคุณตั้งค่าไว้.
*   **GFI Sandbox:** สามารถที่จะอัปโหลดไฟล์. zip ที่ส่งออกจาก Sandbox GFI ด้วยความช่วยเหลือของเครื่องมือนี้ เหล่านี้จะถูกจัดการโดย MISP และรายการของแอ็ตทริบิวต์และไฟล์แนบจะถูกสร้างขึ้นโดยอัตโนมัติจากไฟล์. zip ขณะนี้งานส่วนใหญ่ที่จำเป็นต้องทำในขั้นตอนที่สองของการสร้างกิจกรรมเป็นสิ่งสำคัญที่ต้องดูข้อมูลทั้งหมดที่กำลังถูกป้อนด้วยตนเอง.

### เพิ่มแอตทริบิวต์ให้กับเหตุการณ์:

ขั้นตอนที่สองของการสร้างกิจกรรมคือการเติมข้อมูลให้มีแอตทริบิวต์และไฟล์แนบ ซึ่งสามารถทำได้โดยการเพิ่มด้วยตนเองหรือนำเข้าคุณลักษณะจากรูปแบบภายนอก (OpenIOC, ThreatConnect) หากต้องการนำเข้าจากรูปแบบภายนอกหรืออัปโหลดไฟล์แนบให้ใช้ตัวเลือกในเมนูด้านซ้าย.

![Use these tools to populate the event.](figures/attribute_tools.png)

การใช้ปุ่มที่แสดงไว้ข้างต้นคุณสามารถเติมเหตุการณ์โดยใช้เครื่องมือต่างๆที่จะอธิบายไว้ในส่วนต่อไปนี้ เริ่มต้นด้วยปุ่มเพิ่มแอตทริบิวต์

### เพิ่มแอตทริบิวต์

โปรดจำไว้ว่าระบบจะค้นหานิพจน์ทั่วไปในช่องค่าของแอตทริบิวต์ทั้งหมดเมื่อป้อนแทนที่สตริงที่ตรวจพบภายในตัวตั้งค่าดังกล่าวโดยผู้ดูแลระบบของเซิร์ฟเวอร์ (ตัวอย่างเช่นเพื่อบังคับใช้อักษรตัวพิมพ์ใหญ่ที่เป็นมาตรฐานในเส้นทางสำหรับความสัมพันธ์ของเหตุการณ์หรือเพื่อให้เส้นทางที่ถูกต้อง รูปแบบมาตรฐาน) ต้องกรอกข้อมูลต่อไปนี้:
![This form allows you to add attributes.](figures/add_attribute.png)

*   **Category:** เมนูแบบเลื่อนลงนี้จะอธิบายหมวดหมู่ของแอตทริบิวต์ซึ่งหมายถึงลักษณะของมัลแวร์ที่อธิบายถึงคุณลักษณะนี้ ซึ่งอาจหมายถึงกลไกการติดตาของมัลแวร์หรือกิจกรรมเครือข่ายเป็นต้นสำหรับรายการประเภทที่ถูกต้อง[click here](../categories-and-types)
*   **Type:** ขณะที่ประเภทระบุประเภทของเหตุการณ์ที่พวกเขากำลังอธิบายประเภทของคำอธิบายโดยสิ่งที่หมายถึงแง่มุมที่อธิบาย ตัวอย่างเช่นที่อยู่ IP ของแหล่งที่มาของการโจมตีอีเมลแอดเดรสต้นทางหรือไฟล์ที่ส่งผ่านไฟล์แนบสามารถอธิบายถึงการจัดส่งของมัลแวร์ได้ เหล่านี้จะเป็นประเภทของแอตทริบิวต์ที่มีประเภทของการจัดส่งข้อมูล สำหรับคำอธิบายประเภทของแต่ละประเภทและชนิดที่ถูกต้อง, [click here](../categories-and-types)
*   **Distribution:** รายการแบบเลื่อนลงนี้ช่วยให้คุณสามารถควบคุมว่าใครจะสามารถดูแอตทริบิวต์นี้ การแจกแจงจะสืบทอดโดยแอตทริบิวต์: การตั้งค่าที่เข้มงวดมากที่สุดจะชนะ สำหรับข้อมูลเพิ่มเติมโปรดอ่านข้อมูลการแจกจ่ายในส่วนการสร้างกิจกรรม - [click here](#creating-an-event)
*   **Contextual Comment:** เพิ่มความคิดเห็นในแอตทริบิวต์ นี้จะไม่ถูกใช้สำหรับความสัมพันธ์.
*   **Value:** ค่าที่แท้จริงของแอตทริบิวต์ให้ป้อนข้อมูลเกี่ยวกับค่าที่อิงกับสิ่งที่ถูกต้องสำหรับประเภทแอ็ตทริบิวต์ที่เลือก ตัวอย่างเช่นสำหรับแอ็ตทริบิวต์ type ip-src (ที่อยู่ IP ต้นทาง) 11.11.11.11 จะเป็นค่าที่ถูกต้อง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับประเภทและค่า [click here](../categories-and-types)
*   **Contextual Comment:** คุณสามารถเพิ่มความคิดเห็นบางส่วนไปยังแอตทริบิวต์ที่จะไม่ใช้สำหรับความสัมพันธ์ แต่แทนที่จะทำหน้าที่เป็นข้อมูลที่ให้ข้อมูลอย่างหมดจด
*   **For Intrusion Detection System:** ตัวเลือกนี้อนุญาตให้ใช้แอ็ตทริบิวต์เป็นลายเซ็น IDS เมื่อส่งออกข้อมูล NIDS เว้นแต่จะถูกครอบงำโดยรายการสีขาว สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายการที่อนุญาตพิเศษให้ไปที่ส่วน [administration](#administration).
*   **Batch import:** หากมีแอตทริบิวต์หลายชนิดที่ป้อน (เช่นรายการที่อยู่ IP คุณสามารถป้อนข้อมูลทั้งหมดลงในช่องค่าเดียวกันได้โดยคั่นด้วยเส้นแบ่งระหว่างแต่ละบรรทัด) ซึ่งจะทำให้ระบบสามารถสร้างได้ แยกบรรทัดสำหรับแต่ละแอตทริบิวต์.


### เพิ่มอ็อบเจกต์

กรุณาข้ามไปอ่านที่ [MISP-objects chapter](../misp-object/README.md)


### สร้างและจัดการกลุ่มที่ใช้ร่วมกัน

การแบ่งปันกลุ่มใน MISP เป็นวิธีที่ละเอียดมากขึ้นในการสร้างรายการการแจกจ่ายที่สามารถใช้งานได้ใหม่สำหรับเหตุการณ์ / แอตทริบิวต์ที่อนุญาตให้ผู้ใช้รวมองค์กรจากอินสแตนซ์ของตนเอง (องค์กรท้องถิ่น) รวมทั้งองค์กรจากอินสแตนซ์ที่เชื่อมต่อโดยตรงหรือโดยอ้อม (องค์กรภายนอก) กลุ่มผู้ใช้ที่มีสิทธิ์ในการแก้ไขกลุ่มผู้ใช้ร่วมกันสามารถสร้างกลุ่มที่ใช้ร่วมกันได้ นอกจากนี้การแชร์กลุ่มสามารถแก้ไขได้โดยผู้ใช้ที่มีสิทธิ์ดังกล่าวข้างต้นนอกเหนือจากการเป็นสมาชิกขององค์กรที่สร้างกลุ่มการแชร์หรือองค์กรที่มีการทำเครื่องหมายว่าเป็น "Extender" ของกลุ่มการแชร์ การใช้งานหลักสำหรับคุณลักษณะเพิ่มเติมคือการมอบหมายสิทธิ์ในการเพิ่มผู้ใช้ไปยังคู่ค้าที่เชื่อถือได้ ตัวอย่างเช่นเมื่อแบ่งปันกับภาคอุตสาหกรรมอื่นรู้ว่านักแสดงทั้งหมดที่ควรได้รับข้อมูลมักไม่สามารถทำได้ดังนั้นการมอบสิทธิ์ในการขยายกิจกรรมไปยังตัวแทนที่เชื่อถือได้ของภาคดังกล่าวจะช่วยให้ผู้ที่มีความเข้าใจมากขึ้นในการค้นหาและเพิ่ม รายชื่อคู่ค้าที่เหมาะสมสำหรับกลุ่มการแชร์

![A sample sharing group setup involving 3 instances and showing the various ways to include/exclude organisations](figures/sync.png)

กรณีการใช้งานร่วมกันโดยทั่วไปสำหรับกลุ่มการใช้งานร่วมกันกำลังสร้างกลุ่มย่อยเฉพาะหัวข้อที่สามารถใช้ซ้ำได้ใน MISP ซึ่งแบ่งใช้เหตุการณ์หรือสถานการณ์ที่ใช้ร่วมกันแบบเฉพาะกิจ (เช่นหลายองค์กรที่เกี่ยวข้องกับเหตุการณ์เฉพาะที่ต้องการทำงานร่วมกัน) โดยทั่วไปกลุ่มการแชร์จะเพิ่มระดับของความซับซ้อนสำหรับผู้ใช้ที่เกี่ยวข้องรวมถึงค่าใช้จ่ายที่มีต่อข้อมูลที่ทำเครื่องหมายไว้ด้วย

เป็นคำแนะนำที่ดีที่สุดในการปฏิบัติโดยใช้วิธีการแจกจ่ายแบบดั้งเดิมเว้นแต่จะไม่สามารถครอบคลุมกรณีการใช้งานที่ระบุได้ นอกจากนี้ในขณะที่กลุ่มการแชร์สามารถกำหนดให้กับทั้งเหตุการณ์และแอตทริบิวต์ได้ขอแนะนำให้ใช้การตั้งค่าการแจกแจง "สืบทอด" พิเศษในแอตทริบิวต์เมื่อใดก็ตามที่กลุ่มการแชร์ของแอตทริบิวต์จะตรงกับเหตุการณ์

Sharing groups consist of the following elements, each of which has its own page in the sharing group creator/editor tool (accessed via the Global actions -> List Sharing Groups and Add Sharing Group functionalities):

กลุ่มที่ใช้ร่วมกันประกอบด้วยองค์ประกอบต่อไปนี้ซึ่งแต่ละส่วนมีหน้าของตัวเองในเครื่องมือสร้าง / แก้ไขกลุ่มผู้ใช้ร่วมกัน (เข้าถึงได้ผ่านGlobal actions -> List Sharing Groups และ Add Sharing Group)

![The general tab of the sharing group tool](figures/sgpage1.png)

*  **General:** ข้อมูลเมตาที่อธิบายถึงเจตนาของกลุ่มการแชร์
  *  **Name:** ชื่อเฉพาะของกลุ่มการแชร์.
  *  **Releasable to:** คำอธิบายที่มนุษย์สามารถอ่านได้เกี่ยวกับข้อมูลที่ทำเครื่องหมายด้วยกลุ่มการแบ่งปันสามารถใช้ร่วมกันได้ ฟิลด์นี้จะไม่ถูกใช้โดย MISP สำหรับสิ่งอื่นใดนอกเหนือจากการเป็นช่องข้อมูลที่มุ่งขยายองค์กรของกลุ่มการแชร์.
  *  **Description:** การแสดงข้อความเจตนาของกลุ่มการแชร์.
  *  **Make the sharing group selectable (active):** กลุ่มการแชร์สามารถทำ passive ได้โดยยกเลิกการเลือกการตั้งค่านี้ เหตุการณ์และแอ็ตทริบิวต์ทั้งหมดจะยังคงเป็นไปตามการตั้งค่าการแจกจ่ายของกลุ่มการแชร์แบบพาสเวิร์ดอย่างไรก็ตามกลุ่มการแชร์จะไม่ถูกเสนอเป็นตัวเลือกที่สามารถเลือกได้เมื่อตั้งค่าการกระจายเหตุการณ์ / แอตทริบิวต์ แนวคิดที่อยู่เบื้องหลังนี้ก็คือกลุ่มการแชร์แบบเฉพาะกิจที่ใช้งานได้นานกว่าเป้าหมายสามารถเกษียณอายุได้เพื่อลดความยุ่งเหยิงใน UI.

![The organisations tab of the sharing group tool](figures/sgpage2.png)

*  **Organisations:** เพจที่สองของเครื่องมือประกอบด้วยรายชื่อการแจกจ่ายที่มีองค์กรทั้งหมดที่ตั้งชื่อโดยตรงในฐานะสมาชิกของกลุ่มการแชร์
  *  **Add Local/remote organisations:** องค์กรแบ่งออกเป็นสองรายการ (แสดงเป็นแท็บสองแท็บในเครื่องมือ) สำหรับองค์กรภายนอกและภายนอกที่เป็นที่รู้จักและท้องถิ่น องค์กรท้องถิ่นคาดว่าจะมีผู้ใช้แบบโลคัลอย่างน้อยหนึ่งรายในอินสแตนซ์ในขณะที่องค์กรที่ห่างไกลไม่ทำเช่นนั้น การซิงค์กับอินสแตนซ์จากระยะไกลจะสร้างองค์กรระยะไกลเมื่อใดก็ตามที่มีการรับเหตุการณ์ใหม่ ๆ ขององค์กรที่ไม่รู้จัก องค์กรที่ห่างไกลสามารถถูกแปลงเป็นองค์กรในท้องถิ่นได้ทุกเมื่อ - สิ่งนี้จะกลายเป็นเรื่องที่น่าสนใจหากผู้ใช้องค์กรภายนอกร้องขอให้เข้าถึงอินสแตนซ์ MISP ของคุณ.
  *  **Extend checkmark:** การตรวจสอบเครื่องหมายถูกต่อขยายทำให้องค์กรที่เลือกเป็นส่วนขยายของกลุ่มการแชร์ซึ่งหมายความว่าพวกเขาสามารถแก้ไขกลุ่มการแชร์ได้ คาดว่าพันธมิตรที่เชื่อถือได้เหล่านี้จะปฏิบัติตามแท็ก "releasable to" ในหน้าทั่วไป องค์กรที่สร้างกลุ่มการแชร์จะรวมอยู่ใน Extender เสมอ.

![The servers tab of the sharing group tool](figures/sgpage3.png)

*  **Servers:** หน้าเว็บที่สามของเครื่องมืออธิบายถึงอินสแตนซ์ของ MISP ข้อมูลที่ทำเครื่องหมายด้วยกลุ่มการแชร์จะให้สามารถทำข้อมูลให้ตรงกันได้ โปรดจำไว้ว่าผู้ใช้ที่สามารถดูกิจกรรมในอินสแตนซ์ที่กำหนดจะมีสิทธิ์ดึงเหตุการณ์ไปยังอินสแตนซ์ที่บ้านเนื่องจากเป็นส่วนหนึ่งของกลุ่มการแชร์อย่างไรก็ตามรายชื่อการแจกจ่ายขององค์กรจะยังคงใช้อยู่.
  *  **Enable roaming mode:** การตั้งค่านี้จะปิดการใช้งานรายชื่อเซิร์ฟเวอร์และพึ่งพาได้อย่างหมดจดในรายชื่อองค์กรเพื่อแจกจ่ายข้อมูล ถ้าองค์กรโฮสต์ของการเชื่อมต่อข้อมูลซิงค์อยู่ในรายชื่อการแจกจ่ายขององค์กรอินสแตนซ์จะมีสิทธิ์ในการซิงโครไนซ์ข้อมูลที่ทำเครื่องหมายไว้กับกลุ่มการแชร์ โดยทั่วไปการดำเนินการนี้มีความเสี่ยงสูงกว่าเล็กน้อยเนื่องจากอาศัยผู้ดูแลระบบอย่างถูกต้องในการตั้งค่าการโฮสต์องค์กร แต่จำเป็นต้องทราบว่า URL อินสแตนซ์เฉพาะที่เหตุการณ์ / แอตทริบิวต์ควรไหลออก.
  *  **Add instance:** เพิ่มอินสแตนซ์ลงในรายการแจกจ่ายจากอินสแตนซ์ซิงค์ที่ตั้งค่าไว้ภายใต้ sync actions -> servers
  *  **All orgs:** การเลือกเครื่องหมายถูกนี้จะรวมองค์กรทั้งหมดในอินสแตนซ์ที่กำหนดไว้ในกลุ่มการแชร์ ซึ่งหมายความว่าเพื่อแลกเปลี่ยนกับผู้ใช้ทั้งหมดของชุมชนที่เชื่อมโยงกันไม่จำเป็นต้องรู้ว่าทุกๆองค์กรที่อาศัยอยู่ในอินสแตนซ์นั้น นอกจากนี้ยังหมายความว่ารายการแจกจ่ายจะไม่รวมชื่อองค์กรซึ่งน่าสนใจสำหรับชุมชนที่มีความเป็นส่วนตัวบางแห่ง.

![The summary tab of the sharing group tool](figures/sgpage4.png)

*  **Summary:** เมื่อตั้งค่าเสร็จแล้ว MISP จะสรุปกลุ่มแบ่งปันในหน้าข้อความที่ไฮไลต์ซึ่งควรจะตรวจทานก่อนที่จะส่งกลุ่มการแชร์ / แก้ไขกลุ่มการแชร์ใหม่ ข้อผิดพลาดในการตั้งค่ากลุ่มการแชร์อาจนำไปสู่องค์กรที่ไม่ควรมีส่วนร่วมในกลุ่มการแชร์ที่ได้รับสิทธิ์การเข้าถึงหรือองค์กรที่ได้รับสิทธิ์การแก้ไขที่ไม่ต้องการให้กับกลุ่มการแชร์ โปรดจำไว้ว่าแม้ว่าคุณจะส่งกลุ่มการแชร์ไปแล้วก็ตามจะไม่มีการเผยแพร่จนกว่าเหตุการณ์ / แอตทริบิวต์จะได้รับกลุ่มการแชร์เป็นกลุ่มการแจกจ่ายที่เลือก.

### เติมจากแม่แบบ

เทมเพลตช่วยให้ผู้ใช้สามารถสร้างงานประเภทต่างๆได้อย่างรวดเร็วโดยกรอกข้อมูลในฟิลด์ที่กำหนดไว้ล่วงหน้า ผู้ใช้ที่มีสิทธิ์ในการสร้างเทมเพลตสามารถสร้างเทมเพลตใหม่สำหรับองค์กรของตนหรือสำหรับทุกองค์กรในอินสแตนซ์ของตนได้ หากคุณสนใจในการสร้างเทมเพลตโปรดดูหัวข้อ templating
สำหรับผู้ใช้ที่พยายามเติมเหตุการณ์หลังจากคลิกปุ่มเติมจากเทมเพลตคุณจะเห็นรายการเทมเพลตที่เข้าถึงได้ทั้งหมดในขณะนี้ เลือกรายการที่อธิบายเหตุการณ์ที่คุณกำลังสร้างได้ดีที่สุด

![Choose the most appropriate template for your event.](figures/template_choice.png)

เมื่อคุณเลือกเทมเพลตแล้วคุณจะได้รับแบบฟอร์มที่แท้จริงภายใน ตรวจสอบให้แน่ใจว่าคุณกรอกข้อมูลลงในฟิลด์ที่จำเป็นโดยกรอกข้อมูลลงในช่องที่มีเครื่องหมายดาวไว้ในวงเล็บเช่น: (*) - กรอกข้อมูลครบถ้วน
เทมเพลตจะแบ่งออกเป็นส่วน ๆ โดยแต่ละส่วนมีชื่อและคำอธิบายนอกเหนือไปจากชุดของฟิลด์ต่างๆ แต่ละฟิลด์สามารถเป็นฟิลด์แอตทริบิวต์หรือไฟล์แนบ เขตข้อมูลแอตทริบิวต์มีคอมโพเนนต์ต่อไปนี้:
![MISP will generate attributes based on the field's settings and the data that you provide.](figures/template_field.png)

*  **Field**: ชื่อของฟิลด์พร้อมกับตัวบ่งชี้ว่าเขตข้อมูลนี้มีผลบังคับใช้หรือไม่.
*  **Description**: คำอธิบายสั้น ๆ ขอฟิลลด์.
*  **Types**: ค่าที่ถูกต้องสำหรับฟิลด์ ในกรณีที่มีหลายประเภทที่แสดงในที่นี้คุณสามารถป้อนค่าที่ตรงกับประเภทใดประเภทหนึ่งหรือในกรณีของฟิลด์การนำเข้าชุดงานผสมชนิดใดก็ตามที่กำหนด.
*  **Text field**: ฟิลด์นี้สามารถเป็นช่องข้อความบรรทัดเดียวหรือพื้นที่ข้อความหลายบรรทัด สำหรับอดีตป้อนค่าเดียวของประเภทที่ระบุไว้ข้างต้นในขณะที่สำหรับหลังคุณ cna วางรายการค่าที่คั่นด้วยเส้นแบ่ง.

### Freetext Import Tool

![Just paste a line-break separated list of indicators into the freetext import tool.](figures/freetext1.png)

หากคุณมีรายการตัวบ่งชี้ที่คุณต้องการสร้างแอตทริบิวต์ได้อย่างรวดเร็วจากนั้นเครื่องมือนำเข้าข้อความฟรีคือสิ่งที่คุณต้องการเท่านั้น เพียงแค่วางรายการของตัวบ่งชี้ (คั่นด้วยเส้นแบ่งเป็นเครื่องมือนี้)

![MISP will often find several valid category/type combinations for the values. Do last minute adjustments on the result page.](figures/freetext2.png)

เนื่องจากมีการผสมผสานระหว่างประเภท / ประเภทต่างๆที่ใช้ได้สำหรับค่ามาก MISP จะแนะนำการตั้งค่าที่พบมากที่สุด คุณสามารถเปลี่ยนประเภท / ประเภท / IDS ด้วยตนเองถ้าคุณไม่เห็นด้วยกับผลลัพธ์ ตัวเลือกจะถูก จำกัด ไว้สำหรับการรวมหมวดหมู่ / ประเภทที่ถูกต้องสำหรับค่าที่คุณป้อนไว้

หากพบความสัมพันธ์ใด ๆ แล้วความสัมพันธ์เหล่านี้จะปรากฏในหน้าผลการค้นหา

### Attribute Replace Tool

หากคุณต้องการสร้างและรักษากิจกรรมด้วยชุดตัวบ่งชี้ที่ได้รับการนำออกและเพิ่มเวลาผ่านไปเครื่องมือแทนที่แอตทริบิวต์อาจทำให้งานนี้ง่ายขึ้นสำหรับคุณ

![Select a category/type combination and paste the updated list of indicators into the textarea.](figures/attribute_replace_tool.png)

เพียงเลือกประเภท / ประเภทที่ต้องการให้เลือกว่าควรทำเครื่องหมายแอตทริบิวต์สำหรับการส่งออก IDS และวางรายการดัชนีใหม่ลงในพื้นที่ทำงาน แอตทริบิวต์ของหมวดหมู่ / ประเภทเดียวกันที่มีอยู่ในเหตุการณ์ แต่ไม่ใช่รายการใหม่จะถูกนำออกค่าในรายการวางที่ยังไม่มีอยู่เนื่องจากแอตทริบิวต์จะถูกสร้างขึ้นเนื่องจากแอตทริบิวต์และค่าที่มีแอตทริบิวต์ที่ตรงกันจะไม่มีการแตะต้อง .

### Add attachments to the event:

นอกจากนี้คุณยังสามารถอัปโหลดไฟล์แนบเช่นมัลแวร์เองรายงานไฟล์จากการวิเคราะห์ภายนอกหรือสิ่งประดิษฐ์ที่ลดลงจากมัลแวร์ การคลิกที่ปุ่มเพิ่มสิ่งที่แนบมาจะแสดงฟอร์มที่ช่วยให้คุณสามารถแนบไฟล์กับกิจกรรมได้อย่างรวดเร็ว ต้องกรอกข้อมูลต่อไปนี้:
![Point the uploader to the file you want to upload. Make sure to mark it as malware if the uploaded file is harmful, that way it will be neutralised.](figures/add_attachment.png)

*   **Category:** ประเภทเดียวกันกับคุณลักษณะจะตอบคำถามเกี่ยวกับไฟล์ที่อัปโหลดมีขึ้นเพื่ออธิบาย.
*   **Distribution:**  รายการแบบหล่นลงนี้ช่วยให้คุณสามารถควบคุมว่าใครจะสามารถดูเอกสารแนบนี้ การแจกแจงจะสืบทอดโดยแอตทริบิวต์: การตั้งค่าที่เข้มงวดมากที่สุดจะชนะ สำหรับข้อมูลเพิ่มเติมโปรดดูข้อมูลการแจกจ่ายในส่วน [event section](#creating-an-event).
*   **Upload field:** โดยการกดปุ่มเรียกดูคุณสามารถเรียกดูระบบไฟล์ของคุณและชี้ผู้อัปโหลดไปยังไฟล์ที่คุณต้องการแนบไปกับแอ็ตทริบิวต์ จากนั้นจะอัปโหลดเมื่อกดปุ่มอัปโหลด.
*   **Malware:** กล่องกาเครื่องหมายนี้จะทำเครื่องหมายไฟล์เป็นมัลแวร์และจะถูกบีบอัดและรหัสผ่านเพื่อป้องกันผู้ใช้ระบบไม่ให้ดาวน์โหลดและรันไฟล์ อย่าลืมทำเครื่องหมายที่นี่หากคุณสงสัยว่ามีการติดไวรัสก่อนที่จะอัปโหลด.
*   **Contextual Comment:** คุณสามารถเพิ่มความคิดเห็นบางส่วนไปยังแอตทริบิวต์ที่จะไม่ใช้สำหรับความสัมพันธ์ แต่แทนที่จะทำหน้าที่เป็นข้อมูล.

### เสนอการเปลี่ยนแปลงกิจกรรมที่เป็นขององค์กรอื่น

หากคุณต้องการเสนอการแก้ไขแอตทริบิวต์หรือเสนอคุณลักษณะเพิ่มเติมให้กับองค์กรที่สร้างขึ้นคุณสามารถทำได้โดยใช้ปุ่มที่ใช้แทนฟิลด์ add attribute ด้านซ้ายและไอคอนแก้ไขที่ด้านขวาของแต่ละรายการ ในมุมมองเหตุการณ์ องค์กรที่สร้างขึ้นของกิจกรรมจะสามารถเห็นข้อเสนอใด ๆ และยกเลิกหรือยอมรับการเปลี่ยนแปลงได้

![An attribute with a proposal attached will turn blue and the proposal itself will be grey. If there is a grey proposal without a blue attribute infront of it, it means that someone has proposed a new attribute](figures/proposal.png)

หากองค์กรที่สร้างกิจกรรมอยู่ในเซิร์ฟเวอร์ที่เชื่อมต่ออีกรายหนึ่งพวกเขาจะสามารถยอมรับข้อเสนอได้เมื่อเริ่มต้นดึงและรับข้อเสนอของคุณ หลังจากนี้พวกเขาสามารถเผยแพร่เหตุการณ์ใหม่ได้โดยส่งแอตทริบิวต์ที่เปลี่ยนแปลงไปกลับไปที่อินสแตนซ์ของคุณ

### เติมจาก OpenIOC

นอกจากนี้ยังสามารถพยายามนำเข้าข้อมูลที่มีอยู่ในไฟล์. ioc เครื่องมือนำเข้าจะพยายามรวบรวม IndicatorItems จำนวนมากไว้ในตัวดำเนินการเชิงตรรกะซ้อนกันมากที่สุดโดยไม่ทำลายความถูกต้อง หลังจากขั้นตอนเสร็จสิ้นแล้วคุณจะเห็นรายการของแอ็ตทริบิวต์ที่สร้างเสร็จแล้วและรายการ IndicatorItems ที่ล้มเหลวรวมทั้งกราฟของไฟล์. ioc

![The import tool will list the successful and failed entries after the process is done.](figures/ioc1.png)

![You'll also be able to see a graph of the imported .ioc file and how successful the import was.](figures/ioc2.png)

### Populate from ThreatConnect

นอกจากนี้คุณยังสามารถนำเข้าข้อมูลจากไฟล์ csv ที่ส่งออก ThreatConnect คอลัมน์ต่อไปนี้ใช้โดยเครื่องมือการนำเข้า (จึงเป็นฟิลด์บังคับเพื่อเลือกในระหว่างการส่งออก):
*   Type
*   Value
*   Confidence
*   Description
*   Source

ผลลัพธ์จะเป็นรายการแอตทริบิวต์ที่เพิ่มลงในเหตุการณ์ที่เลือกในปัจจุบันแต่ละรายการจะถูกทำเครื่องหมายด้วยความคิดเห็นที่ระบุว่าแหล่งที่มานั้นมาจากการนำเข้า ThreatConnect

### Adding IOCs from a PDF report

คุณสามารถใช้สคริปต์ทั่วไปที่เรียกว่า [IOC parser](https://github.com/armbues/ioc_parser) หรือใช้สคริปต์ที่เผยแพร่โดย Palo Alto เพื่อแปลง IAR parser output ไปเป็นเหตุการณ์ MISP: [report_to_misp] (https://github.com/PaloAltoNetworks-BD/report_to_misp/).

### Publish an event:

![Only use publish (no email) for minor changes such as the correction of typos.](figures/publish.png)

เมื่อมีการอัปโหลด / ตั้งค่าแอตทริบิวต์และสิ่งที่แนบทั้งหมดที่คุณต้องการรวมไว้ในกิจกรรมแล้วให้สิ้นสุดการสร้างโดยเผยแพร่กิจกรรม (คลิกเหตุการณ์ที่เผยแพร่ในมุมมองเหตุการณ์) การแจ้งเตือนจะแจ้งเตือนผู้ใช้ที่มีสิทธิ์ (ขึ้นอยู่กับการควบคุมส่วนตัวของเหตุการณ์และแอตทริบิวต์ / สิ่งที่แนบและไม่ว่าจะมีการเปิดใช้งานการแจ้งเตือนอัตโนมัติ) หรือไม่ให้ผลักดันเหตุการณ์ดังกล่าวไปยังอินสแตนซ์ที่อินสแตนซ์ของคุณเชื่อมต่อและเผยแพร่ต่อไป กฎการแจกจ่าย นอกจากนี้ยังอ่านแอตทริบิวต์ที่เกี่ยวกับเครือข่ายสำหรับการสร้างลายเซ็น NIDS ด้วย (ผ่านคุณลักษณะการส่งออกลายเซ็น NIDS สำหรับข้อมูลเพิ่มเติมไปที่ส่วนการส่งออก)
มีทางเลือกอื่นในการเผยแพร่กิจกรรมโดยไม่ต้องแจ้งเตือนผู้ใช้คนอื่น ๆ โดยใช้ปุ่ม "เผยแพร่ (ไม่มีอีเมล)" ควรใช้เฉพาะสำหรับการแก้ไขเล็กน้อย (เช่นการแก้ไขการสะกดผิด)

หากอินสแตนซ์ของคุณเปิดใช้งานงานแบ็กกราวด์แล้วเหตุการณ์อาจไม่ได้รับการเผยแพร่ทันที

## Browsing past events:

อินเทอร์เฟซ MISP ช่วยให้ผู้ใช้มีภาพรวมหรือค้นหาเหตุการณ์และแอตทริบิวต์ของเหตุการณ์ที่เก็บอยู่ในระบบได้หลายวิธี
### To list all events:

บนแถบเมนูด้านซ้ายตัวเลือก "List events" จะสร้างรายการของ 60 เหตุการณ์ล่าสุด ในขณะที่แอตทริบิวต์ตัวเองไม่ปรากฏในมุมมองนี้คุณสามารถดูข้อมูลต่อไปนี้ได้:

![This is the list of events in the system. Use the buttons to the right to alter or view any of the events.](figures/list_events2.png)
*   **Published:** กิจกรรมที่เผยแพร่แล้วจะถูกทำเครื่องหมายด้วยเครื่องหมายถูก กิจกรรมที่ไม่ได้เผยแพร่ถูกทำเครื่องหมายด้วยเครื่องหมายกากบาท
*   **Org:** องค์กรที่สร้างกิจกรรม
*   **Owner Org:** องค์กรที่เป็นเจ้าของเหตุการณ์ในกรณีนี้ ฟิลด์นี้จะปรากฏแก่ผู้ดูแลเท่านั้น
*   **ID:** หมายเลขประจำตัวของเหตุการณ์ที่กำหนดโดยระบบเมื่อเหตุการณ์ถูกป้อนครั้งแรก (หรือในกรณีของเหตุการณ์ที่ถูกซิงโครไนซ์เมื่อมันถูกคัดลอกครั้งแรกมากกว่า - เพิ่มเติมเกี่ยวกับการทำข้อมูลให้ตรงกันในบทที่ xy)
*   **Tags:** แท็กที่กำหนดให้กับกิจกรรมนี้
*   **#Attr.:** จำนวนแอตทริบิวต์ที่เหตุการณ์มี
*   **Email:** ที่อยู่อีเมลของผู้สื่อข่าวของกิจกรรม ไม่ปรากฏแก่ผู้ใช้ทั่วไป ผู้ดูแลระบบองค์กรสามารถดูที่อยู่อีเมลของผู้ใช้องค์กรของตนเองได้
*   **Date:** วันที่ของการโจมตี
*   **Threat Level:** ระดับความเสี่ยงของการโจมตีระดับต่อไปนี้เป็นไปได้:
  *    **Low:** มัลแวร์ทั่วไป
  *    **Medium:** ภัยคุกคามแบบถาวรขั้นสูง (APTs)
  *    **High:** APTs ที่ซับซ้อนและการโจมตีแบบ 0day
  *    **Undefined:** ฟิลด์นี้จะไม่สามารถกำหนดและแก้ไขได้ในภายหลัง
*   **Analysis:** แสดงถึงขั้นตอนปัจจุบันของการวิเคราะห์สำหรับเหตุการณ์โดยมีตัวเลือกที่เป็นไปได้ดังต่อไปนี้:
  *   **Initial:** การวิเคราะห์เพิ่งเริ่มต้น	
  *   **Ongoing:** การวิเคราะห์กำลังดำเนินการอยู่
  *   **Completed:** การวิเคราะห์เสร็จสมบูรณ์
*   **Info:** คำอธิบายสั้น ๆ ของกิจกรรมโดยเริ่มจากหมายเลขอ้างอิงภายใน
*   **Distribution:** ฟิลด์นี้ระบุถึงสิทธิพิเศษในการแบ่งปันของกิจกรรม สำหรับรายละเอียดโปรดดูข้อมูลการแจกจ่ายในส่วน [event section](#creating-an-event).
*   **Actions:** การควบคุมที่ผู้ใช้ต้องดูหรือปรับเปลี่ยนเหตุการณ์ การดำเนินการที่เป็นไปได้ที่มีอยู่  (depending on user privileges - [click here](#roles) to find out more about privileges):
  *   **Publish:** Publishing an event will have several effects: The system will e-mail all eligible users that have auto-alert turned on (and having the needed privileges for the event, depending on its private classification) with a description of your newly published event, it will be flagged as published and it will be pushed to all eligible servers (to read more about synchronisation between servers, have a look at the [section on connecting servers](#connecting-to-other-instances)
  *   **Edit:** การคลิกปุ่มแก้ไขจะแสดงหน้าจอเดียวกันกับที่ใช้สำหรับสร้างเหตุการณ์ใหม่ยกเว้นว่าทุกช่องจะกรอกข้อมูลของกิจกรรมที่กำลังแก้ไขอยู่ คุณสามารถแก้ไขการเผยแพร่กิจกรรมได้เฉพาะเมื่อคุณเป็นผู้ใช้งานขององค์กรที่สร้างขึ้นเท่านั้น สำหรับข้อมูลเพิ่มเติมเกี่ยวกับมุมมองนี้โปรดดูที่ส่วน (อ่านเพิ่มเติมเกี่ยวกับการซิงโครไนซ์ระหว่างเซิร์ฟเวอร์ได้ที่ [creating an event](#creating-an-event).
  *   **Delete:** ระบบจะแจ้งให้คุณทราบก่อนลบกิจกรรมที่ไม่พึงประสงค์.
  *   **View:** จะนำมุมมองเหตุการณ์ซึ่งนอกเหนือจากข้อมูลพื้นฐานที่มีอยู่ในรายการงานจะมีดังต่อไปนี้::

### Filters

นอกจากนี้ยังสามารถกรองกิจกรรมที่แสดงโดยการคลิกที่ไอคอนรูปแว่นขยายขนาดเล็กที่อยู่ถัดจากชื่อฟิลด์และป้อนคำที่กรอง

### Event view

![This view includes the basic information about an event, a link to related events, all attributes and attachments with tools to modify or delete them and extra functions for publishing the event or getting in touch with the event's reporter.](figures/event_detail.png)

##General Event Information##

*   **ID:** The ID of the event.
*   **Uuid:** In order to avoid collisions between events and attributes (during for example a sync) a Uuid is assigned that uniquely identifies each of them.
*   **Org** The organisation that has originally created the event. The logo (if it exists on the server, alternatively a string) representing the organisation is also shown int he right upper corner.
*   **Contributors:** Shows a list of the organisations that have contributed to the event via proposals. If you click any of the logos listed here, you'll get redirected to a filtered event history view, including only the changes made by the organisation.
*   **Tags:** A list of tags associated with the event. Clicking a tag will show a list of events with the same tag attached. The little cross next to each tag allows you to remove the tag from the event, whilst the '+' button allows you to assign a tag. For the latter two options to be visible, you have to have tagging permission.
*   **Date:** The date of detection, set by the user that creates the event, not to be confused with the creation date of the event.
*   **Threat Level:** The assigned threat level of the event.
*   **Analysis:** The status of the analysis.
*   **Distribution:** This shows the distribution rules applied to this event, controlling whether only the creating organisation can see (Your organisation only) it or everyone on the instance (This community only). The two remaining settings allow the event to be propagated to organisations on remote connected instances.
*   **Info:** A short description of the event itself. Make sure not to put information in here that could be used for correlation purposes and be better suited as an Attribute.
*   **Published:** Whether the event has been published or not. Publishing allows the attributes of the event to be used for all eligible exports and it notifies users that have subscribed to the event alerts. Also, a publish initiates a push to all eligible instances.

**List of Related Events**
The list of relations is shown on the right hand side of the general event information. Events can be related by having one or more attributes that are exact matches. For example, if two events both contain a source IP attribute of 11.11.11.11 then they are related. The list of events that are related the currently shown one, are listed under "Related Events", as links (titled the related event's date and ID number) to the events themselves.

**Data Element Toggles**
You can control some of the data that is shown on this page using three toggles. The elements that can be disabled are the pivot threads, the attributes (and proposals) and the Discussions. You can collapse these elements and then expand them again using the same button.

**Pivot Threads**
While moving from event to event through the relation links (a process that we refer to as pivoting), you create a path that shows which events you have traversed. This path is reset by leaving the event view and navigating elsewhere in the application or by deleting the root pivot element.
Each event visited is represented by a bubble in the pivot thread graph, connected by lines that show how the user has arrived at the next connected event. It is possible to jump back to an earlier relation and pivot to another event through that, creating branches in the graph.
The currently selected event is coloured blue in the graph. If you would like to delete an element from the graph (including all of elements that branch off of it) just click on the small x within a pivot bubble. For a deletion to be possible the following conditions have to be met:
*   The pivot element to be deleted cannot be on the path that leads to the currently selected event
*   The pivot element residing in the graph's root can always be deleted - this will simply reset the current pivot thread

**Attributes and Proposals**
A list of all attributes and proposals attached to the event. The fields for each of them only differ in the available actions and the fact that for proposals to attributes all fields are blank that would stay unchanged if the proposal was accepted (for example, proposing a change to an attribute to turn the IDS flag on will have all fields apart from the IDS flag blank in the proposal. Here is a list of what each of the fields represents:
*   **Date**: The date of the last modification to the attribute. Proposals don't have a date of last edit.
*   **Category**: The category of the attribute or proposal. For a list of possible categories visit the section on [categories and types](categories-and-types).
*   **Type**: The type of the attribute or proposal. For a list of possible categories visit the section on [categories and types](categories-and-types).
*   **Value**: The value or value-pair of the attribute. This is the main payload of the attribute, which is described by the category and type columns. For certain types of attributes that are made up of value-pairs the two parts will be split by a pipe (|), such as for filename|md5. The value field(s) are used by the correlation engine to find relations between events. In value-pair attributes both values are correlated individually.
*   **Comment**: Attributes can have a contextual comment to further describe the attribute. These comments are not used for correlation and are purely informative.
*   **Related Events**: A list of the event IDs that also contain an attribute with the same value.
*   **IDS**: Flags an attribute as an indicator of compromise, allowing it to be included in all of the eligible exports.
*   **Distribution**: Defines the distribution of the attribute individually. An attribute can have a different distribution level than the event. In any case, the lowest distribution level of the two is used.
*   **Actions**: The user can interact with the events through these buttons, which will be further described in the next portion of the guide as they differ for attributes and proposals.

Depending on the colour coding of the row, you can have an attribute, a proposal to the event or a proposal to an attribute:
*   **Attributes**: Each uncoloured line represents an Attribute.
*   **Proposals to an Event**: Each gray line at the end of the list represents a Proposal to an event. These are proposals for a new attribute, mostly unrelated to any of the currently existing attributes. If the creator of the event accepts one of these a new attribute will be created.
*   **Proposals to an Attribute**: Each attribute can have several edit proposals. These will be placed right below the attribute that the proposal affects and - as with the event proposals - is coloured grey. The original attribute's row is coloured blue if a proposal exists for it.

Using the modify button will bring up the attribute creation view, with all data filled out with the attribute's currently stored data.

**Event Discussion Thread**

Each event has its own assigned discussion where users (that are eligible to see the event) can participate in an open discussion. The users are anonymised in the messages, all that other users will see is their user ID number and their organisation. To post a message on the Event Discussion, either use the reply button on a previous post or use the quickresponse field at the bottom of the page.
Each post is made up of the following:
*   **Date:**The date when the post was created.
*   **Post navigation:**This should the post's ID as well as a link to jump to the top of the discussion thread on the page itself.
*   **Organisation logo:**If such an image exists for the organisation that has posted the message, then the logo is shown.
*   **Message:**The body of the post itself. This can also include automatically generated links to other events and threads as well as show quoted test in embedded bubbles. Editing an event will also append a post with a message indicating that it was edited together with the timestamp of the edit.
*   **User:**The e-mail address of the poster if he/she is from the organisation as the current user. Alternatively a generated sting is shown that includes the user ID of the user, so that his/her e-mail address could remain hidden whilst still being identifiable.
*   **Action buttons:**Edit, Delete and Reply. The first two of the three options are only available to the poster of the message or a site admin. Quoting a post will automatically include the original message in [quote] tags.

Here is a list of the various tools you can use while using this feature:
*   **Pagination:** There are 5 posts visible on each event page, if there have been more messages posted, use the previous and next button to navigate through the thread. This will not reload the rest of the page.
*   **Discussion Tags:** Users can quote something by encapsulating it in [quote][/quote] tags, they can create a link to another event with the [event][/event] tags or to another discussion thread with [thread][/thread].
*   **Quick Post:** Adding a post will take the user to a separate add Post page, something that can be a bit of an inconvenience. To avoid this, there is a quick post button, where users can add messages on the fly without having to reload the page. On top of the quick post field, 3 buttons allow users to generate quote, event and thread tags quickly.


### Event History:

View the logs of the event that show how the event has changed over time, including the contribution from other organisations in the form of proposals. There are two ways to get to this view, either by clicking on View Event History on the side menu of an event view, or by clicking on a contribing organisation's logo on the event view. The latter will show a restricted form of the logs, showing only Proposals created by the selected organisation. The fields shown in this view are as described as follows:
*   **Org**: The logo (or in the lack thereof a string representation) of the organisation.
*   **Action**: Each entry in the log happens during an action, such as the creation, modification or deletion of data and some special actions (such as accepting a proposal). This field shows which action caused the entry to be created.
*   **Model**: As described above, a log entry is generated on certain actions. This field shows which type of data was affected that caused the log entry to be created (such as a change to the event, the creation of an attribute, the discarding of a proposal, etc).
*   **Title**: This is a short description of the change itself and it is not nearly as detailed as the information administrators get in the audit logs. However, for attributes and proposals the category / type and value of the created or edited attribute is shown.
*   **Created**: The date and time of the log entry's creation.

### Listing all attributes:
	Apart from having a list of all the events, it is also possible to get a list of all the stored attributes in the system by clicking on the list attributes button. The produced list of attributes will include the followings fields:

![Use the buttons to the right to view the event that this attribute belongs to or to modify/delete the attribute.](figures/list_attributes2.png)
*   **Event:** This is the ID number of the event that the attribute is tied to. If an event belongs to your organisation, then this field will be coloured red.
*   **Org:** The organisation that has created the event.
*   **Category:** The category of the attribute, showing what the attribute describes (for example the malware's payload). For more information on categories, go to section xy
*   **Type:** The type of the value contained in the attribute (for example a source IP address). For more information on types, go to section xy
*   **Value:** The actual value of the attribute, describing an aspect, defined by the category and type fields of the malware (for example 11.11.11.11).
*   **Comment:** An optional contextual comment attached to the attribute.
*   **IDS:** Shows whether the attribute has been flagged for NIDS signature generation or not.
*   **Actions:** A set of buttons that allow you to view the event that the attribute is tied to, to edit the attribute (using the same view as what is used to set up attributes, but filled out with the attribute's current data) and a delete button.

### Searching for attributes:

Apart from being able to list all events, it is also possible to search for data contained in the value field of an attribute, by clicking on the "Search Attributes" button.

![You can search for attributes by searching for a phrase contained in its value. Narrow your search down by selecting a type and/or a category which the event has to belong to.](figures/search_attribute.png)

This will bring up a form that lets you enter one or several search strings (separate search strings with line breaks) that will be compared to the values of all attributes, along with options to narrow down the search based on category and type. The entered search string has to be an exact match with (the sub-string of) a value. A second text field makes it possible to enter event IDs for events that should be excluded from the search (again, each line represents an event ID to be excluded). The third text field allows the user to restrict the results to attributes from certain organisations or to attributes not created by certain other organisations, using the above described syntax.
The list generated by the search will look exactly the same as listing all attributes, except that only the attributes that matched the search criteria will be listed (to find out more about the list attributes view, [click here](categories-and-types)). The search parameters will be shown above the produced list and the search terms will be highlighted.
The last option is a checkbox that restricts all of the results to attributes that are marked as IDS signatures.

!["You can view the event that an attribute belongs to with the view button, or you can edit/delete the attribute via the buttons on the right."](figures/search_attribute_result.png)


## Updating and modifying events and attributes:

Every event and attribute can easily be edited. First of all it is important to find the event or attribute that is to be edited, using any of the methods mentioned in the section on [browsing past events](#browsing_events).
Once it is found, the edit button (whether it be under actions when events/attributes get listed or simply on the event view) will bring up the same screen as what is used to create the entry of the same type (for an event it would be the event screen as [seen here](#Creating an event), for an attribute the attribute screen as [described here](#add-attributes-to-the-event)).
Keep in mind that editing any event (either directly or indirectly through an attribute) will unpublish it, meaning that you'll have to publish it (through the event view) again once you are done.

## Tagging:

As described earlier, users with tagging rights can arbitrarily tag events using tags chosen from a pool of available options. If you have tagging privileges and would like to create a new tag, navigate to Event Actions - Add Tag. You'll be presented with the following form:

![Enter a name for the tag and click on the color field to be able to pick a colour for it.](figures/tag.png)

Fill out the following fields:
*   **Name**: Pick a name for the tag. Try to use consistent naming conventions across your instance, to avoid confusion.
*   **Colour**: You can choose a colour for the tag by clicking on the colour field and using the colour picker tool. Try to avoid having duplicate or similar looking colours to help avoid confusion.

## Templating:

Newer users can easily be overwhelmed by having to manually populate events with attributes without any guidance. What sort of information should go into the event? What should be the category and type of a C2 IP? Templates allow users to use simple forms to populate events.
Even though MISP ships with a few default templates, it is possible for users (with the appropriate templating privilege) to create new templates for their users or for all users of the instance. Let's look at how you can create a template.
First go to Event Actions - Add Template to go to the event creation view.

![Fill in the generic information about the template.](figures/create_template.png)

The following fields have to be filled out:
*   **Name**: The name of the template should describe what type of an event it should be used to generate attributes.
*   **Tags**: You can attach tags to the template - an event populated using the template would automatically receive the tag(s). Add new tags using the + button. If you chnage your mind about a tag you can remove it with the cross next to the tag name.
*   **Event Description**: A short description about the events that this template should be used for.
*   **Share this template with others**: The template can be set to be usable by any organisation on the instance or only by the one that has created it.

Once the skeleton template is created, you can start populating the template with data. There are 3 types of elements that can be used during the creation of a template: attribute, file and text elements. Text elements divide the template into sections with an information field, followed by all of the attribute/file fields until a new text field is read. Don't worry about the order of the elements during creation, they can be re-arranged using drag & drop. Let's look at the 3 element types:

**Attribute Element**

![This element will generate regular attributes based on user entry.](figures/template_attribute.png)

The following fields have to be filled out:
*   **Name**: The field name that will be presented to the user.
*   **Description**: A brief description of the element. Make sure that you provide sufficient information to the user to make it obvious what is expected.
*   **Category**: The category used for any attributes created using this template element.
*   **Type**: The type or complex type used for any attributes created using this template element. Complex types allow for several related types to be used on data entry. For example, a "file" complex type element allows for filenames and hashes.
*   **Use Complex types**: If the category permits it, switch to a complex type using this checkbox.
*   **Automatically mark for IDS**: If checked, any attributes generated using this element will be marked for IDS exporting.
*   **Mandatory element**: If the elemnt is marked as mandatory, then the template form can only be submitted by users if this field is filled out.
*   **Batch import element**: Allow for multiple values to be entered (separated by line breaks).

**File Element**

![This element will generate attachments based on user entry.](figures/template_file.png)

The following fields have to be filled out:
*   **Name**: The field name that will be presented to the user.
*   **Description**: A brief description of the element. Make sure that you provide sufficient information to the user to make it obvious what is expected.
*   **Category**: The category to be used by all attachments uploaded through this element.
*   **Malware**: If the uploaded files are malicious and should be encrypted and password protected, mark this checkbox.
*   **Mandatory element**: If it should be required to upload an attachment, check this checkbox.
*   **Batch import element**: Ticking this checkbox allows users to upload several files using this element.

**Text Element**

![This element will start a section in the template, which continues until the next text element or the end of the template.](figures/template_text.png)

The following fields have to be filled out:
*   **Name**: The name of the section that will be presented to the user.
*   **Text**: The description of the section. Explain briefly to the user what the following attribute/file elements will be dealing with. There are several ways to split a template into sections, try to have ease of use in mind while creating it.

## Contacting the reporter:

To get in touch with the reporter of a previously registered event, just find the event for which you would like to contact the reporter by either finding it on the list of events, by finding it through one of its attributes or by finding it through a related event.
Once the event is found and the event view opened, click the button titled "Contact Reporter". This will bring up a view where you can enter your message that is to be e-mailed to all members of the reporting organisation that subscribe to receiving such reports or the reporting user himself. Along with your message, the detailed information about the event in question will be included in the e-mail.

![Enter your message to the reporter and choose whether his/her entire organisation should get the message or not by ticking the check-box.](figures/contact_reporter.png)

By default, the message will be sent to every member of the organisation that posted the event in the first place, but if you tick the check-box below the message field before sending the mail, only the person that reported the event will get e-mailed.

## Automation:
It is possible to quickly and conveniently export the data contained within the system using the automation features located in the main menu on the left (available to users with authentication key access only). There are various sets of data that can be exported, by using the authentication key provided by the system (also shown on the export page). If for whatever reason you would need to invalidate your current key and get a new one instead (for example due to the old one becoming compromised) just hit the reset link next to the authentication key in the export view or in your "my profile" view.
To find out about the various export formats and the usage within the automation functions, please read the page on the [API's usage](#api).

## Exporting data:

For users that do not have authentication key access, an alternate export feature is available that relies on your interactive login to the site. To access these, just use the export menu button to the left and you'll be presented with a list of export options.
Depending on your server's configuration, you will be presented with one of two possible pages, depending on whether you have background processing enabled or not.

#### Export page with background jobs disabled

The page will list a set of export formats that you can immediately download as a file. Just click on the desired export format and MISP will start collecting all the data that you will receive in a file. Keep in mind that this can be a lengthy process. To avoid having to wait, consult with your instance's site administrator about enabling the background processing.

![Use the export features here to quickly download data in various formats](figures/export.png)

#### Export page with background jobs enabled

If the background jobs are enabled, you'll be redirected to a different version of the export page. Here you will see a table with all of the major export formats and the current status of the cached export files. Keep in mind that these are generated on an organisation by organisation basis, so even though others have generated newer export caches your organisation may have an outdated cache. You can simply issue a generate command (by clicking the "Generate" button) on the desired export type and the background workers will start fetching and assembling your cache. A progress bar will show the progress of the export process.
Once done, you can click "Download" to download the freshly generated cache file. If the cache is already up to date from before, then you don't have to regenerate the cache, just click on the "download" button.
You may have noticed that the TEXT export only has a generate button - this is because TEXT exports are made up of a lot of types of exports, all of which get generated together. To download any of these files, just click on any of the attribute types at the bottom of the table.
A quick description of each of the fields in the table:
*   **Type**: The type of the export (such as XML, Suricata, MD5, etc.).
*   **Last Update**: The generation date of the current cache for the given export type.
*   **Description**: A description of the export format.
*   **Outdated**: This compares the cache generation date to the last timestamp when an event was updated and lets you know whether the cache is outdated or not.
*   **Progress**: Shows the progress of the last initiated generation process.
*   **Actions**: Download or Generate the given cache with these buttons.

![Use the export features here to quickly download data in various formats](figures/export_bg.png)

#### Exporting search results and individual events
Apart from the options offered by the export pages, it's also possible to export all events involved in a search attribute result table, by using the "Download results as XML" button on the left menu bar.

![Download a .xml from all the events that are shown through an attribute in the search results.](figures/export_search.png)

Each event's view has its own export feature, both as an XML export and as a .ioc file. To reach these features, just navigate to an event and use the appropriate buttons on the right side.

![Download a .xml or a .ioc of the event.](figures/export_search.png)

## Connecting to other instances:

Apart from being a self contained repository of attacks/malware, one of the main features of MISP is its ability to connect to other instances and share (parts of) its information. The following options allow you to set up and maintain such connections.

### Setting up a connection to another server:

In order to share data with a remote server via pushes and pulls, you need to request a valid authentication key from the hosting organisation of the remote instance. When clicking on List Servers and then on New Server, a form comes up that needs to be filled out in order for your instance to connect to it. The following fields need to be filled out:

![Make sure that you enter the authentication key that you have been given by the hosting organisation of the remote instance, instead of the one you have gotten from this one.](figures/add_server.png)

*   **Base URL:** The URL of the remote server.
*   **Organization:** The organisation that runs the remote server. It is very impoportant that this setting is filled out exactly as the organisation name set up in the bootstrap file of the remote instance.
*   **Authkey:** The authentication key that you have received from the hosting organisation of the remote instance.
*   **Push:** This check-box controls whether your server is allowed to push to the remote instance.
*   **Pull:** This check-box controls whether your server can request to pull all data from the remote instance.
*   **Self Signed:** Ticking this checkbox will allow syncing with instances using self-signed certificates.
*   **Certificate File:** If the instance that you want to connect to has their entire own certificate chain, you can use this to import a .pem file with it and override CakePHP's standard root CA file.

**If you are an administrator**, trying to allow another instance to connect to your own, it is vital that two rules are followed when setting up a synchronisation account:
*   The synchronisation user has to have the sync permission and full read/write/publish privileges turned on
*   Both the sync user and the organisation setting in your instance's Config/bootstrap.php file have to match the organisation identifier of the hosting organisation.

### Browsing the currently set up server connections and interacting with them:

If you ever need to change the data about the linked servers or remove any connections, you have the following options to view and manipulate the server connections, when clicking on List Servers: (you will be able to see a list of all servers that your server connects to, including the base address, the organisation running the server the last pushed and pulled event IDs and the control buttons.).

![Apart from editing / deleting the link to the remote server, you can issue a push all or pull all command from here.](figures/list_servers.png)

*   **Editing the connection to the:** By clicking edit a view, [that is identical to the new instance view](#setting-up-a-connection-to-another-server), is loaded, with all the current information of the instance pre-entered.
*   **Deleting the connection to the instance:** Clicking the delete button will delete the link to the instance.
*   **Push all:** By clicking this button, all events that are eligible to be pushed on the instance you are on will start to be pushed to the remote instance. Events and attributes that exist on the far end will be updated.
*   **Pull all:** By clicking this button, all events that are set to be pull-able or full access on the remote server will be copied to this instance. Existing events will not be updated.

## Rest API:

The platform is also [RESTfull](http://en.wikipedia.org/wiki/Representational_state_transfer), so this means that you can use structured format (XML or JSON) to access Events data.

### Requests

Use any HTTP compliant library to perform requests.
You can choose which format you would like to use as input/output for the REST calls by specifying the Accept and Content-Type headers.

The following headers are required if you wish to recieve / push XML data:
**Authorization**: _your authorisation key_
**Accept**: _application/xml_
**Content-Type**: _application/xml_

The following headers are required if you wish to recieve / push JSON data:
**Authorization**: _your authorisation key_
**Accept**: _application/json_
**Content-Type**: _application/json_
The following table shows the relation of the request type and the resulting action:

| HTTP format       | URL            | Controller action invoked     |
| ----------------- | -------------- | ----------------------------- |
| GET               | /events        | EventsController::index()     |
| GET               | /events/123    | EventsController::view(123)   |
| POST              | /events        | EventsController::add()       |
| PUT               | /events/123    | EventsController::edit(123)   |
| DELETE            | /events/123    | EventsController::delete(123) |
| POST              | /events/123    | EventsController::edit(123)   |

*Attachments are included using base64 encoding below the `data` tag.
<br/>

### Example - Get single Event

In this example we fetch the details of a single Event (and thus also his Attributes).
The request should be:

`GET https://your_misp_url/events/123`

And with the HTTP Headers:
`Accept: application/xml`
`Authorization: your_api_key`

The response you're going to get is the following data:

```xml
<pre><?xml version="1.0" encoding="UTF-8" standalone="no"?>;
<response>
	<Event>
		<id>57</id>
		<org>NCIRC</org>
		<date>2014-03-04</date>
		<threat_level_id>1</threat_level_id>
		<info>Code monkey doing code monkey stuff</info>
		<published>1</published>
		<uuid>50aa54aa-f7a0-4d74-910d-10f0ff32448e</uuid>
		<attribute_count>1</attribute_count>
		<analysis>1</analysis>
		<timestamp>1393327600</timestamp>
		<distribution>1</distribution>
		<proposal_email_lock>0</proposal_email_lock>
		<orgc>Iglocska</orgc>
		<locked>0</locked>
		<publish_timestamp>1393327600</publish_timestamp>
		<Attribute>
			<id>9577</id>
			<type>other</type>
			<category>Artifacts dropped</category>
			<to_ids>1</to_ids>
			<uuid>50aa54bd-adec-4544-b494-10f0ff32448e</uuid>
			<event_id>57</event_id>
			<distribution>1</distribution>
			<timestamp>1393327600</timestamp>
			<comment>This is an Attribute</comment>
			<value>Some_attribute</value>
			<ShadowAttribute />
		</Attribute>
		<ShadowAttribute />
		<RelatedEvent />
	</Event>
	<xml_version>2.2.0</xml_version>
</response>
```


#### Example - Add new Event

In this example we want to add a single Event.
The request should be:

```
POST https://your_misp_url/events
Accept: application/xml
Authorization: your_api_key
```

And the request body:

```xml
<Event>
	<date>2014-03-04</date>
	<threat_level_id>1</threat_level_id>
	<info>Something concise</info>
	<published>1</published>
	<analysis>1</analysis>
	<distribution>1</distribution>
	<Attribute>
		<type>other</type>
		<category>Artifacts dropped</category>
		<to_ids>1</to_ids>
		<distribution>1</distribution>
		<comment>This is an Attribute</comment>
		<value>Some_attribute</value>
	</Attribute>
</Event>
```

The response you're going to get is the following data:

```
HTTP/1.1 100 Continue
HTTP/1.1 200 Continue
Date: Tue, 04-Mar-2014 15:00:00
Server: Apache/2.2.22 (Ubuntu) PHP/5.4.9-4ubuntu2.3
X-Powered-By: PHP/5.4.9-4ubuntu2.3
Set-Cookie: CAKEPHP=deleted; expires=Wed, 05-Mar-2014 15:00:00 GMT; path=/
Set-Cookie: CAKEPHP=a4ok3lr5p9n5drqj27025i4le3; expires Tue, 04-Mar-2014 15:00:00 GMT; path=/; HttpOnly
Content-Length: 1 kB
Content-Type: application/xml
```

```xml
<?xml version = "1.0" encoding = "UTF-8"?>
<response>
	<Event>
		<id>76</id>
		<org>NCIRC</org>
		<date>2014-03-04</date>
		<threat_level_id>1</threat_level_id>
		<info>Something concise</info>
		<published>1</published>
		<uuid>50aa54aa-f7a0-4d74-920d-10f0ff32448e</uuid>
		<attribute_count>1</attribute_count>
		<analysis>1</analysis>
		<timestamp>1393328991</timestamp>
		<distribution>1</distribution>
		<proposal_email_lock>0</proposal_email_lock>
		<orgc>Iglocska</orgc>
		<locked>0</locked>
		<publish_timestamp>1393947960</publish_timestamp>
		<Attribute>
			<id>10462</id>
			<type>other</type>
			<category>Artifacts dropped</category>
			<to_ids>1</to_ids>
			<uuid>50aa54bd-adec-4544-b412-10f0ff32448e</uuid>
			<event_id>76</event_id>
			<distribution>1</distribution>
			<timestamp>1393328991</timestamp>
			<comment/>
			<value>Some_attribute</value>
			<ShadowAttribute/>
		</Attribute>
		<ShadowAttribute/>
		<RelatedEvent>
			<id>75</id>
			<org>NCIRC</org>
			<date>2012-11-19</date>
			<info>Code monkey doing code monkey stuff</info>
			<uuid>50aa54aa-f7a0-4d74-910d-10f0ff32448e</uuid>
			<published>1</published>
			<analysis>1</analysis>
			<attribute_count>1</attribute_count>
			<orgc>Iglocska</orgc>
			<timestamp>1393327600</timestamp>
			<distribution>1</distribution>
			<proposal_email_lock>0</proposal_email_lock>
			<locked>0</locked>
			<threat_level_id>1</threat_level_id>
			<publish_timestamp>1393947655</publish_timestamp>
		</RelatedEvent>
	</Event>
	<xml_version>2.2.0</xml_version>
</response>
```

The respone from requesting an invalid page

```xml
<?xml version = "1.0" encoding = "UTF-8"?>
<response>
	<name>Not Found</name>
	<url>/The_meaning_of_life</url>
</response>
```
