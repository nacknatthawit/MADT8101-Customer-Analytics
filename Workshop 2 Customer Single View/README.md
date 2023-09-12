# Customer Single View

### What is a Customer Single View

Customer Single View is an accessible and consistent set of information about how a customer has interacted with your coompany, including what they have bought, their personal data, opinions and feedback.

## Create Customer Single View

**DATA :**
- Supermarket Dataset

**Vairable and Discerption :**

![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/047ad29f-b07d-4dc8-ae5e-46e75fd4f281)

**Create a Customer Single View with features such as**
- custommer code (CUST_CODE)
- Average basket size (avg_bkt_size)
- Average basket size in 3 month (avg_bkt_size_3m)
- Average basket size in 6 month (avg_bkt_size_6m)
- Total number of transactions (total_trans)
- Number of transactions in 3 month (total_trans_3m)
- Number of transactions in 6 month (total_trans_6m)
- Total spending (total_spend)
- Total spending in 3 month (total_spend_3m)
- Total spending in 6 month (total_trans_6m)
- Mean time between purchase (mean_time_between_purchase)	
- Member duration (Day) (mem_duration)
- First visit (first_visit)
- Last visit (last_visit)

**Result**

![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/f1339094-c3ff-43a3-967b-a971d854b9af)

## Basic Customer Analytics

**Objective :** Upspending current customers.

**Method :** Compare spending between short-period and long-period to identify who is spending more.

- From Customer Single view find spending per transaction last 3 month and spending per transaction last 6.
- Use only member spending per transaction last 3 month and spending per transaction last 6 month not equal to zero.
- Find percentile for each member with spending per transaction last 3 month and spending per transaction last 6 month.
- Compare member when percentile spending per transaction last 3 month more then percentile spending per transaction last 6 month.
- Compare member when spending per transaction last 3 month more then spending per transaction last 6 month.

**Result :** This member, who is spending more, presents an opportunity for up-selling or cross-selling, as their higher spending suggests a likelihood of increased purchases.

![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/4e8e592d-ed45-4569-b134-4f431de9da8f)

Once the members with a higher likelihood of making a purchase have been identified, the next step involves deciding between cross-selling and up-selling strategies. For instance, in the case of cross-selling, product recommendations can be analyzed to determine which products are frequently purchased together.


