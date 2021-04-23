---
title: Получение имени домена Account-Style группы
description: Пользователи, группы, компьютеры и другие субъекты безопасности могут быть представлены в форме учетной записи домена.
ms.assetid: 85627d2d-2845-4998-9957-ce0c8b6473bd
ms.tgt_platform: multiple
keywords:
- группы AD, получение имени группы в стиле учетной записи домена
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8758e61072b862f7c4cd1581b8d54dafb38915be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887671"
---
# <a name="getting-the-domain-account-style-name-of-a-group"></a><span data-ttu-id="7c771-104">Получение имени домена Account-Style группы</span><span class="sxs-lookup"><span data-stu-id="7c771-104">Getting the Domain Account-Style Name of a Group</span></span>

<span data-ttu-id="7c771-105">Пользователи, группы, компьютеры и другие субъекты безопасности могут быть представлены в форме учетной записи домена.</span><span class="sxs-lookup"><span data-stu-id="7c771-105">Users, groups, computers, and other security principals can be represented in domain account form.</span></span> <span data-ttu-id="7c771-106">Учетная запись домена (имя входа, используемое в более ранних версиях Windows NT) имеет следующую форму:</span><span class="sxs-lookup"><span data-stu-id="7c771-106">Domain account (the logon name used in earlier versions of Windows NT) has the following form:</span></span>


```C++
<domain>\<account>
```



<span data-ttu-id="7c771-107">Где " <domain> " — имя домена Windows NT, содержащего пользователя, а " <account> " — свойство **SamAccountName** указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="7c771-107">Where "<domain>" is the name of the Windows NT domain that contains the user and "<account>" is the **samAccountName** property of the specified user.</span></span> <span data-ttu-id="7c771-108">Например: "Fabrikam \\ жеффсмис".</span><span class="sxs-lookup"><span data-stu-id="7c771-108">For example: "Fabrikam\\jeffsmith".</span></span>

<span data-ttu-id="7c771-109">В форме учетной записи домена можно указать доверенное лицо в элементе управления доступом в дескрипторе безопасности.</span><span class="sxs-lookup"><span data-stu-id="7c771-109">The domain account form can specify the trustee in an ACE in a security descriptor.</span></span> <span data-ttu-id="7c771-110">Он также используется для имени входа на компьютерах под управлением Windows версии NT 4,0 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="7c771-110">It is also used for the logon name on computers running Windows version NT 4.0 and earlier.</span></span>


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



 

 




