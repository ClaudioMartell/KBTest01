---
title: How to Specify Posting Periods [FR]
description: When you specify posting periods, you limit the period in which posting is allowed.

author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords:
ms.date: 06/18/2021
ms.author: bholtorf

ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Specify Posting Periods In the French Version

When you specify posting periods, you limit the period in which posting is allowed.  

## To specify posting periods  

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Setup**, and then choose the related link.  
2. On the **General Ledger Setup** page, in the **Allow Posting From** field, specify the start date of the posting period.  
3. In the **Allow Posting To** field, specify the end date of the posting period.  

    The dates are validated against the allowed posting ranges to make sure that they belong to open fiscal years. For more information, see Allowed Posting Range.  

4. To verify what the allowed posting range is, choose the **Get Allowed Posting Range** action.  

The dates that you define here apply to the whole company, that is, to all users.  

> [!NOTE]  
> You can define different posting periods for different users and apply a posting period to a user on the **User Setup** page.

If you enter dates here, the dates entered on the **General Ledger Setup** page will not apply to these users.  

## See Also

[Fiscal Periods and Fiscal Years](fiscal-periods-and-fiscal-years.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]