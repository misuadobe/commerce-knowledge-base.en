---
title: "Fastly Error: Plugin VCL version is outdated! Please re-Upload"
labels: 2.2.x,2.3.x,Fastly error,Magento Commerce Cloud,Plugin VCL,Troubleshooting,VCL snippets,ece-tools,how to,Adobe Commerce,cloud infrastructure,on-premises
description: "This article provides a solution for when you see the message \"*Plugin VCL version is outdated! Please re-Upload.*\" in Fastly Configuration, in the Commerce Admin, due to not having installed the latest Fastly module."
---

# Fastly Error: Plugin VCL version is outdated! Please re-Upload

This article provides a solution for when you see the message "*Plugin VCL version is outdated! Please re-Upload.*" in Fastly Configuration, in the Commerce Admin, due to not having installed the latest Fastly module.

## Affected products and versions

Adobe Commerce on cloud infrastructure 2.2.x., 2.3.x<br>
Fastly: This error can affect all versions of the Fastly module except the latest one. For information on the latest release, see [Fastly release notes](https://github.com/fastly/fastly-magento2/releases) on GitHub.

## Issue

1. Log in to the Commerce Admin panel.
1. Navigate to **Stores** > **Configuration** > **Advanced** > **System** > **Full Page Cache**   **Fastly Cache.**
1. In the **Automatic Upload & Service Activation** section, there will be a "*Plugin VCL version is outdated! Please re-Upload.*" notification.
1. You attempt to upload the VCL snippets by clicking on the "Upload VCL to Fastly" button but you still see the warning "*Plugin VCL version is outdated! Please re-Upload.*"

## Cause

The Fastly extension was updated (along with a bundled VCL configuration and templates), but the updated VCL config has not been uploaded to the Fastly service. When you update the Adobe Commerce module `Fastly_Cdn`, you have to upload an updated VCL config to Fastly again.

## Solution

1.  Check that you have the latest ECE-Tools installed and at the [current version](https://devdocs.magento.com/guides/v2.2/cloud/release-notes/cloud-tools.html) in our developer documentation. ECE-Tools has a version of the Fastly package in its dependencies.
    
    This may not be the latest version of the Fastly plugin, but it is likely to be a later version than the one you have currently installed, and it is best practice to have the latest ECE-Tools installed.
    
1.  If you are not on the current version of ECE-Tools, follow these steps to [upgrade](https://devdocs.magento.com/guides/v2.2/cloud/project/ece-tools-update.html) in our developer documentation.
1.  After you have upgraded ECE-Tools, check if you now have a current version of the [Fastly plugin](https://github.com/fastly/fastly-magento2/tree/master/etc/vcl_snippets) installed.
1.  If the Fastly plugin is not the current version, follow these steps to [upgrade the plugin to the most current version](https://devdocs.magento.com/guides/v2.3/cloud/cdn/configure-fastly.html#upgrade "Follow link") in our developer documentation.

## Related reading


* For information about setting up and configuring Fastly, see [Configure Fastly services](https://devdocs.magento.com/guides/v2.3/cloud/cdn/cloud-fastly.html) in our developer documentation.
* For general information about Fastly, see [fastly.com](https://www.fastly.com/).