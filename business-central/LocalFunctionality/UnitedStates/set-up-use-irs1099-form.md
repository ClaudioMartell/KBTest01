---
title: Set up and use the IRS 1099 form [US]
description: Learn how to set up the 1099 tax form boxes so that you can submit the required reports.
author: altotovi
ms.topic: conceptual
ms.search.keywords: local, 1099
ms.search.form: 26, 29, 50, 51, 10015, 10016, 10018, 10900
ms.date: 03/28/2024
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
---

# Set up and use the IRS 1099 form

> [!IMPORTANT]
> From version 24.0, you can start using this new 1099 functionality for better transparency, integration, and automation. To do this, you must enable this new feature using the **Feature Management** page. You can find more details [here](introduction-to-the-irs-forms.md). If you do not enable it earlier, [!INCLUDE[prod_short](../../includes/prod_short.md)] will automatically do it with the version 27.0, so we recommend to start using the new version right now.  

The Internal Revenue Service (IRS) requires one or more versions of the 1099 tax form for payments to vendors. Copies of these forms must be sent to vendors annually on or before the last day of January. On your purchase documents, you can specify that the document is 1099 liable, and you can specify the 1099 code for the vendor.

## Setup

Before you start using [!INCLUDE[prod_short](../../includes/prod_short.md)], you must set up **1099 Form Boxes** and **Vendors** as 1099 liable. The most common 1099 codes are already set up for you, and they're defined on the **1099 Form Box** page, where you can also add new 1099 codes. Before you prepare your reporting for the new year, you must first update your [!INCLUDE[prod_short](../../includes/prod_short.md)] to handle the new requirements.

### To update the 1099 form boxes

In order to support the form changes by the IRS, [!INCLUDE[prod_short](../../includes/prod_short.md)] offers the **Update Form Boxes** action to include new codes and other requirements in the 1099 form. For more information, see [Regulatory 1099 Format Changes and Details](tax-1099-changes.md).

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **1099 Form Boxes**, and then choose the related link.
2. Choose the **Update Form Boxes** action.  

> [!NOTE] 
> Don't fill out the 1099 form boxes manually. Instead, select **Update Form Boxes**.

> [!IMPORTANT]
> Running the action **Update Form Boxes** makes reporting for the previous year impossible, since some boxes change their meaning. Make sure that you have done all your reporting for the previous year before you update the form boxes to prepare your system for reporting for the new year.

### To set up a vendor as 1099 liable

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.
2. Open the relevant vendor's card.
3. On the **Payments** FastTab, in the **IRS 1099 Code** field, choose the relevant IRS 1099 code.
4. Repeat steps 2 and 3 for additional vendors.  

## Documents and entries

### To process a document as 1099 liable

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoice**, and then choose the related link.
2. Create a new entry, and then, in the **Vendor Name** field on the **Purchase Invoice** header, specify a vendor with the relevant IRS 1099 code.
3. Optionally, on the **Shipping and Payment** FastTab, in the **IRS 1099 Code** field, override the default value with another code, or delete it to have transaction without an IRS 1099 code.

    The **IRS 1099 Code** field is prepopulated with the value from the vendor card.  
4. Enter all information into the required fields for purchase invoice and post the document. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

Once the document is posted, you can go to the **Vendor Ledger Entries** list page and find that the **IRS 1099 Code** and **IRS 1099 Amount** fields are automatically populated.  

> [!TIP]
> Instead of a purchase invoice, you can also use a purchase order as the document, but in this case, the **IRS 1099 Code** field will be on the **Invoice Details** FastTab.

### To correct posted entries

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.
2. Open the relevant vendor's card.
3. On the **Vendor Card** page, choose the **Ledger Entries** action to open the **Vendor Ledger Entries** page. Here, you can review a list of all transactions for your vendor.  
4. Locate the entry that you want to correct.  
5. If you want to change the IRS code, find the **IRS 1099 Code** field, and then change the code for the relevant entry.  
6. If you want to change the amount, find the **IRS 1099 Amount** field, and then update the existing amount.  

## Reporting

### To find the IRS 1099 statistics

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.
2. Open the relevant vendor's card.
3. On the **Vendor Card** page, choose the **1099 Statistics** action to open the **Vendor 1099 Statistics** page.

### To review IRS 1099 amounts for a specific vendor

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.
2. Open the relevant vendor's card.
3. On the **Vendor Card** page, choose the **Vendor 1099 Information** action to open the **Vendor 1099 Information** report.  
4. Set filters for vendor number and date, and then choose to print or preview the report.

### To print the 1099 tax forms

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **1099 Form Boxes**, and then choose the related link.
2. On the **1099 Form Boxes** page, choose the **Reports** action, and then choose one of vendor 1099 reports for printing:

   - **Vendor 1099 Div** - Prints the federal form 1099-DIV for dividends and distribution. You can print all or specific 1099-DIV forms. The report uses the codes that apply to the DIV form amount boxes from the **1099 Form Boxes** page.
   - **Vendor 1099 Int** - Prints the federal form 1099-INT for interest income. You can print all or specific 1099-INT forms. The report uses the codes that apply to the INT form amount boxes from the **1099 Form Boxes** page.
   - **Vendor 1099 Misc** - Prints the federal form 1099-MISC for miscellaneous income. You can print all or specific 1099-MISC forms. The report uses the codes that apply to the MISC form amount boxes from the **1099 Form Boxes** page.
   - **Vendor 1099 Nec** – Prints the federal form 1099-NEC for nonemployee compensation. You can print all or specific 1099-NEC forms. The report uses the codes that apply to the NEC form amount boxes from the **1099 Form Boxes** page.

> [!NOTE]
> Regulatory changes affecting this report and the table data are generally handled in end-of-year updates. For more information, see [Regulatory 1099 Form Box Changes](tax-1099-changes.md).

### To submit the 1099 tax forms electronically

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **1099 Form Boxes**, and then choose the related link.
2. On the **1099 Form Boxes** page, choose the **Vendor 1099 Magnetic Media** action.
3. Specifies the 1099 forms that can be exported.

The report uses the codes that apply to the form amount boxes from the **1099 Form Boxes** page. The codes are mapped to the form boxes in the file layouts of this report, therefore the table data and report version for a particular tax year must be in agreement. If any custom codes are added to the table these must be mapped to the form boxes inside this object.

> [!NOTE]
> The form information exported by this report is the same as the reports that print 1099 forms that are described in the previous section.

> [!NOTE]
> Regulatory changes affecting this report and the table data are generally handled in end-of-year updates.

## See also

[Regulatory 1099 Format Changes and Details](tax-1099-changes.md)  
[United States Local Functionality](united-states-local-functionality.md)  
[Register New Vendors](../../purchasing-how-register-new-vendors.md)  
[Record Purchase](../../purchasing-how-record-purchases.md)  
[Work with [!INCLUDE[prod_short](../../includes/prod_short.md)]](../../ui-work-product.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
