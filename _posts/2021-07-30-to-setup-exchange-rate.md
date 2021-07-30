---
layout: posts
title: "Business Central - To set up currency exchange rate updates"
categories: ['Dynamics Business Central', 'Finance']
classes: wide
excerpt: "How to set up automatic currency exchange rate updates on Dynamics Business Central without extra cost."
---

### Objective
It's hassle to update exchange rate everyday. We can set up automatic updates for exchange rates on Dynamics Business Central.

### Procedure
1. Choose the ![Alt](/assets/images/icon_search.png "Search Icon") icon, enter ***Currency Exchange Rate Services***, and then choose the related link. \

2. On the ***Currency Exchange Rate Services*** page, choose the ***New*** action. \
![full](/assets/images/bc_exchange_rate_01.png "Business Central - Exchange Rate Updates"){: .full}

3. Key in following fields like screenshot below. \
![full](/assets/images/bc_exchange_rate_02.png "Business Central - Exchange Rate Updates"){: .full}
- Code: FLOATRATES
- Description: from floatrates.com
- Service URL: http://www.floatrates.com/daily/nzd.xml
- Service Provider: floatrates.com
- Parent Node for Currency Code: /channel/item/targetCurrency
- Currency Code: /channel/item/targetCurrency
- Starting Date: /channel/item/pubDate
- Exchange Rate Amount: /channel/item/exchangeRate
- Relational Exch. Rate Amount: 1 (under Default Value column)

4. Click on drop-down of Transformation Rule column on Starting Date row then click ***New*** action. \
![full](/assets/images/bc_exchange_rate_03.png "Business Central - Exchange Rate Updates"){: .full}

5. Key in following fields like screenshot below. Then click ***OK***. \
![full](/assets/images/bc_exchange_rate_04.png "Business Central - Exchange Rate Updates"){: .full}
- Code: FLOAT_DATE
- Transformation Type: Substring
- Next Transformation Rule: US_DATE_FORMAT
- Starting Text: “ “ (This is space not blank)
- Ending Text: “ GMT” (This is a space, then GMT)

6. Click on ***Enabled*** button. \
![full](/assets/images/bc_exchange_rate_05.png "Business Central - Exchange Rate Updates"){: .full}

7. Then click on ***Yes*** on popped up window. \
![full](/assets/images/bc_exchange_rate_06.png "Business Central - Exchange Rate Updates"){: .full}

8. Click on ***Process*** and ***Set Status to Ready***. \
![full](/assets/images/bc_exchange_rate_07.png "Business Central - Exchange Rate Updates"){: .full}

9. Choose the ![Alt](/assets/images/icon_search.png "Search Icon") icon, enter ***Currencies***, and then choose the related link. Then check whether Exchange Rates are updated. If you don’t see any exchange rates, then click on ***Exchange Rate Service -> Update Exchange Rates***. \
![full](/assets/images/bc_exchange_rate_08.png "Business Central - Exchange Rate Updates"){: .full}