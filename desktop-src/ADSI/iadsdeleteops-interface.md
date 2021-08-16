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
ms.openlocfilehash: 192411e53f54de2a5f73cc043f35cea6787f4b879972b6a69ada4760c175292a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839947"
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



 

 




