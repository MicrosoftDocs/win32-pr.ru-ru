---
description: LSA предоставляет функции, которые администраторы могут использовать для запроса и установки глобальных сведений о политике для локального компьютера и домена.
ms.assetid: bbe27d16-0a6b-435a-ae80-5e983047b511
title: Управление сведениями о политике
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc76137f41c592370dbeecafd243f11012cb1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664224"
---
# <a name="managing-policy-information"></a><span data-ttu-id="4d674-103">Управление сведениями о политике</span><span class="sxs-lookup"><span data-stu-id="4d674-103">Managing Policy Information</span></span>

<span data-ttu-id="4d674-104">LSA предоставляет функции, которые администраторы могут использовать для запроса и установки глобальных сведений о политике для локального компьютера и домена.</span><span class="sxs-lookup"><span data-stu-id="4d674-104">The LSA provides functions that administrators can use to query and set global policy information for the local computer and the domain.</span></span>

<span data-ttu-id="4d674-105">Прежде чем можно будет управлять сведениями о политике, приложение должно получить обработчик для объекта локальной [**политики**](policy-object.md) , как показано при [открытии обработчика объектов политики](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="4d674-105">Before you can manage policy information, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span> <span data-ttu-id="4d674-106">Этот обработчик необходим для функций, управляющих сведениями о политиках.</span><span class="sxs-lookup"><span data-stu-id="4d674-106">This handle is required by the functions that manage policy information.</span></span>

<span data-ttu-id="4d674-107">Чтобы получить сведения о локальной политике безопасности, вызовите [**лсакуеринформатионполици**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy).</span><span class="sxs-lookup"><span data-stu-id="4d674-107">To retrieve information about the local security policy, call [**LsaQueryInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy).</span></span> <span data-ttu-id="4d674-108">Чтобы задать локальную политику безопасности, вызовите [**лсасетинформатионполици**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy).</span><span class="sxs-lookup"><span data-stu-id="4d674-108">To set local security policy, call [**LsaSetInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy).</span></span> <span data-ttu-id="4d674-109">Описание перечисления [**\_ \_ класс сведений о политике**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class) содержит сведения о типах политик, которые можно запрашивать или задавать.</span><span class="sxs-lookup"><span data-stu-id="4d674-109">The description of the [**POLICY\_INFORMATION\_CLASS**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class) enumeration details the types of policy information that can be queried or set.</span></span>

<span data-ttu-id="4d674-110">В следующем примере показано, как получить сведения о домене учетной записи системы, используя обработчик для объекта [**политики**](policy-object.md) системы.</span><span class="sxs-lookup"><span data-stu-id="4d674-110">The following example demonstrates how to obtain a system's account domain information, given a handle to the system's [**Policy**](policy-object.md) object.</span></span>


```C++
#include <windows.h>

BOOL GetAccountDomainInfo(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult = STATUS_SUCCESS;
  PPOLICY_ACCOUNT_DOMAIN_INFO pPADInfo = NULL;
  PWCHAR name = NULL;
  UINT nameSize;
  
  ntsResult = LsaQueryInformationPolicy(
    PolicyHandle,                   // Open handle to a Policy object.
    PolicyAccountDomainInformation, // The information to get.
    (PVOID *)&pPADInfo              // Storage for the information.
  );

  if (ntsResult == STATUS_SUCCESS)
  {  
    // There is no guarantee that the LSA_UNICODE_STRING buffer
    // is null-terminated, so copy the name to a buffer that is.
    nameSize =  pPADInfo->DomainName.Length + 1 * sizeof(WCHAR);
    name = (WCHAR *) LocalAlloc(LPTR, nameSize);
    if (!name)
    {
        wprintf(L"Failed LocalAlloc\n");
        exit(1);
    }
    wcsncpy_s(name, nameSize, pPADInfo->DomainName.Buffer,
        pPADInfo->DomainName.Length);
    wprintf(L"The account domain name is %ws\n", name);
    LocalFree(name);
    if (STATUS_SUCCESS != LsaFreeMemory(pPADInfo))
        wprintf(L"LsaFreeMemory error\n");
  }
  else
  {
    // Show the corresponding win32 error code.
    wprintf(
        L"Error obtaining account domain information - (win32) %lu\n",
        LsaNtStatusToWinError(ntsResult));
  }

  return !ntsResult;
}

```



 

 
