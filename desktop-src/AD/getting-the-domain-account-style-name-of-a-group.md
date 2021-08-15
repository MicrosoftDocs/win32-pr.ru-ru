---
title: Получение имени домена Account-Style группы
description: Пользователи, группы, компьютеры и другие субъекты безопасности могут быть представлены в форме учетной записи домена.
ms.assetid: 85627d2d-2845-4998-9957-ce0c8b6473bd
ms.tgt_platform: multiple
keywords:
- группы AD, получение имени группы в стиле учетной записи домена
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc1b5a076ab3e63059fb79fa784039a8fb2ffb0b1c6396392140b64fa36e16f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189093"
---
# <a name="getting-the-domain-account-style-name-of-a-group"></a>Получение имени домена Account-Style группы

Пользователи, группы, компьютеры и другие субъекты безопасности могут быть представлены в форме учетной записи домена. учетная запись домена (имя входа, используемое в более ранних версиях Windows NT) имеет следующую форму:


```C++
<domain>\<account>
```



где " <domain> " — имя домена Windows NT, содержащего пользователя, а " <account> " — свойство **samAccountName** указанного пользователя. Например: "Fabrikam \\ жеффсмис".

В форме учетной записи домена можно указать доверенное лицо в элементе управления доступом в дескрипторе безопасности. он также используется для имени входа на компьютерах под управлением Windows версии NT 4,0 и более ранних версий.


```C++
// Need to include the following headers to use DsGetDcName.
// #include <LMCONS.H>
// #include <Dsgetdc.h>
// #include <Lmapibuf.h>
// This function returns the previous version name of the security principal 
// specified by the distinguished name specified by szDN.
// The szDomain parameter should be NULL to use the current domain
// to get the name translation. Otherwise, specify the domain to use as the
// domain name (such as liliput) 
// or in dotted format (such as lilliput.Fabrikam.com).
HRESULT GetDownlevelName(LPOLESTR szDomainName, LPOLESTR szDN, LPOLESTR *ppNameString)
{
HRESULT hr = E_FAIL;
IADsNameTranslate *pNameTr = NULL;
IADs *pObject = NULL;
CComBSTR sbstrInitDomain = "";
 
if ((!szDN)||(!ppNameString))
{
    return hr;
}
 
// Use the current domain if none is specified.
if (!szDomainName)
{
    // Call DsGetDcName to get the name of this computer's domain.
    PDOMAIN_CONTROLLER_INFO DomainControllerInfo = NULL;
    DWORD dReturn = 0L;
    dReturn = DsGetDcName(  NULL,
                NULL,
                NULL,
                NULL,
                DS_DIRECTORY_SERVICE_REQUIRED,
                &DomainControllerInfo
    );
    if (dReturn==NO_ERROR)
    {
        sbstrInitDomain = DomainControllerInfo->DomainName;
        hr = S_OK;
    }
 
    // Free the buffer.
    if (DomainControllerInfo)
        NetApiBufferFree(DomainControllerInfo);
}
else
{
    sbstrInitDomain = szDomainName;
    hr = S_OK;
}
 

if (SUCCEEDED(hr))
{
 
    // Create the COM object for the IADsNameTranslate object.
    hr  = CoCreateInstance( 
                                CLSID_NameTranslate,
                                NULL,
                                CLSCTX_INPROC_SERVER,
                                IID_IADsNameTranslate,
                                (void **)&pNameTr
                          );
    if (SUCCEEDED(hr))
    {
 
        // Initialize for the specified domain.
        hr = pNameTr->Init(ADS_NAME_INITTYPE_DOMAIN, sbstrInitDomain);
        if (SUCCEEDED(hr))
        {
            CComBSTR sbstrNameTr;

            hr = pNameTr->Set(ADS_NAME_TYPE_1779, CComBSTR(szDN));
            hr = pNameTr->Get(ADS_NAME_TYPE_NT4, &sbstrNameTr);
            if (SUCCEEDED(hr))
            {
                *ppNameString = (OLECHAR *)CoTaskMemAlloc (sizeof(OLECHAR)*(sbstrNameTr.Length() + 1));
                if (*ppNameString)
                    wcscpy_s(*ppNameString, sbstrNameTr);
                else
                    hr=E_FAIL;
            }
        }

        pNameTr->Release();
    }
}
 
// Caller must call CoTaskMemFree to free ppNameString.
return hr;
}
```



 

 




