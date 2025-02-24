---
title: 'MDVA-44188: Emails are not sent to IDs containing ".-"'
labels: QPT patches,Quality Patches Tool,Support Tools,QPT 1.1.13,email,error,Magento,Adobe Commerce,cloud infrastructure,on-premises,2.4.3,2.4.3-p1,2.4.4
description: "The MDVA-44188 patch fixes the issue where emails are not sent to the email IDs containing `.-`. This patch is available when the [Quality Patches Tool (QPT)](https://support.magento.com/hc/en-us/articles/360047139492) 1.1.13 is installed. The patch ID is MDVA-44188. Please note that the issue is scheduled to be fixed in Adobe Commerce 2.4.5."
---

# MDVA-44188: Emails are not sent to IDs containing ".-"

The MDVA-44188 patch fixes the issue where emails are not sent to the email IDs containing `.-`. This patch is available when the [Quality Patches Tool (QPT)](https://support.magento.com/hc/en-us/articles/360047139492) 1.1.13 is installed. The patch ID is MDVA-44188. Please note that the issue is scheduled to be fixed in Adobe Commerce 2.4.5.

## Affected products and versions

**The patch is created for Adobe Commerce version:**

* Adobe Commerce (all deployment methods) 2.4.3-p1

**Compatible with Adobe Commerce versions:**

* Adobe Commerce (all deployment methods) 2.4.3 - 2.4.4

>[!NOTE]
>
>The patch might become applicable to other versions with new Quality Patches Tool releases. To check if the patch is compatible with your Adobe Commerce version, update the `magento/quality-patches` package to the latest version and check the compatibility on the [QPT landing page](https://devdocs.magento.com/quality-patches/tool.html#patch-grid). Use the patch ID as a search keyword to locate the patch.

## Issue

Unable to send emails to email IDs that contain `.-` in their user name.

<u>Steps to reproduce</u>:

1. Register a customer with an email address containing `.-`. For example, `.-foo@example.com`.
1. Place an order.

<u>Expected results</u>:

User with the email ID containing `.-` receives emails as usual.

<u>Actual results</u>:

Email is not sent to the email ID containing `.-`. The following error is shown in error logs: *Could not add an invalid email address to the mailing queue*.

## Apply the patch

To apply individual patches, use the following links depending on your deployment method:

* Adobe Commerce or Magento Open Source on-premises: [Software Update Guide > Apply Patches](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching/mqp.html) in our developer documentation.
* Adobe Commerce on cloud infrastructure: [Upgrades and Patches > Apply Patches](https://devdocs.magento.com/cloud/project/project-patch.html) in our developer documentation.

## Related reading

To learn more about Quality Patches Tool, refer to:

* [Quality Patches Tool released: a new tool to self-serve quality patches](https://support.magento.com/hc/en-us/articles/360047139492) in our support knowledge base.
* [Check if patch is available for your Adobe Commerce issue using Quality Patches Tool](https://support.magento.com/hc/en-us/articles/360047125252) in our support knowledge base.

For info about other patches available in QPT, refer to [Patches available in QPT](https://devdocs.magento.com/quality-patches/tool.html#patch-grid) in our developer documentation.