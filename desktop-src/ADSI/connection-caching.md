---
title: Кэширование подключения
description: При подключении к серверу на клиентском компьютере для этого процесса кэшируется маркер подключения, пока соединение не будет закрыто.
ms.assetid: 927afd35-8703-4234-b6a8-6320a3667532
ms.tgt_platform: multiple
keywords:
- кэширование подключений ADSI
- Кэширование подключения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857d102a52be9c7ccf40f9076892a85d5b3b8683
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067329"
---
# <a name="connection-caching"></a><span data-ttu-id="16e13-105">Кэширование подключения</span><span class="sxs-lookup"><span data-stu-id="16e13-105">Connection Caching</span></span>

<span data-ttu-id="16e13-106">При подключении к серверу на клиентском компьютере для этого процесса кэшируется маркер подключения, пока соединение не будет закрыто.</span><span class="sxs-lookup"><span data-stu-id="16e13-106">When a connection to a server is made, the connection handle is cached on the client computer for that process until that connection is closed.</span></span> <span data-ttu-id="16e13-107">Если один и тот же сервер, порт и учетные данные используются в последующем соединении и только флаги проверки подлинности привязки " **\_ Быстрая \_ Привязка** " или " **\_ \_ Привязка сервера ADS** " различаются, то ADSI будет повторно использовать существующее соединение.</span><span class="sxs-lookup"><span data-stu-id="16e13-107">If the same server, port, and credentials are used in a subsequent connection, and only the **ADS\_FAST\_BIND** or **ADS\_SERVER\_BIND** authentication flags differ, ADSI will reuse the existing connection.</span></span> <span data-ttu-id="16e13-108">ADSI выполняет кэширование подключения отдельно для каждого процесса.</span><span class="sxs-lookup"><span data-stu-id="16e13-108">ADSI performs this connection caching on a per-process basis.</span></span>

<span data-ttu-id="16e13-109">Чтобы повысить производительность, используйте существующие подключения, когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="16e13-109">To increase performance, reuse existing connections when possible.</span></span>

<span data-ttu-id="16e13-110">В следующем примере кода показано, как работает кэширование подключений.</span><span class="sxs-lookup"><span data-stu-id="16e13-110">The following code example shows how connection caching works.</span></span>


```VB
Dim cachedConn As IADs
Dim obj As IADs
Dim cachedName As String
Dim objName As String
 
' Connect to the server and maintain this handle to cache the connection.
Set cachedConn = GetObject("LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com")
 
cachedName = cachedConn.Get("distinguishedName")
Debug.Print (cachedName)
 
' Reuse the connection to MyMachine opened by cachedConn.
' Be aware that this line executes quickly because it is not required
' to transmit over the network again.
Set obj = GetObject("LDAP://MyMachine/CN=Bob,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection.
Set obj = Nothing
 
' Reuse the connection to MyMachine opened by cachedConn again.
Set obj = GetObject("LDAP://MyMachine/CN=Administrator,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection again.
Set obj = Nothing
 
' Release the first connection.
Set cachedConn = Nothing
 
' The connection to MyMachine is closed.
```



 

 




