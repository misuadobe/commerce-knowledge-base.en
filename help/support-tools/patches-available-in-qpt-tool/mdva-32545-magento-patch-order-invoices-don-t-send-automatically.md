---
title: "MDVA-32545 patch: order invoices don't send automatically"
labels: 2.3.0,2.3.1,2.3.2,2.3.2-p2,2.3.3,2.3.3-p1,2.3.4,2.3.4-p1,2.3.4-p2,2.3.5,2.3.5-p1,2.3.5-p2,2.3.6,2.4.0,2.4.0-p1,2.4.1,QPT 1.0.13,QPT patches,Magento Commerce,Magento Commerce Cloud,Quality Patches Tool,order invoices,sale transaction type,send automatically,Adobe Commerce,cloud infrastructure,on-premises,quality patches for Adobe Commerce,Magento Open Source
description: "The MDVA-32545 patch fixes the issue where Invoice emails don't automatically send to the customer for orders placed from the Admin. This affects any payment method with the **Sale** transaction type, like **Braintree** or **PayPal Payflow Pro**."
---

# MDVA-32545 patch: order invoices don't send automatically

The MDVA-32545 patch fixes the issue where Invoice emails don't automatically send to the customer for orders placed from the Admin. This affects any payment method with the **Sale** transaction type, like **Braintree** or **PayPal Payflow Pro**.

This patch is available when the [Quality Patches Tool (QPT)](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching.html#mqp) 1.0.13 is installed. Please note that the issue was fixed in Adobe Commerce version 2.4.2.

## Affected products and versions

**The patch is created for Adobe Commerce version:**

Adobe Commerce on cloud infrastructure 2.3.2-p2

**Compatible with Adobe Commerce versions:**

Adobe Commerce on cloud infrastructure and Adobe Commerce on-premises 2.3.0 - 2.4.1

>[!NOTE]
>
>The patch might become applicable to other versions with new Quality Patches Tool releases. To check if the patch is compatible with your Adobe Commerce version, update the `magento/quality-patches` package to the latest version and check the compatibility on the [QPT landing page](https://devdocs.magento.com/quality-patches/tool.html#patch-grid). Use the patch ID as a search keyword to locate the patch.

## Issue

<u>Steps to reproduce</u>:

1. Enable any payment method with the **Sale** transaction type. (For example: **Braintree** or **PayPal Payflow Pro**.)
1. Create a simple product.
1. Create a customer account in the frontend.
1. Place an order from the Admin.

<u>Expected results</u>:

The invoice email is sent to the customer automatically, as expected.

<u>Actual results</u>:

The invoice email is not sent to the customer automatically.

## Apply the patch

To apply individual patches, use the following links depending on your deployment method:

* Adobe Commerce or Magento Open Source on-premises: [Software Update Guide > Apply Patches](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching/mqp.html) in our developer documentation.
* Adobe Commerce on cloud infrastructure: [Upgrades and Patches > Apply Patches](https://devdocs.magento.com/cloud/project/project-patch.html) in our developer documentation.

## Related reading

To learn more about Quality Patches Tool, refer to:

* [Quality Patches Tool released: a new tool to self-serve quality patches](https://support.magento.com/hc/en-us/articles/360047139492) in our support knowledge base.
* [Check if patch is available for your Adobe Commerce issue using Quality Patches Tool](https://support.magento.com/hc/en-us/articles/360047125252) in our support knowledge base.

For info about other patches available in QPT, refer to the [Patches available in QPT](https://devdocs.magento.com/quality-patches/tool.html#patch-grid) in our developer documentation.