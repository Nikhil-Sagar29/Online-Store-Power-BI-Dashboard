# Datasets 
---

File structure
--

|SI.No  |Property	        | Description|
|-------|-----------------|-----------|
|  1    |event_time	      | Time when event happened at (in UTC).|
|  2    |event_type	      | Only one kind of event: purchase.|
|  3    |product_id	      | ID of a product|
|  4    |category_id	    | Product's category ID.|
|  5    |category_code	  | Product's category taxonomy (code name) if it was possible to make it. Usually present for meaningful categories and skipped for different kinds of accessories.|
|  6    |brand	          | Downcased string of brand name. Can be missed.|
|  7    |price	          | Float price of a product. Present.|
|  8    |user_id          |	Permanent user ID.|
|  9    |user_session     |	Temporary user's session ID. Same for each user's session. Is changed every time user come back to online store from a long pause.|
    
    
Event types
---    
Events can be:

1. view - a user viewed a product
2. cart - a user added a product to shopping cart
3. remove_from_cart - a user removed a product from shopping cart
4. purchase - a user purchased a product

## Raw Datasets

### E-Commerce behavior data from multi category store - [![Dataset](https://img.shields.io/badge/Datasets-black)](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store?select=2019-Nov.csv)

The Dataset Link above involves:
1. Contains raw, uncleaned, and unfiltered data
2. Total size: 14.65 GB
             -  November Dataset: 9.08 GB
             -  October Dataset: 5.67 GB
3. High storage and processing requirements
4. May cause performance issues in Power BI / SQL
5. Suitable for full-scale data engineering workflows
   
## Cleaned & Optimized Datasets
---

### E-Commerce behavior data from multi category store - [![Dataset](https://img.shields.io/badge/Datasets-black)](https://drive.google.com/drive/folders/1fm8_YiuNl2xeF80MImwVU08tBQI50KD6?usp=sharing)

The Dataset Link above Invloves:
1. Cleaned and filtered for efficient analysis
2. Reduced size: 40 MB (zipped), Includes :
    - Cleaned November dataset (~97.6 MB)
    - Cleaned October dataset (~79.3 MB)
    - Appended dataset (Oct + Nov) (~257.2 MB)
    - Date table for time-based analysis (~2 KB)
      
3. Optimizations Applied:
   - Removed unnecessary columns
   - Filtered only relevant records (e.g., purchase events)
   - Cleaned datetime format (removed UTC inconsistencies)
   - Structured for Power BI and SQL performance

##### Note : 

The cleaned dataset preserves the original structure and is optimized only for analysis performance.
     
4. Benefits:
   - Faster loading and processing
   - Optimized for dashboarding
   - Suitable for EDA and business analysis projects

       
   
