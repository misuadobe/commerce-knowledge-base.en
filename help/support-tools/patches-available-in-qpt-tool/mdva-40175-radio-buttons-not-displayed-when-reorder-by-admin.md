---
title: "MDVA-40175: Radio buttons not displayed when reorder"
labels: QPT patches,Quality Patches Tool,Support Tools,Magento,Adobe Commerce,cloud infrastructure,on-premises,QPT 1.1.10,2.4.0,2.4.0-p1,2.4.1,2.4.1-p1,2.4.2,2.4.2-p1,2.4.2-p2,Radio buttons,reorder,delivery methods
description: "The MDVA-40175 patch solves the issue where the Radio buttons are not displayed when users try to reorder. This patch is available when the [Quality Patches Tool (QPT)](https://support.magento.com/hc/en-us/articles/360047139492) 1.1.10 is installed. The patch ID is MDVA-40175. Please note that the issue was fixed in Adobe Commerce 2.4.3."
---

# MDVA-40175: Radio buttons not displayed when reorder

The MDVA-40175 patch solves the issue where the Radio buttons are not displayed when users try to reorder. This patch is available when the [Quality Patches Tool (QPT)](https://support.magento.com/hc/en-us/articles/360047139492) 1.1.10 is installed. The patch ID is MDVA-40175. Please note that the issue was fixed in Adobe Commerce 2.4.3.

## Affected products and versions

**The patch is created for Adobe Commerce version:**

* Adobe Commerce (all deployment methods) 2.4.2-p1

**Compatible with Adobe Commerce versions:**

* Adobe Commerce (all deployment methods) 2.4.0 - 2.4.2-p2

>[!NOTE]
>
>The patch might become applicable to other versions with new Quality Patches Tool releases. To check if the patch is compatible with your Adobe Commerce version, update the `magento/quality-patches` package to the latest version and check the compatibility on the [QPT landing page](https://devdocs.magento.com/quality-patches/tool.html#patch-grid). Use the patch ID as a search keyword to locate the patch.

## Issue

Radio buttons are not displayed in the Payment & Shipping Information section when users try to reorder.

<u>Prerequisites</u>:

1. A Customer account with a shipping address and a billing address is created.
1. A Simple Product is created.
1. Several delivery methods are configured.
1. At least one order is created.

<u>Steps to reproduce</u>:

1. Go to the Admin panel > **Sales** > **Orders**.
1. Select the created order.
1. Click the **View** link.
1. Click the **Reorder** button.
1. Scroll down the page to the **Payment & Shipping Information** section.
1. Click the **Click to change shipping method**.

<u>Expected results</u>:

The list of delivery methods with radio buttons appear.

<u>Actual results</u>:

The list of delivery methods without radio buttons appear.

## Apply the patch

To apply individual patches, use the following links depending on your deployment method:

* Adobe Commerce or Magento Open Source on-premises: [Software Update Guide > Apply Patches](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching/mqp.html) in our developer documentation.
* Adobe Commerce on cloud infrastructure: [Upgrades and Patches > Apply Patches](https://devdocs.magento.com/cloud/project/project-patch.html) in our developer documentation.

## Related reading

To learn more about Quality Patches Tool, refer to:

* [Quality Patches Tool released: a new tool to self-serve quality patches](https://support.magento.com/hc/en-us/articles/360047139492) in our support knowledge base.
* [Check if patch is available for your Adobe Commerce issue using Quality Patches Tool](https://support.magento.com/hc/en-us/articles/360047125252) in our support knowledge base.

For info about other patches available in QPT, refer to [Patches available in QPT](https://devdocs.magento.com/quality-patches/tool.html#patch-grid) in our developer documentation.