---
title: Dfsdiag
ms.custom: na
ms.prod: windows-server-2012
ms.reviewer: na
ms.suite: na
ms.technology: 
  - techgroup-storage
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c0891e67-0187-4f18-923d-5623e6127f90
---
# Dfsdiag
The `Dfsdiag` command provides diagnostic information for DFS Namespaces.

## Syntax

```
dfsdiag [ /TestDCs [/Domain:<Domain name>]| /TestSites </Machine:<server name>| /DFSPath:<namespace root or DFS folder> [/Recurse]> [/Full] | /TestDFSConfig /DFSRoot:<namespace> | /TestDFSIntegrity /DFSRoot:<DFS root path> [/Recurse] [/Full] | /TestReferral /DFSPath:<DFS path for getting referrals> [/Full] | /?]

```

### Parameters

|Parameter|Description|
|-------------|---------------|
|[Dfsdiag TestDCs](dfsdiag/Dfsdiag-TestDCs.md)|Checks domain controller configuration.|
|[Dfsdiag TestSites](dfsdiag/Dfsdiag-TestSites.md)|Checks site associations.|
|[Dfsdiag TestDFSConfig](dfsdiag/Dfsdiag-TestDFSConfig.md)|Checks DFS Namespace configuration.|
|[Dfsdiag TestDFSIntegrity](dfsdiag/Dfsdiag-TestDFSIntegrity.md)|Checks DFS Namespace integrity.|
|[Dfsdiag TestReferral](dfsdiag/Dfsdiag-TestReferral.md)|Checks referral responses.|
|/?|Displays help at the command prompt.|

## Additional references

-   [Command-Line Syntax Key](Command-Line-Syntax-Key.md)

