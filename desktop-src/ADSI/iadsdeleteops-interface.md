---
title: Интерфейс Иадсделетеопс
description: Интерфейс Иадсделетеопс используется в подпрограммых супервизора и обслуживания для базового хранилища каталога. Он может удалять конечные объекты и целые поддеревья в одной операции.
ms.assetid: 821b71c2-e9f5-4ca8-9366-e8a3f1907670
ms.tgt_platform: multiple
keywords:
- Интерфейс ADSI интерфейса Иадсделетеопс
- Иадсделетеопс ADSI, использование
- ADSI ADSI, пример кода C/C++, использование Иадсделетеопс для удаления целых групп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6332dd28e903996e8688d6c6fc672df080822595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654129"
---
# <a name="iadsdeleteops-interface"></a>Интерфейс Иадсделетеопс

Интерфейс [**иадсделетеопс**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) используется в подпрограммых супервизора и обслуживания для базового хранилища каталога. Он может удалять конечные объекты и целые поддеревья в одной операции.

Если этот интерфейс не поддерживался, удаление объекта из Active Directory потребует рекурсивного перечисления и удаления каждого автономного объекта. При использовании этого интерфейса любой объект контейнера со всеми содержащимися в нем объектами и подобъектам можно удалить с помощью одной операции.

В следующем примере кода удаляется контейнер "ENG" и все дочерние объекты.


```C++
HRESULT hr;
IADsDeleteOps *pDeleteOps;
LPWSTR pwszUsername = NULL;
LPWSTR pwszPassword = NULL;

// Insert code to securely retrieve the pwszUsername and pwszPassword
// or leave as NULL to use the default security context of the 
// calling application.
 
// Bind to the LDAP provider.
hr = ADsOpenObject(L"LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com", 
    pwszUsername,
    pwszPassword,
    0,
    ADS_SECURE_AUTHENTICATION,
    IID_IADsDeleteOps, 
    (void**)&pDeleteOps);
if(S_OK == hr)
{
    // Delete the container and all child objects.
    pDeleteOps->DeleteObject(0);

    // Release the interface.
    pDeleteOps->Release();
}

if(pwszUsername)
{
    SecureZeroMemory(pwszUsername, lstrlen(pwszUsername) * sizeof(TCHAR));
}
if(pwszPassword)
{
    SecureZeroMemory(pwszPassword, lstrlen(pwszPassword) * sizeof(TCHAR));
}
```



В следующем примере кода удаляется контейнер "ENG" и все дочерние объекты.


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 




