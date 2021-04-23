---
title: Пример кода для привязки к хорошо известным объектам
description: Этот раздел содержит пример кода, который привязывается к хорошо известному объекту с помощью строки привязки ВКГУИД.
ms.assetid: 59345173-5598-4b0a-976c-c5741b785ce1
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, привязка к хорошо известным объектам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f60a1bbf457bab5b6a22a1b4b5470a4f4dbb4c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486617"
---
# <a name="example-code-for-binding-to-well-known-objects"></a><span data-ttu-id="de82f-104">Пример кода для привязки к хорошо известным объектам</span><span class="sxs-lookup"><span data-stu-id="de82f-104">Example Code for Binding to Well Known Objects</span></span>

<span data-ttu-id="de82f-105">В следующем примере кода C++ показано, как выполнить привязку к хорошо известному объекту с помощью строки привязки ВКГУИД.</span><span class="sxs-lookup"><span data-stu-id="de82f-105">The following C++ code example shows how to bind to a well-known object using the WKGUID binding string.</span></span>


```C++
//*********************************************************
//
//  BindToWellKnownObject()
//
//  Binds to one of the well-known objects in the current domain 
//  with the current user credentials. pwszGUID must be one of  
//  the GUID strings defined in NTDSAPI.H, such as 
//  GUID_USERS_CONTAINER_W.
//
//******************************************************************

HRESULT BindToWellKnownObject(LPCWSTR pwszGUID, IADs **ppObject)
{
    if(NULL == ppObject)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppObject = NULL;

    // Bind to the rootDSE object.
    hr = ADsOpenObject(L"LDAP://rootDSE",
                    NULL,
                    NULL,
                    ADS_SECURE_AUTHENTICATION,
                    IID_IADs,
                    (LPVOID*)&pRoot);
    if(SUCCEEDED(hr))
    {
        VARIANT var;
        
        VariantInit(&var);

        // Get the current domain DN.
        hr = pRoot->Get(CComBSTR("defaultNamingContext"), &var);
        if(SUCCEEDED(hr))
        {
            // Build the binding string.
            LPWSTR pwszFormat = L"LDAP://<WKGUID=%s,%s>";
            LPWSTR pwszPath;

            pwszPath = new WCHAR[lstrlenW(pwszFormat) + 
                           lstrlenW(pwszGUID) + 
                           lstrlenW(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, pwszFormat, pwszGUID, var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IADs,
                                (LPVOID*)ppObject);

                delete pwszPath;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }

            VariantClear(&var);        
        }

        pRoot->Release(); 
    }

    return hr;
}
```



 

 




