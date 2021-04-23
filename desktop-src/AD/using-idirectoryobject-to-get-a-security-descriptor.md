---
title: Использование Идиректорйобжект для получения дескриптора безопасности
description: Этот раздел содержит пример кода, используемый для получения дескриптора безопасности.
ms.assetid: 989abd3f-9043-4c3f-a99a-63fa95daf203
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory с помощью Идиректорйобжект для получения дескриптора безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 562438d37d6bfadadfee95d13f80cb4c4728e0f2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789444"
---
# <a name="using-idirectoryobject-to-get-a-security-descriptor"></a><span data-ttu-id="5b19e-104">Использование Идиректорйобжект для получения дескриптора безопасности</span><span class="sxs-lookup"><span data-stu-id="5b19e-104">Using IDirectoryObject to Get a Security Descriptor</span></span>

<span data-ttu-id="5b19e-105">Этот раздел содержит пример кода, используемый для получения дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="5b19e-105">This topic includes a code example used to get a security descriptor.</span></span>

<span data-ttu-id="5b19e-106">Следующий пример кода C++:</span><span class="sxs-lookup"><span data-stu-id="5b19e-106">The following C++ code example:</span></span>

-   <span data-ttu-id="5b19e-107">Создает буфер.</span><span class="sxs-lookup"><span data-stu-id="5b19e-107">Creates a buffer.</span></span>
-   <span data-ttu-id="5b19e-108">Использует интерфейс [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) для получения дескриптора безопасности указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="5b19e-108">Uses the [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) interface to get the security descriptor of the specified object.</span></span>
-   <span data-ttu-id="5b19e-109">Копирует дескриптор безопасности в буфер.</span><span class="sxs-lookup"><span data-stu-id="5b19e-109">Copies the security descriptor to the buffer.</span></span>
-   <span data-ttu-id="5b19e-110">Возвращает указатель на структуру [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , содержащую данные дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="5b19e-110">Returns a pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains the security descriptor data.</span></span>


```C++
HRESULT GetSDFromIDirectoryObject(
    IDirectoryObject *pObject,
    PSECURITY_DESCRIPTOR *pSecurityDescriptor)
{
    HRESULT hr = E_FAIL;
    PADS_ATTR_INFO pAttrInfo;
    DWORD dwReturn= 0;
    LPWSTR pAttrName= L"nTSecurityDescriptor";
    PSECURITY_DESCRIPTOR pSD = NULL;

    if(!pObject || !pSecurityDescriptor)
    {
        return E_INVALIDARG;
    }
 
    // Get the nTSecurityDescriptor.
    hr = pObject->GetObjectAttributes( &pAttrName, 
                                       1, 
                                       &pAttrInfo, 
                                       &dwReturn );
    if((FAILED(hr)) || (dwReturn != 1)) 
    {
        wprintf(L" failed: 0x%x\n", hr);
        return hr;
    }
 
    // Check the attribute name and type.
    if((_wcsicmp(pAttrInfo->pszAttrName,L"nTSecurityDescriptor") == 0) &&
     (pAttrInfo->dwADsType==ADSTYPE_NT_SECURITY_DESCRIPTOR))
    {
        // Get a pointer to the security descriptor.
        pSD = (PSECURITY_DESCRIPTOR)(pAttrInfo->pADsValues->SecurityDescriptor.lpValue);
               
        DWORD SDSize = pAttrInfo->pADsValues->SecurityDescriptor.dwLength;
               
        // Allocate memory for the buffer and copy the security descriptor to the buffer.
        *pSecurityDescriptor = (PSECURITY_DESCRIPTOR)CoTaskMemAlloc(SDSize);
        if (*pSecurityDescriptor)
        {
            CopyMemory((PVOID)*pSecurityDescriptor, (PVOID)pSD, SDSize);
        }
        else
        {
            hr = E_FAIL;
        }

        // Caller must free the memory for pSecurityDescriptor using CoTaskMemFree.
    }
 
    // Free memory used for the attributes retrieved.
    FreeADsMem(pAttrInfo); 
 
    return hr;
}
```



 

 