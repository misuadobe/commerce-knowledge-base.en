---
title: During installation, Reflection Exception error
labels: Error,Exception,Troubleshooting,Magento Commerce,Magento Commerce Cloud,Redis,Reflection,cache,how to,installation,Adobe Commerce
description: "This article provides a solution for the Reflection Exception error during installation."
---

# During installation, Reflection Exception error

This article provides a solution for the Reflection Exception error during installation.

## Details {#details}

During the installation, a message similar to the following displays:

```php
[ERROR] exception 'ReflectionException' with message 'Class Magento\Framework\StoreManagerInterface does not exist' in /<path>/lib/internal/Magento/Framework/Code/Reader/ClassReader.php
```

## Solution {#solution}

Clear all directories and files under Adobe Commerce's `var` subdirectory and install the Adobe Commerce software again.

As the [Adobe Commerce file system owner](https://devdocs.magento.com/guides/v2.3/install-gde/prereq/file-sys-perms-over.html) or as a user with `root` privileges, enter the following commands:

```bash
$ cd <your Magento install directory>/var
```

```bash
$ rm -rf var/cache/* di/* generation/* page_cache/*
```

### Redis {#redis}

If you use Redis and still get an error, clear the Redis cache as follows:

```bash
$ redis-cli FLUSHALL
```