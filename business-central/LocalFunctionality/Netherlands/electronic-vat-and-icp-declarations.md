---
title: Submit electronic VAT & ICP declarations [NL]
description: With the eXtensible Business Reporting Language (XBRL) reporter, you can submit the ICP declaration or the VAT declaration in the required XML format.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords:
ms.date: 06/12/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Submitting electronic VAT and ICP declarations in the Dutch version
Companies must submit periodic VAT and Intracommunautaire leveringen (ICP) declarations to the tax authorities.  

VAT declarations must be submitted on a monthly or quarterly basis.
ICP declarations must be submitted on a quarterly basis.

> [!NOTE]  
> ICP declarations must be submitted by companies/regions that sell goods or services to European Union (EU) countries. Purchases are not included in this declaration. <br /><br />
For a transaction to qualify for ICP, it is required that the merchandise have crossed the border physically. It is not enough that the location of an invoice address or the office of the vendor or customer is in another EU country or region.  

You can submit the VAT declarations and ICP declarations in the following ways:  

- Sign in to the website of the Dutch tax office and enter the information manually. For more information, see the [website](https://www.belastingdienst.nl/wps/wcm/connect/en/individuals/individuals) of the Dutch tax office.  

- Create an electronic declaration and submit the encrypted file through the Digipoort channel to the Dutch tax office. Digipoort is the electronic post office provided by the Dutch government for companies. It provides the common infrastructure for the communication of information between companies and the government, including VAT declarations. The reports are in the eXtensible Business Reporting Language (XBRL) format. For more information, see [Create Reports with XBRL](../../bi-create-reports-with-xbrl.md).

## To prepare for electronic declaration
Before you can send electronic declarations to the tax authorities, you must perform the following tasks:

1. Ensure that you obtain the certificates from the government. If you haven't, take the following steps to obtain the certificates:

    - Obtain a PKIoverheid certificate for the company if you don't have one already. A list of certificate providers can be found here: [https://www.logius.nl/producten/toegang/pkioverheid/aansluiten/toegetreden-csps](https://www.logius.nl/producten/toegang/pkioverheid/aansluiten/toegetreden-csps).  

    - Register a user of Digipoort, which can be done here: [https://aansluiten.procesinfrastructuur.nl/site/registratienieuw](https://aansluiten.procesinfrastructuur.nl/site/registratienieuw).

    - Obtain a **Digipoort Service certificate**, which can be obtained at the Dutch Tax Administration website: [https://aansluiten.procesinfrastructuur.nl](https://aansluiten.procesinfrastructuur.nl).

2. Enter general data and personal data received from the tax authorities on the **Elec. Tax Declaration Setup** page. For more information, see [Setting Up Electronic VAT and ICP Declarations](how-to-set-up-electronic-vat-and-icp-declarations.md).

3. Set up a VAT category code for all XML elements in the electronic VAT declaration. For more information, see [Set Up VAT Categories](how-to-set-up-vat-categories.md).

## To create an electronic declaration
1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Elec. Tax Declarations**, and then choose the related link.  
2. On the **Elec. Tax Declaration List** page, choose the **New** action.  
3. On the **Elec. Tax Declaration Card** page, fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](../../includes/tooltip-inline-tip_md.md)]  
4. Choose the **OK** button.

The XML elements and the accompanying data of the electronic declaration are displayed on the **Lines** FastTab on the **Elec. Tax Declaration Card** page.

The XBRL reporter ensures that all account numbers that are imported from Business Central are mapped to the XBRL elements in a report. The XBRL reporter also displays a list of errors of unmapped elements or accounts.

## To submit an electronic declaration
With the XBRL reporter, you can submit the Intracommunautaire Leveringen (ICP) declaration or the VAT declaration in the required XML format. When it's submitted, the file is sent to the tax authorities as defined on the **Elec. Tax Declaration Setup** page.

1. On the **Elec. Tax Declaration Card** page, choose the **Submit Electronic Tax Declaration** action.
2. Fill in the fields as described in the following table.

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Client Certificate**|Select the **PKIoverheid** certificate for the company.|  
    |**Client Certificate Password**|Enter the password that encrypts the client certificate.|
    |**Service Certificate**|Select the **Digipoort Service** certificate.|

3. Choose the **OK** button.  

The electronic declaration is submitted to the tax authorities.

> [!NOTE]  
> If there are no intra-community deliveries in the declaration period, then an electronic ICP declaration is created without XML elements for the deliveries. If you submit such a declaration, an error message will be displayed.

## To import a response message from the tax authorities
For each electronic declaration, the tax authorities send a response message. These messages must be received from the server of the tax authorities
and be processed. The first step is to import the response message into [!INCLUDE[prod_short](../../includes/prod_short.md)].

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Elec. Tax Decl. Response Msgs.**, and then choose the related link.  
2. Choose the **Receive Response Messages** action.  
3. On the **Options** FastTab, fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Client Certificate**|Select the **PKIoverheid** certificate for the company.|  
    |**Client Certificate Password**|Enter the password that encrypts the client certificate.|
    |**Service Certificate**|Select the **Digipoort Service** certificate.|  

4. Choose the **OK** button.

## To process a response message from the tax authorities
When a response message is imported, it must be processed by validating its content against the related electronic declaration. If no errors are found in the electronic declaration and the data has been processed by the tax authorities, then the **Status** field on the **Elec. Tax Declaration Card** page is changed to **Acknowledgement**.

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Elec. Tax Decl. Response Msgs.**, and then choose the related link.  
2. Choose the **Process Response Messages** action.  
3. On the **Process Response Messages Batch Job** page, select the appropriate filters, and then choose the **OK** button.  

    The processed information about the response message is displayed in the **Elec. Tax Decl. Response Msgs.**. page.  

4. To export a message or attachment, choose the **Export Response Message** action or the **Export Response Attachment** action.

## See also  
[Setting Up Electronic VAT and ICP Declarations](how-to-set-up-electronic-vat-and-icp-declarations.md)  
[Set Up VAT Categories](how-to-set-up-vat-categories.md)  
[Create Reports with XBRL](../../bi-create-reports-with-xbrl.md)  
[Netherlands Local Functionality](netherlands-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
