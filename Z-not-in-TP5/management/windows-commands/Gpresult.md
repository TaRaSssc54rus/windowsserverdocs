---
title: Gpresult
ms.custom: na
ms.prod: windows-server-2012
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dfaa3adf-2c83-486c-86d6-23f93c5c883c
---
# Gpresult
Displays the Resultant Set of Policy (RSoP) information for a remote user and computer.

To use RSoP reporting for remotely targeted computers through the firewall, you must have firewall rules that enable inbound network traffic on the ports as described in the topic, [Remote Resultant Set of Policy (RSoP) Group Policy results: ports that require firewall rules](assetId:///91ce6c1e-98e4-4b9d-9f6c-b73a5faa49dd#BKMK_RemoteRSoP).

For examples of how this command can be used, see [Examples](#BKMK_Examples).

## Syntax

```
gpresult [/s <COMPUTER> [/u <USERNAME> [/p [<PASSWORD>]]]] [/user [<TARGETDOMAIN>\]<TARGETUSER>] [/scope {user | computer}] {/r | /v | /z | [/x | /h] <FILENAME> [/f] | /?}
```

## Parameters

> [!NOTE]
> Except when you use **/?**, you must include an output option, either **/r**, **/v**, **/z**, **/x**, or **/h**.

|Parameter|Description|
|-------------|---------------|
|/s <COMPUTER>|Specifies the name or IP address of a remote computer. Do not use backslashes. The default is the local computer.|
|/u <USERNAME>|Uses the credentials of the specified user to run the command. The default user is the user who is logged on to the computer that issues the command.|
|/p [<PASSWORD>]|Specifies the password of the user account that is provided in the **/u** parameter. If **/p** is omitted, **gpresult** prompts for the password. **/p** cannot be used with **/x** or **/h**.|
|/user [<TARGETDOMAIN>\\]<TARGETUSER>|Specifies the remote user whose RSoP data is to be displayed.|
|/scope {user &#124; computer}|Displays RSoP data for either the user or the computer. If **/scope** is omitted, **gpresult** displays RSoP data for both the user and the computer.|
|[/x &#124; /h] <FILENAME>|Saves the report in either XML (**/x**) or HTML (**/h**) format at the location and with the file name that is specified by the *FILENAME* parameter. Cannot be used with **/u**, **/p**, **/r**, **/v**, or **/z**.|
|/f|Forces **gpresult** to overwrite the file name that is specified in the **/x** or **/h** option.|
|/r|Displays RSoP summary data.|
|/v|Displays verbose policy information. This includes detailed settings that were applied with a precedence of 1.|
|/z|Displays all available information about Group Policy. This includes detailed settings that were applied with a precedence of 1 and higher.|
|/?|Displays Help at the command prompt.|

## Remarks

-   Group Policy is the primary administrative tool for defining and controlling how programs, network resources, and the operating system operate for users and computers in an organization. In an Active Directory environment, Group Policy is applied to users or computers based on their membership in sites, domains, or organizational units.

-   Because you can apply overlapping policy settings to any computer or user, the Group Policy feature generates a resulting set of policy settings when the user logs on. **Gpresult** displays the resulting set of policy settings that were enforced on the computer for the specified user when the user logged on.

-   Because **/v** and **/z** produce lots of information, it is useful to redirect output to a text file (for example, **gpresult/z >policy.txt**).

-   The **gpresult** command is available in  Windows Server 2012 , Windows Server 2008 R2, Windows Server2008, Windows 8, Windows 7, and Windows Vista.

## <a name="BKMK_Examples"></a>Examples
The following example retrieves RSoP data for the remote user **targetusername** of the computer **srvmain**, and displays RSoP data about the user only. The command is run with the credentials of the user **maindom\hiropln**, and **p@ssW23** is entered as the password for that user.

```
gpresult /s srvmain /u maindom\hiropln /p p@ssW23 /user targetusername /scope user /r
```

The following example saves all available information about Group Policy for the remote user **targetusername** of the computer **srvmain** to a file that is named **policy.txt**. No data is included about the computer. The command is run with the credentials of the user **maindom\hiropln**, and **p@ssW23** is entered as the password for that user.

```
gpresult /s srvmain /u maindom\hiropln /p p@ssW23 /user targetusername /z > policy.txt
```

The following example displays RSoP data for the computer **srvmain** and the logged-on user. Data is included about both the user and the computer. The command is run with the credentials of the user **maindom\hiropln**, and **p@ssW23** is entered as the password for that user.

```
gpresult /s srvmain /u maindom\hiropln /p p@ssW23 /r
```

## Additional references

-   [Group Policy TechCenter](http://go.microsoft.com/fwlink/?LinkID=145531)

-   [Remote Resultant Set of Policy (RSoP) Group Policy results: ports that require firewall rules](assetId:///91ce6c1e-98e4-4b9d-9f6c-b73a5faa49dd#BKMK_RemoteRSoP)

-   [Command-Line Syntax Key](Command-Line-Syntax-Key.md)

