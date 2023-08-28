# Voice of Customer
<img src="https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/8ad8648f-c729-464d-b621-6e3da832230b" height="400" width="600" >

## DATASET
[toshinoshop(Shopee Mall)](https://shopee.co.th/Toshino%E0%B8%A3%E0%B8%B2%E0%B8%87%E0%B8%9B%E0%B8%A5%E0%B8%B1%E0%B9%8A%E0%B8%81%E0%B9%84%E0%B8%9F2-6%E0%B8%8A%E0%B9%88%E0%B8%AD%E0%B8%872-6%E0%B8%AA%E0%B8%A7%E0%B8%B4%E0%B8%95%E0%B8%8B%E0%B9%8C-2USB%E0%B8%AA%E0%B8%B2%E0%B8%A2%E0%B8%A2%E0%B8%B2%E0%B8%A73-5%E0%B8%A1.%E0%B8%A3%E0%B8%B8%E0%B9%88%E0%B8%99ET-913USB-ET-914USB-ET-915USB-ET-912-ET-913-i.251098584.19620106839?sp_atk=5aed7023-3ebe-4813-9de0-ee425a9a1434&xptdk=5aed7023-3ebe-4813-9de0-ee425a9a1434)

## Topic Modeling
number of topics = 3

### Result

![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/f5673051-402b-4f7e-90b1-7ed47d0693d7)
![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/8f663e53-191b-475c-91cd-ec6fe83cc781)
![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/3a3e0cb9-125b-42bb-9572-bddfc7e8dcbf)

## Document Clustering

### K-mean

```
Cluster ID : 0
Most common words include : [('สินค้า', 4), ('ดี', 3), ('สั่ง', 3), ('ปลั๊ก', 2), ('ไฟ', 2), ('/', 2), ('ปลั้ก', 1), ('พ่วง', 1), ('พอทชาร์จusb', 1), ('ให้ด', 1)]

Cluster ID : 1
Most common words include : [('สินค้า', 12), ('ดี', 7), ('ราคา', 3), ('คุณภาพ', 3), ('ค้า', 2), ('คุ้มค่า', 2), ('คุ้ม', 1), ('ค่า', 1), ('รับประกัน', 1), ('มั่นใจ', 1)]

Cluster ID : 2
Most common words include : [('ดี', 4), ('ไฟ', 3), ('ปลั๊ก', 2), ('ช่อง', 2), ('ยี่ห้อ', 1), ('กกกกกอด', 1), ('ทน', 1), ('นนนนรางปลั๊ก', 1), ('Toshino', 1), ('งาน', 1)]
```

### Cosine Similarity

```
Cluster ID : 0
Most common words include :[('ดี', 32), ('สินค้า', 32), ('ช่อง', 10), ('ปลั๊ก', 10), ('ไฟ', 9), ('งาน', 6), ('คุณภาพ', 6), ('ยี่ห้อ', 5), ('ค้า', 5), ('สาย', 4)]

Cluster ID : 1
Most common words include :[('ดี', 7), ('เสียหาย', 2), ('รีวิว', 2), ('แพคมา', 2), ('แพคส่ง', 1), ('ไวดี', 1), ('ห่อ', 1), ('ภาพ', 1), ('แนบ', 1), ('ใบ', 1)]

Cluster ID : 2
Most common words include :[('บับเบิ้ล', 2), ('กล่อง', 2), ('ไฟ', 2), ('เสียบ', 2), ('/', 2), ('ลอง', 2), ('แพคมา', 1), ('ดี', 1), ('หนา', 1), ('สภาพ', 1)]
```

