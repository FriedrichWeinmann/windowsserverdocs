---
title: Using the get-AllNamespaces Command
ms.custom: na
ms.prod: windows-server-2012
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e8fe896d-a69a-4180-923b-9f18185f5941
---
# Using the get-AllNamespaces Command
Displays information about all namespaces on a server.

## Syntax
Windows Server 2008:

```
WDSUTIL /Get-AllNamespaces [/Server:<Server name>] [/ContentProvider:<name>] [/Show:Clients] [/ExcludeDeletePending]
```

Windows Server 2008 R2:

```
WDSUTIL /Get-AllNamespaces [/Server:<Server name>] [/ContentProvider:<name>] [/Details:Clients] [/ExcludeDeletePending]
```

## Parameters

|Parameter|Windows Server 2008|Windows Server 2008 R2|
|-------------|-----------------------|--------------------------|
|\[\/Server:<Server name>\]|Specifies the name of the server. This can be either the NetBIOS name or the fully qualified domain name \(FQDN\). If no server name is specified, the local server will be used.||
|\[\/ContentProvider:<name>\]|Displays the namespaces for the specified content provider only.||
|\[\/Show:Clients\]|Only supported for Windows Server 2008. Displays information about client computers that are connected to the namespace.||
|\[\/Details:Clients\]|Only supported for Windows Server 2008 R2. Displays information about client computers that are connected to the namespace.||
|\[\/ExcludeDeletePending\]|Excludes any deactivated transmissions from the list.||

## <a name="BKMK_examples"></a>Examples
To view all namespaces, type:

```
WDSUTIL /Get-AllNamespaces
```

To view all namespaces except those that are deactivated, type:

-   Windows Server 2008

    ```
    WDSUTIL /Get-AllNamespaces /Server:MyWDSServer /ContentProvider:"MyContentProv" /Show:Clients /ExcludeDeletePending
    ```

-   Windows Server 2008 R2

    ```
    WDSUTIL /Get-AllNamespaces /Server:MyWDSServer /ContentProvider:"MyContentProv" /Details:Clients /ExcludeDeletePending
    ```

#### Additional references
[Command-Line Syntax Key](../../Command-Line-Syntax-Key.md)

[Using the new-Namespace Command](../using-the-new-command/Using-the-new-Namespace-Command.md)

[Using the remove-Namespace Command](../using-the-remove-command/Using-the-remove-Namespace-Command.md)

[Subcommand: start-Namespace](../the-start-server-command/Subcommand--start-Namespace.md)

