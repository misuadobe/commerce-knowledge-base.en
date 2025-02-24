---
title: 'MDVA-35092: Vimeo Error: "Video not found"'
labels: 2.3.5-p1,2.3.5-p2,2.3.6-p1,2.4.0,2.4.0-p1,2.4.1,2.4.2,QPT 1.0.17,QPT patches,Magento Commerce,Magento Commerce Cloud,Quality Patches Tool,Vimeo,error,support tools,video,Adobe Commerce,cloud infrastructure,on-premises
description: "The MDVA-35092 patch fixes the issue where you see Error: *\"Video not Found\"*. This error message displays when you enter a Vimeo video using the native Add Video interface in the product admin of Adobe Commerce. This patch is available when the [Quality Patches Tool (QPT)](https://support.magento.com/hc/en-us/articles/360047139492) 1.0.17 is installed. Please note that the issue was fixed in Adobe Commerce 2.4.3."
---

# MDVA-35092: Vimeo Error: "Video not found"

The MDVA-35092 patch fixes the issue where you see Error: *"Video not Found"*. This error message displays when you enter a Vimeo video using the native Add Video interface in the product admin of Adobe Commerce. This patch is available when the [Quality Patches Tool (QPT)](https://support.magento.com/hc/en-us/articles/360047139492) 1.0.17 is installed. Please note that the issue was fixed in Adobe Commerce 2.4.3.

## Affected products and versions

**The patch is created for Adobe Commerce version:**

Adobe Commerce on cloud infrastructure 2.4.1

**Compatible with Adobe Commerce versions:**

Adobe Commerce on-premises and Adobe Commerce on cloud infrastructure 2.3.5 - 2.4.2

>[!NOTE]
>
>The patch might become applicable to other versions with new Quality Patches Tool releases. To check if the patch is compatible with your Adobe Commerce version, update the `magento/quality-patches` package to the latest version and check the compatibility on the [QPT landing page](https://devdocs.magento.com/quality-patches/tool.html#patch-grid). Use the patch ID as a search keyword to locate the patch.

## Issue

The Vimeo simple API stops working as expected.

<u>Steps to reproduce</u>:

1. Log in to the Admin.
1. To edit an existing product, go to **CATALOG** > **Products** > **Edit**, or to create a new product, go to **CATALOG** > **Products** > **Edit** > **Add Product**.
1. Click the **Images And Videos** tab on the Product page.
1. Click **Add Video** and add a Vimeo video's URL. Click **Save**.

<u>Expected results</u>:

The new video is found and saved.

<u>Actual results</u>:

Error: *"Video not Found"* is displayed.

## Apply the patch

To apply individual patches, use the following links depending on your deployment method:

* Adobe Commerce or Magento Open Source on-premises: [Software Update Guide > Apply Patches](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching/mqp.html) in our developer documentation.
* Adobe Commerce on cloud infrastructure: [Upgrades and Patches > Apply Patches](https://devdocs.magento.com/cloud/project/project-patch.html) in our developer documentation.

## Related reading

To learn more about Quality Patches Tool, refer to:

* [Quality Patches Tool released: a new tool to self-serve quality patches](https://support.magento.com/hc/en-us/articles/360047139492) in our support knowledge base.
* [Check if patch is available for your Adobe Commerce issue using Quality Patches Tool](https://support.magento.com/hc/en-us/articles/360047125252) in our support knowledge base.

For info about other patches available in QPT, refer to the [Patches available in QPT](https://support.magento.com/hc/en-us/sections/360010506631-Patches-available-in-QPT-tool-) section.