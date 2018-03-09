# Web-server-Beaglebone-Green
how 2 cre8 Web server beaglebone Green(Debian 8) .....PHP7.0, Nginx, yii framework, composer
1. ขั้นแรก สิ่งที่ต้องเตรียม
1.1 Beaglebone Green
1.2 OS: Debian 8
1.3 Putty หรือ อื่น ๆ 

2. ขั้นตอนการติดตั้ง Debian และ update Packages  
2.1 ดาวน์โหลดไฟล์ OS จาก https://rcn-ee.com/rootfs/bb.org/testing/2018-03-06/lxqt-4gb/BBB-blank-debian-8.10-lxqt-4gb-armhf-2018-03-06-4gb.img.xz
2.2 Mount ไฟล์ที่โหลดมาลงใน SDCard แนะนำ 8GB ขึ้นไป
2.3 นำ SDcard ไปเสียบใต้ Board Beagleboneจากนั้นกดปุ่ม Flash (สังเกตุปุ่มจะอยู่โดดเดี่ยวตรงข้ามกับปุ่ม Power กับ Restart)
2.4 เมื่อทำการ Flash เสร็จแล้ว ให้เสียบสายlan และทำการ Remote Shell เข้าไปที่ Beaglebone โดยการใส่ IP ของ beaglebone (แนะนำให้เช็คIPจากที่ใดก็ได้ก่อนRemote)
2.5 ทำการใส่ user:password (debian:temppwd)
2.6 ทำการสั่งปิด service ของ beaglebone ก่อนโดยพิมพ์ดังนี้:
      systemctl disable bonescript.socket
      systemctl disable bonescript.service
      systemctl stop bonescript.socket
      systemctl stop bonescript.service
2.6 เขียนคำสั่ง sudo apt-get update && sudo apt-get -y upgrade 
2.7 รอจนกระทั่งเสร็จสิ้นกระบวนการ เป็นอันจบ

3. ติดตั้ง Nginx
3.1 พิมพ์ command: sudo apt-get install nginx
3.2 เมื่อเสร็จแล้วให้ลองทำการ test หน้าเว็บดู ให้พิมพ์ IP ของคุณในช่อง url 
3.3 ถ้าขึ้นหน้า Welcome Nginx ก็เป็นอันใช้ได้

