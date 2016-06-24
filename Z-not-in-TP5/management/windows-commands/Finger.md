---
title: Finger
ms.custom: na
ms.prod: windows-server-2012
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 907ea637-5c6c-4752-84c2-46bbf2a68a33
---
# Finger
Displays information about a user or users on a specified remote computer (typically a computer running UNIX) that is running the Finger service or daemon. The remote computer specifies the format and output of the user information display. Used without parameters, **finger** displays help. For examples of how this command can be used, see [Examples](assetId:///c6d43992-8243-4f0a-8605-3152c8a8fe9a#BKMK_Examples).

## Syntax

```
finger [-l] [<User>] [@<Host>] [...]
```

### Parameters

|Parameter|Description|
|-------------|---------------|
|-l|Displays user information in long list format.|
|<User>|Specifies the user about which you want information. If you omit the *User* parameter, **finger** displays information about all users on the specified computer.|
|@<Host>|Specifies the remote computer running the Finger service where you are looking for user information. You can specify a computer name or IP address.|
|/?|Displays Help at the command prompt.|

## Remarks
Multiple User@Host parameters can be specified.

You must prefix **finger** parameters with a hyphen (-) rather than a slash (/).

This command is available only if the Internet Protocol (TCP/IP) protocol is installed as a component in the properties of a network adapter in Network Connections.

The Windows Server 2003 does not provide a finger service.

## <a name="BKMK_Examples"></a>Examples
To display information for user1 on the computer users.microsoft.com, type:

```
finger user1@users.microsoft.com
```

To display information for all users on the computer users.microsoft.com, type:

```
finger @users.microsoft.com
```

## Additional references

-   [Command-Line Syntax Key](Command-Line-Syntax-Key.md)

