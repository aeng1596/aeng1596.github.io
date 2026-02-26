# 3.1.2 Configure a Firewall
+ ในฐานะผู้ดูแลระบบรักษาความปลอดภัยด้านไอทีขององค์กรขนาดเล็ก คุณต้องกำหนดค่า Windows Firewall บนเครื่องคอมพิวเตอร์เพื่อควบคุมการรับส่งข้อมูลเครือข่าย โดยการสร้างกฎ Inbound และ Outbound เพื่ออนุญาตหรือบล็อกการเชื่อมต่อที่ระบุ
+ วัตถุประสงค์ของการปฏิบัติในห้องปฏิบัติการนี้ มีดังนี้:
    + กำหนดค่า Windows Firewall with Advanced Security โดยใช้ข้อมูลดังต่อไปนี้

# วิธีเข้าถึง: Control Panel > System and Security > Windows Defender Firewall > Advanced Settings

| Parameter | Value |
| :--- | :--- |
| **Rule Type** | Port |
| **Protocol** | TCP |
| **Port** | 8080 |
| **Action** | Block the connection |
| **Profile** | Domain, Private, Public |
| **Name** | Block Port 8080 |

+ สร้าง Inbound Rule เพื่อบล็อก Port 8080
+ ยืนยันว่ากฎถูกสร้างและเปิดใช้งานเรียบร้อยแล้ว

# Start Lab

  + 1.เริ่มต้นที่หน้า Desktop ของ Windows คลิก Start Menu แล้วพิมพ์ Windows Defender Firewall

  ![Desktop](Lab-3.1.2/01-Desktop.jpg)

  + 2.เปิด Windows Defender Firewall with Advanced Security

  ![Windows Defender Firewall](Lab-3.1.2/02-Windows-Defender-Firewall.jpg)

  + 3.คลิก Inbound Rules ที่แผงด้านซ้าย จากนั้นคลิก New Rule... ที่แผงด้านขวา

  ![Inbound Rules](Lab-3.1.2/03-Inbound-Rules.jpg)

  + 4.เลือก Rule Type เป็น Port แล้วคลิก Next

  ![Rule Type](Lab-3.1.2/04-Rule-Type.jpg)

  + 5.เลือก TCP และกรอก Specific local ports เป็น 8080 แล้วคลิก Next

  ![Protocol and Ports](Lab-3.1.2/05-Protocol-Ports.jpg)

  + 6.เลือก Action เป็น Block the connection แล้วคลิก Next

  ![Action](Lab-3.1.2/06-Action.jpg)

  + 7.เลือก Profile ทั้งหมด (Domain, Private, Public) แล้วคลิก Next

  ![Profile](Lab-3.1.2/07-Profile.jpg)

  + 8.กรอกชื่อกฎ Block Port 8080 แล้วคลิก Finish เพื่อบันทึก

  ![Name](Lab-3.1.2/08-Name.jpg)

  + 9.ตรวจสอบว่ากฎ Block Port 8080 ปรากฏใน Inbound Rules และมีสถานะ Enabled

  ![Verify Rule](Lab-3.1.2/09-Verify-Rule.jpg)

  + 10.กด Score Lab เพื่อตรวจสอบผลและสิ้นสุด Lab 3.1.2 Configure a Firewall

  ![Report](Lab-3.1.2/10-Report.jpg)
