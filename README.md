# Project Cafe Rewards Offer

## Description of the data
The data being worked on is data of customers' interaction with offers by Cafe Rewards within 30 days (data source: [mavenanalytics.io](mavenanalytics.io/data-playground), ‘Cafe Rewards Offer’). The dataset contains the following data frames:
* customers (called `df_cs`): customers' demography
* events (`df_events`): data of transactions and customers' interaction with offers (the file size is too large to include here)
* offers (`df_offers`): contain details of offers
* `data_dictionary`: the dictionary of every column in the datasets.

During this period, customers were given offers with a certain pattern (related to time and the type of offer) which had been planned to maximize the possibility of the customer's purchase. The types of offers are grouped into three types: **BOGO** (Buy One, Get One), **discount**, and **informational** (advertisement of cafe's product). Each type has several offers with different `offer_id` and offer details such as difficulty (the minimum amount needed), reward, duration, and cafe's channel which is used to spread the offers.

The customer interaction with the offer begins with the `offer received` event, followed by `offer viewed`, and `offer completed` which means the customer made a transaction involving the offer. The event written in `df_events` is the last event/interaction the customer performed. While regular purchases without involving an offer are labeled as `transaction`. 

The analysis was conducted to see the effect of the offer on the number of transactions that occurred, identify the popularity of the offer, and perform customer segmentation based on their demography.

## Insights
Based on the data, within 30 days, the offers had a positive impact in increasing the number of transactions. Maximizing the influence of these offers can be done by **increasing the conversion and completion rate** of each offer. A high conversion rate means that customers will have easier access to the offer, leading to the hope that it can increase the chances of the offer being completed by the customer.
* To **increase the conversion rate**, it is necessary to review the channels used to spread the offers. The more channels used, the greater the opportunity for customers to view the offer. Based on the analysis that has been done, *the 'social' channel* is better at increasing conversion rates than other channels.
* **Increasing the completed rate** can be done by adjusting the offer details (difficulty, duration, and reward) with customer preferences. In general, customers tend to complete *BOGO offers* with a smaller minimum amount (difficulty) and a longer duration where offers with greater difficulty contribute to a greater number of sales and smaller difficulties contribute to transaction volume. Meanwhile, in *the discount offer type*, customers do not show any particular preferences.

Recommendations that can be given to **increase the chances of completing offers for all groups** are to provide special offers for new customers (membership period <1 year) and for senior age groups. Adjusting the difficulty of the offer with the income of customers who are dominated by income <80,000 can also increase the chances of more customers completing the offer.
