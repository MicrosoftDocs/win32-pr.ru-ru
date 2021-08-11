---
title: Использование Идиректорйобжект для получения дескриптора безопасности
description: Этот раздел содержит пример кода, используемый для получения дескриптора безопасности.
ms.assetid: 989abd3f-9043-4c3f-a99a-63fa95daf203
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory с помощью Идиректорйобжект для получения дескриптора безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7b2bd256fb9601cc61ff41465763ccc30c39bc68ff79760019dad1f8d510bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182518"
---
# <a name="using-idirectoryobject-to-get-a-security-descriptor"></a>Использование Идиректорйобжект для получения дескриптора безопасности

Этот раздел содержит пример кода, используемый для получения дескриптора безопасности.

Следующий пример кода C++:

-   Создает буфер.
-   Использует интерфейс [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) для получения дескриптора безопасности указанного объекта.
-   Копирует дескриптор безопасности в буфер.
-   Возвращает указатель на структуру [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , содержащую данные дескриптора безопасности.


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



 

 