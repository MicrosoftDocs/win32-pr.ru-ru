---
title: Пример кода для привязки к контейнеру пользователя
description: Этот раздел содержит пример кода, который будет привязан к контейнеру Users в текущем домене, а также вернуть и Иадсконтаинер интерфейс для контейнера.
ms.assetid: 78524b05-f57a-4816-92eb-e37be74dd245
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, привязка к контейнеру пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db1ccb3d2331c4ccef5bbf28f58fa5c046337c7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069773"
---
# <a name="example-code-for-binding-to-the-users-container"></a>Пример кода для привязки к контейнеру пользователя

Следующий пример кода C++ привязывается к контейнеру Users в текущем домене, а также к интерфейсу Return и [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) для контейнера. Дополнительные сведения о привязке к хорошо известным объектам см. [в разделе Binding to Well-Known Objects using вкгуид](binding-to-well-known-objects-using-wkguid.md).


```C++
//**********************************************************
//
//  GetUsersContainer()
//
//  Binds to the well-known Users container in the current domain 
//  with the current user credentials. GUID_USERS_CONTAINER_W is 
//  defined in NTDSAPI.H.
//
//*******************************************************************

HRESULT GetUsersContainer(IADsContainer **ppContainer)
{
    if(NULL == ppContainer)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppContainer = NULL;

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

            pwszPath = new WCHAR[wcslen(pwszFormat) + 
                           wcslen(GUID_USERS_CONTAINER_W) + 
                           wcslen(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, 
                         pwszFormat, 
                         GUID_USERS_CONTAINER_W,
                         var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IADsContainer,
                                (LPVOID*)ppContainer);

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



 

 