# Voice of Customer

Voice of the Customer (VoC) is the practice of gathering and analyzing customer feedback to gain insights into their preferences, needs, and expectations. The primary benefit of VoC is its capacity to enhance customer satisfaction by identifying and addressing areas for improvement in products, services, and customer experiences. By listening to customers, businesses can make informed decisions, enhance their offerings, and foster loyalty, ultimately leading to competitive advantage, reduced churn, and continuous improvement across the organization.

<img src="https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/8ad8648f-c729-464d-b621-6e3da832230b" height="400" width="600" >

**DATASET :** 
[toshinoshop(Shopee Mall)](https://shopee.co.th/Toshino%E0%B8%A3%E0%B8%B2%E0%B8%87%E0%B8%9B%E0%B8%A5%E0%B8%B1%E0%B9%8A%E0%B8%81%E0%B9%84%E0%B8%9F2-6%E0%B8%8A%E0%B9%88%E0%B8%AD%E0%B8%872-6%E0%B8%AA%E0%B8%A7%E0%B8%B4%E0%B8%95%E0%B8%8B%E0%B9%8C-2USB%E0%B8%AA%E0%B8%B2%E0%B8%A2%E0%B8%A2%E0%B8%B2%E0%B8%A73-5%E0%B8%A1.%E0%B8%A3%E0%B8%B8%E0%B9%88%E0%B8%99ET-913USB-ET-914USB-ET-915USB-ET-912-ET-913-i.251098584.19620106839?sp_atk=5aed7023-3ebe-4813-9de0-ee425a9a1434&xptdk=5aed7023-3ebe-4813-9de0-ee425a9a1434)

**METHOD :**

- Topic Modeling with LDA

- Document clustering using K-mean and Cosine Similarity

## Topic Modeling
number of topics = 2

### Result

#### Topic 1 : Product Selection and Satisfaction
This topic seems to focus on discussions related to selecting products, satisfaction with purchases, pricing, and the features of electrical items.
```
[('สินค้า', 0.031782236),
 ('ปลั๊ก', 0.018651133),
 ('ไฟ', 0.016264388),
 ('ช่อง', 0.016251704),
 ('เลือก', 0.01594252),
 ('ชอบ', 0.015938876),
 ('คุ้ม', 0.015865235),
 ('ราคา', 0.015849996),
 ('ซื้อ', 0.015737643),
 ('5', 0.015629182)]
```

#### Topic 2 : Product Quality and Business
This topic appears to revolve around discussions about product quality, pricing, ordering processes, and business aspects such as trade and commerce.
```
[('ดี', 0.09083381),
 ('สินค้า', 0.06773613),
 ('ช่อง', 0.022803437),
 ('ไฟ', 0.022799475),
 ('งาน', 0.020907851),
 ('ราคา', 0.014963789),
 ('คุณภาพ', 0.014955871),
 ('สั่ง', 0.014933768),
 ('ปลั๊ก', 0.014089214),
 ('ค้า', 0.012942444)]
```
## Document Clustering

### K-mean
The most frequent words unite the three clusters with a common theme, as customers from Cluster 0, Cluster 1, and Cluster 2 all consistently emphasize the significance of 'สินค้า' and 'ดี'. This collective focus effectively underscores an appreciation shared for product quality.
```
Cluster ID : 0
Most common words include : [('สินค้า', 4), ('ดี', 2), ('ค้า', 2), ('คุณภาพ', 1), ('มั่นใจ', 1), ('ปลอด', 1), ('ภัการ', 1), ('จัดส่ง', 1), ('สั่งการ', 1), ('แพ็ค', 1)]

Cluster ID : 1
Most common words include : [('ดี', 7), ('สินค้า', 5), ('ไฟ', 5), ('สั่ง', 4), ('ปลั๊ก', 4), ('ช่อง', 3), ('Toshino', 2), ('สาย', 2), ('งาน', 2), ('แพค', 2)]

Cluster ID : 2
Most common words include : [('สินค้า', 8), ('ดี', 5), ('ราคา', 2), ('คุ้มค่า', 2), ('คุ้ม', 1), ('ค่า', 1), ('รับประกัน', 1), ('ไว', 1), ('แพง', 1), ('เลือก', 1)]
```

### Cosine Similarity
In this case, Using Cosine Similarity, we've been able to clearly distinguish the differences between the groups.

Cluster ID : 0 is 'Quality Products'
- ongoing quality improvements to meet customer expectations.

Cluster ID : 1 is 'Issues and Reviews'

Cluster ID : 2 is 'Packaging'
- optimize packaging for a better customer experience

```
Cluster ID : 0
Most common words include :[('ดี', 32), ('สินค้า', 32), ('ช่อง', 10), ('ปลั๊ก', 10), ('ไฟ', 9), ('งาน', 6), ('คุณภาพ', 6), ('ยี่ห้อ', 5), ('ค้า', 5), ('สาย', 4)]

Cluster ID : 1
Most common words include :[('ดี', 7), ('เสียหาย', 2), ('รีวิว', 2), ('แพคมา', 2), ('แพคส่ง', 1), ('ไวดี', 1), ('ห่อ', 1), ('ภาพ', 1), ('แนบ', 1), ('ใบ', 1)]

Cluster ID : 2
Most common words include :[('บับเบิ้ล', 2), ('กล่อง', 2), ('ไฟ', 2), ('เสียบ', 2), ('/', 2), ('ลอง', 2), ('แพคมา', 1), ('ดี', 1), ('หนา', 1), ('สภาพ', 1)]
```

