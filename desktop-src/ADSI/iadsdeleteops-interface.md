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
# <a name="iadsdeleteops-interface"></a><span data-ttu-id="699e7-107">Интерфейс Иадсделетеопс</span><span class="sxs-lookup"><span data-stu-id="699e7-107">IADsDeleteOps Interface</span></span>

<span data-ttu-id="699e7-108">Интерфейс [**иадсделетеопс**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) используется в подпрограммых супервизора и обслуживания для базового хранилища каталога.</span><span class="sxs-lookup"><span data-stu-id="699e7-108">The [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) interface is used in supervisory and maintenance routines for the underlying directory store.</span></span> <span data-ttu-id="699e7-109">Он может удалять конечные объекты и целые поддеревья в одной операции.</span><span class="sxs-lookup"><span data-stu-id="699e7-109">It can delete leaf objects and entire subtrees in a single operation.</span></span>

<span data-ttu-id="699e7-110">Если этот интерфейс не поддерживался, удаление объекта из Active Directory потребует рекурсивного перечисления и удаления каждого автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="699e7-110">If this interface were not supported, deleting an object from Active Directory would require that each contained object be recursively enumerated and deleted.</span></span> <span data-ttu-id="699e7-111">При использовании этого интерфейса любой объект контейнера со всеми содержащимися в нем объектами и подобъектам можно удалить с помощью одной операции.</span><span class="sxs-lookup"><span data-stu-id="699e7-111">With this interface, any container object, with all its contained objects and subobjects, can be deleted with a single operation.</span></span>

<span data-ttu-id="699e7-112">В следующем примере кода удаляется контейнер "ENG" и все дочерние объекты.</span><span class="sxs-lookup"><span data-stu-id="699e7-112">The following code example deletes the "Eng" container and all child objects.</span></span>


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



<span data-ttu-id="699e7-113">В следующем примере кода удаляется контейнер "ENG" и все дочерние объекты.</span><span class="sxs-lookup"><span data-stu-id="699e7-113">The following code example deletes the "Eng" container and all child objects.</span></span>


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 




