---
title: Install mssqlctl for managing SQL 2019 big data clusters | Microsoft Docs
description: Learn how to install the mssqlctl tool for installing and managing SQL Server 2019 big data clusters (preview).
author: rothja 
ms.author: jroth 
manager: craigg
ms.date: 12/04/2018
ms.topic: conceptual
ms.prod: sql
---

# Install mssqlctl to manage SQL Server 2019 big data clusters

This article describes how to install the **mssqlctl** tool on Windows or Linux.

**mssqlctl** is a command-line utility written in Python that enables cluster administrators to bootstrap and manage the big data cluster via REST APIs. The minimum Python version required is v3.5. You must also have `pip` that is used to download and install **mssqlctl** tool. The instructions below provide examples for Windows and Ubuntu. For installing Python on other platforms, see the [Python documentation](https://wiki.python.org/moin/BeginnersGuide/Download).

> [!IMPORTANT]
> If you installed a previous version of **mssqlctl**, you must delete the cluster *before* upgrading **mssqlctl** and installing the new release. For more information, see [Upgrading to a new release](deployment-guidance.md#upgrade).

## <a id="windows"></a> Windows mssqlctl installation

1. On a Windows client, download the necessary Python package from [https://www.python.org/downloads/](https://www.python.org/downloads/). For python3.5.3 and later, pip3 is also installed when you install Python. 

   > [!TIP] 
   > When installing Python3, select to add Python to your path. If you do not, you can later find where pip3 is located and manually add it to your path.

1. Install **mssqlctl** with the following command:

   ```bash
   pip3 install --extra-index-url https://private-repo.microsoft.com/python/ctp-2.2 mssqlctl
   ```

## <a id="linux"></a> Linux mssqlctl installation

On Linux, you must install Python 3.5 and then upgrade pip. The following example shows the commands that would work for Ubuntu. For other Linux platforms, see the [Python documentation](https://wiki.python.org/moin/BeginnersGuide/Download).

1. Install the necessary Python packages:

   ```bash
   sudo apt-get update && /
   sudo apt-get install -y python3 && /
   sudo apt-get install -y python3-pip && /
   sudo -H pip3 install --upgrade pip
   ```

1. Install **mssqlctl** with the following command:

   ```bash
   pip3 install --extra-index-url https://private-repo.microsoft.com/python/ctp-2.2 mssqlctl
   ```

## Next steps

For more information about big data clusters, see [What are SQL Server 2019 big data clusters?](big-data-cluster-overview.md).
