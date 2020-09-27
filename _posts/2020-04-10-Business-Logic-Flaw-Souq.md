---
layout: single
title: "Business Logic Flaw on Souq.com"
header:
  overlay_image: blog-cover.png
---

## Vulnerability Writeup

Affected Endpoint: ```https://egypt.souq.com/eg-ar/account.php```

### How to Reproduce

1- Select any product you want to buy, but it must has the free shipping option above specific amount of money, For example: Gym Bar which cost ```139``` EG pounds an has free shipping option if you buy things above ```250``` EG pounds.

2- Then if you buy one product below the free shipping limit the total price will be the product price + the shipping price, For example: ```139 + 26 = 165``` EG pounds.

3- Now buy things above the free shipping limit, For example: you can buy two Gym Bar which will cost ```278``` EG pounds and make the purchase.

4- Visit this link ```https://egypt.souq.com/eg-ar/account.php``` and cancel one of your items, For example: we will cancel of the Gym Bar so the remaining items will be only one Gym Bar which will cost ```139``` EG pounds the original price without the shipping price, so the total price would be ```139``` EG pounds instead of ```165``` EG pounds.

### Impact

This vulnerability can lead to decrease the price of the products by deleting the shipping price of the product and this lead to money lose to the company.

### Proof of Concept

<iframe width="420" height="315" src="https://www.youtube.com/embed/GIZhjhgx_wQ"> </iframe> 

