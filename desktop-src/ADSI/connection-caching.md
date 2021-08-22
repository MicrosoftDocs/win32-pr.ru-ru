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
ms.openlocfilehash: fa0fbf63d65a6941e986069289db201a237deb9ddc7058f291218c1496d0a40e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429031"
---
# <a name="connection-caching"></a>Кэширование подключения

При подключении к серверу на клиентском компьютере для этого процесса кэшируется маркер подключения, пока соединение не будет закрыто. если один и тот же сервер, порт и учетные данные используются в последующем соединении, а только флаги проверки подлинности bind **\_ FAST \_ bind** или **ads \_ server \_** различаются, ADSI будет повторно использовать существующее соединение. ADSI выполняет кэширование подключения отдельно для каждого процесса.

Чтобы повысить производительность, используйте существующие подключения, когда это возможно.

В следующем примере кода показано, как работает кэширование подключений.


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



 

 




