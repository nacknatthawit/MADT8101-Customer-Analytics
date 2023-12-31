# Customer Segmentation & Product Recommendation

**BUSINESS OVERVIEW :**

HDI, operating as a network marketing enterprise in Asia, offers a diverse range of natural products derived from bees. Within its product lineup, HDI features five primary categories: adult and children's products, personal care items, skincare solutions, and a selection of food and beverages.

**DATA :**  
- Member data: HDI company master data of downline and their sponsor
- Transaction 2021 - 2023: HDI company product sales from year 2021 to 2023

**BUSINESS OBJECTIVE :**

- Increase sales by strategically targeting all customer groups to maximize our sales potential.

## Customer Segmentation

**Data Prepocessing :**
Create a Customer Single View with features such as
- ent
- join_duration(Month)
- No_downline
- avg_amount
- avg_amount_3months
- avg_amount_6months
- transaction_count
- transaction_count_3months
- transaction_count_6months
- avg_ticket_size
- avg_ticket_size_3month
- avg_ticket_size_6month
- online(ratio 0 to 1)
- online_3month(ratio 0 to 1)
- online_6month(ratio 0 to 1)
- last_transaction_day
- mean_time_between_purchase

**Clustering with K-Means :**

Select number of clusters = 4

**Result**

![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/ec263ddc-0c6c-4767-b48d-300edba42be0)

**Problem :** 
It is challenging to classify cluster0 as either composed of newcomers or churned customers due to their combination of low average spending(last 3 months), low recent transactions(last 3 months), small average ticket sizes(last 3 months), and a high number of days since their last transaction.

**Solution:** 
Creating a new cluster by splitting cluster 0 based on the condition that their average spending in the last 3 months and last 6 months is both equal to zero.

**Result**

![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/5f7137c7-cfa4-4bb4-ac04-6b6599a66fc5)

### Business Strategies by cluster

Pursuing the objectives of increased transaction frequency, higher average ticket size, and reduced meantime between purchases for each tier, with the ultimate aim of elevating members to higher tier levels.
![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/587e4fe3-47f0-413b-ab28-57cd51f96c58)

## Product Recommendation

**Method :**

- Colaborative Filtering (Item-based filtering)
- Market Basket Analysis

### Colaborative Filtering (Item-based filtering)

**Example Result (Cluster 0)**

Cosine similarity matrix between 2 products.

![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/b3a6f668-d060-4de1-92b7-683806f07cae)

Top 10 high similarity between 2 products.

![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/33b1bfed-1685-4565-a3eb-7b810e8d073f)

Recommendation Algorithm for member if cluster = 0 and product = 'KC4C41'

Top 5 recommended items similar to KC4C41 :

KC4C44   0.97

KC4C4C   0.92

KC4CCW   0.90

KC4C4R   0.88

KC4C4E   0.86

**Use case:**
If a member is a newbie and has successfully sold 'KC4C41,' we recommend them to consider selling other related items such as 'KC4C44,' 'KC4C4C,' 'KC4CCW,' 'KC4C4R,' and 'KC4C4E'.

### Market Basket Analysis

Market basket analysis is a data mining technique used to discover patterns and associations among products or items that are frequently purchased together by customers. It aims to uncover relationships between items in a dataset, helping businesses identify which products are often bought in conjunction with each other.

**Result**

![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/11ddb17b-899f-4d4a-97fc-e1c978b03318)

**Use case:** 

From the results of a market basket analysis, businesses can identify pairs or groups of products that are often purchased together. This information can be used to implement cross-selling strategies, where customers are encouraged to buy complementary products or items that tend to go hand-in-hand.

## Segment Movement Analysis

To Segment Movement Analysis of memberships, we utilize labeled member data from the year 2023, which was derived from clustering. We construct a classification model to predict the historical behavior of members and determine which clusters they were previously associated with. This model enables us to visualize changes in the behavior patterns of individual members over the course of the year, presenting the transitions with a Sankey diagram.

![image](https://github.com/nacknatthawit/MADT8101-Customer-Analytics/assets/115746160/a9316b05-6910-41b0-8245-21426957be82)

**Result**

Segment movement analysis reveals that a significant portion of our members have exhibited churn behavior. However, it's worth noting that a subset of members who churned in both 2021 and 2022 have subsequently reactivated their memberships.
