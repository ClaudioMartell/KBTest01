---
title: How to Post the Year-End Closing Entry [FR]
description: This article tells you how to post the year-end closing entries after you use the Close Income Statement batch job.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords:
ms.date: 06/18/2021
ms.author: bholtorf

ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Post the Year-End Closing Entry in the French Version

After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.  

## To post the year-end closing entry  

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.  
2. Review the entries.  
3. Choose the **Post** action.  
4. In the posting confirmation page, choose the **Yes** button.  

If an error is detected, an error message is displayed. If the posting is successful, the system removes the posted entries from the journal.  

Once posted, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.  

## See Also

[Year End Processes Overview](year-end-processes-overview.md)   
[Close Years](how-to-close-years.md)   
[Fiscally Close Years](how-to-fiscally-close-years.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]