---
title: "MDVA-23764 Magento patch: error when loading dynamic blocks"
labels: 2.3.3,2.3.3-p1,2.3.4,2.3.4-p2,QPT 1.0.13,Magento Commerce,Magento Commerce Cloud,Quality Patches Tool,dynamic block,support tools
description: "The MDVA-23764 Magento patch fixes the bug in"
---

# MDVA-23764 Magento patch: error when loading dynamic blocks

The MDVA-23764 Magento patch fixes the bug in

```php
JsFooterPlugin.php
```

that affects the display of dynamic blocks. This patch is available when the [Quality Patches Tool (QPT)](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching.html#mqp) 1.0.13 is installed. Please note that the issue was fixed in Magento 2.3.5.

## Affected products and versions

 **The patch is created for Magento version:** Magento Commerce Cloud 2.3.3.

 **Compatible with Magento versions:** Magento Commerce and Magento Commerce Cloud 2.3.2 - 2.3.4-p2.

>[!NOTE]
>
>The patch might become applicable to other versions with new Quality Patches Tool releases. To check if the patch is compatible with your Adobe Commerce version, update the `magento/quality-patches` package to the latest version and check the compatibility on the [QPT landing page](https://devdocs.magento.com/quality-patches/tool.html#patch-grid). Use the patch ID as a search keyword to locate the patch.

## Issue

 <u>Steps to reproduce:</u>

Try to load a URL that looks like following: https://\[magento domain\]/banner/ajax/load/.

 <u>Actual result:</u>

An error similar to the following is thrown: *Uncaught TypeError: strpos() expects parameter 1 to be string, null given in...(line of code)* .

 <u>Expected result:</u>

URL is loaded without errors.

## Apply the patch

For instructions on how to apply an QPT patch, use the following links depending on your Magento product:

* Magento Commerce: DevDocs [Apply patches using Quality Patches Tool](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching/mqp.html) .
* Magento Commerce Cloud: DevDocs [Upgrades and Patches > Apply patches](https://devdocs.magento.com/cloud/project/project-patch.html) .

## Related reading

To learn more about Quality Patches Tool, refer to:

* [Quality Patches Tool released: a new tool to self-serve quality patches](https://support.magento.com/hc/en-us/articles/360047139492) .
* [Check if patch is available for your Magento issue using Quality Patches Tool](https://support.magento.com/hc/en-us/articles/360047125252) .

For info about other patches available in QPT tool, refer to the [Patches available in QPT tool](https://support.magento.com/hc/en-us/sections/360010506631-Patches-available-in-QPT-tool-) section.