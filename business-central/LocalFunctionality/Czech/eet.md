---
    title: Registration of Sales (EET) 
    description: The entrepreneur who realizes „sales to be registered“ has the obligation to register sales. A “sale to be registered” is a payment in cash, by card, or by similar means, which entails a business income and which is not exempt from registration.

    author: v-pejano

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: Czech, local, CZ, VAT, Control Report
    ms.date: 10/12/2018
    ms.author: v-pejano
---


# Registration of Sales (EET)
Registration of sales (EET) is registration of sales coming from business activities and paid in cash. Information about these transactions are sent to the tax authorities. At the time of payment is created data message and sent online to the server of Tax office. As answer from the server is message with unique transaction ID, which has to be printed on the receipt for customer.

Payment methods included in EET:

*   In cash  
*   By card  
*   Check  
*   Bill of Exchange  
*   Other similar types like gift cards, coupons, bitcoin etc.  

For more information see official portal [www.etrzby.cz](http://www.etrzby.cz).  


## How it works in [!INCLUDE[d365fin](../../includes/d365fin_md.md)]
There are covered following sales documents in [!INCLUDE[d365fin](../../includes/d365fin_md.md)]:

*   Sales invoice payment  
*   Payment of prepayment invoice  
*   Refund sales credit memo  
*   Refund of prepayment invoice  
*   Cash desk receipt for sales to the G/L account (without source sales document)  

With posting of defined documents (and with defined payment method) is created EET ledger entry and based on the functionality regime is processed:

*   On-line – EET entry is created and stored in [!INCLUDE[d365fin](../../includes/d365fin_md.md)], message to the tax authorities is generated and sent to the server. Answer from the server is processed, stored and on customer’s receipt is printed unique transaction ID generated by tax authorities.  
*   Off-line - EET entry is created and stored in [!INCLUDE[d365fin](../../includes/d365fin_md.md)]. On customer’s receipt is printed unique ID generated in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] (identification of company and document). EET records are processed later by batch job.  

## Main parts of functionality
*   EET ledger entries – table where are stored and processed registered documents. Each record contains sales data required by tax authorities, needed for print on receipt and data from electronic communication. New records are created automatically by posting of source documents.  
*   EET service settings.  
*   Certificate settings.  
*   EET POS terminals – identification of registered places.  

## See Also
[Czech Local Functionality](czech-local-functionality.md)  
[Finance](../../finance.md) 
