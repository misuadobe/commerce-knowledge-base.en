---
title: "MDVA-36170: GraphQL query to category returns not cached data"
labels: 2.3.1,2.3.2,2.3.2-p2,2.3.3,2.3.3-p1,2.3.4,2.3.4-p2,2.3.5-p1,2.3.5-p2,2.3.6,2.3.6-p1,2.4.0,2.4.0-p1,2.4.1,2.4.1-p1,GraphQL,GraphQL queries,QPT 1.0.20,QPT patches,Magento Commerce,Magento Commerce Cloud,caching,category,data,support tools,Adobe Commerce,cloud infrastructure,on-premises
description: "The MDVA-36170 patch fixes the issue where the result of the GraphQL query is not cached. This patch is available when the [Quality Patches Tool (QPT)](https://support.magento.com/hc/en-us/articles/360047139492) 1.0.20 is installed. The patch ID is MDVA-36170. Please note that the issue was fixed in Adobe Commerce 2.4.2."
---

# MDVA-36170: GraphQL query to category returns not cached data

The MDVA-36170 patch fixes the issue where the result of the GraphQL query is not cached. This patch is available when the [Quality Patches Tool (QPT)](https://support.magento.com/hc/en-us/articles/360047139492) 1.0.20 is installed. The patch ID is MDVA-36170. Please note that the issue was fixed in Adobe Commerce 2.4.2.

## Affected products and versions

**The patch is created for Adobe Commerce version:**

Adobe Commerce on cloud infrastructure 2.3.6

**Compatible with Adobe Commerce versions:**

Adobe Commerce (all deployment methods) 2.3.1 - 2.4.1-p1

>[!NOTE]
>
>The patch might become applicable to other versions with new Quality Patches Tool releases. To check if the patch is compatible with your Adobe Commerce version, update the `magento/quality-patches` package to the latest version and check the compatibility on the [QPT landing page](https://devdocs.magento.com/quality-patches/tool.html#patch-grid). Use the patch ID as a search keyword to locate the patch.

## Issue

Fixes the issue where the result of the GraphQL query is not cached.

<u>Steps to reproduce</u>:

The merchant is using the GET method for GraphQL caching but not getting the cached data.

<pre>https://magento_url/graphql?query={ products(filter: {category_id: {eq: "2"}}, pageSize: 2000, currentPage: 1, sort: {position: ASC}) {
items {
  sku
  id
  name
  description {
    html
  }
  url_key
  specifications
  image {
    label
    gallery_url
  }
  __typename
  quantity_in
  small_image {
    gallery_url
    label
  }
  product_price_range {
    maximum_price {
      final_price {
        value
      }
    }
    minimum_price {
      final_price {
        value
      }
    }
  }
  ... on ConfigurableProduct {
    variants{
      attributes{
        code
        label
        value_index
      }
      product{
        sku
        quantity_in
      }
    }
   }
  }
}
}}</pre>

<u>Expected results</u>:

The data is cached.

<u>Actual results</u>:

The data is not cached.

## Apply the patch

To apply individual patches, use the following links depending on your deployment method:

* Adobe Commerce or Magento Open Source on-premises: [Software Update Guide > Apply Patches](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching/mqp.html) in our developer documentation.
* Adobe Commerce on cloud infrastructure: [Upgrades and Patches > Apply Patches](https://devdocs.magento.com/cloud/project/project-patch.html) in our developer documentation.

## Related reading

To learn more about Quality Patches Tool, refer to:

* [Quality Patches Tool released: a new tool to self-serve quality patches](https://support.magento.com/hc/en-us/articles/360047139492) in our support knowledge base.
* [Check if patch is available for your Adobe Commerce issue using Quality Patches Tool](https://support.magento.com/hc/en-us/articles/360047125252) in our support knowledge base.

For info about other patches available in QPT, refer to [Patches available in QPT](https://devdocs.magento.com/quality-patches/tool.html#patch-grid) in our developer documentation.