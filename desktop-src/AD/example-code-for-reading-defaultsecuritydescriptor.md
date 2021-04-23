---
title: Пример кода для чтения Дефаултсекуритидескриптор
description: В следующем примере кода считывается Дефаултсекуритидескриптор для указанного класса объекта.
ms.assetid: 9462686d-654b-40bb-be10-80ca03790ad5
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, чтение Дефаултсекуритидескриптор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7913b6008f1794e36f699f675cf79b5028931c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887679"
---
# <a name="example-code-for-reading-defaultsecuritydescriptor"></a><span data-ttu-id="190f7-104">Пример кода для чтения Дефаултсекуритидескриптор</span><span class="sxs-lookup"><span data-stu-id="190f7-104">Example Code for Reading defaultSecurityDescriptor</span></span>

<span data-ttu-id="190f7-105">В следующем примере кода считывается **дефаултсекуритидескриптор** для указанного класса объекта.</span><span class="sxs-lookup"><span data-stu-id="190f7-105">The following code example reads the **defaultSecurityDescriptor** for a specified object class.</span></span>


```C++
//  Add adsiid.lib to your project
//  Add activeds.lib to your project

#include <stdio.h>
#include "stdafx.h"
#include "iads.h"
#include "adshlp.h"

//  Entry point to the application
int wmain(int argc, WCHAR* argv[])
{
    HRESULT hr;
    IADsContainer *pAbsSchema = NULL;   //  For the abstract schema
    IADsClass *pClass = NULL;           //  For class objects
    IADsProperty *pProp = NULL;         //  For attribute objects
    IADsSyntax *pSyntax = NULL;         //  For syntax objects
    IEnumVARIANT *pEnum = NULL;
    ULONG lFetch;
    VARIANT var;
    VARIANT_BOOL bMulti, bAbstract, bAux;
    BSTR bstrPI, bstrClass, bstrName;
    LONG lCount = 0;
    LONG lVarType = 0;
    IADs *pChild = NULL;
    DWORD dwUnknownClass = 0;

    CoInitialize(NULL);

    //  Bind to the abstract schema.
    hr = ADsGetObject(L"LDAP://schema",
                      IID_IADsContainer,
                      (void**)&pAbsSchema);
    if (FAILED(hr)) 
        goto cleanup;

    //  Enumerate the attribute and class entries in the abstract schema.
    hr = ADsBuildEnumerator(pAbsSchema, &pEnum);
    if (FAILED(hr)) 
        goto cleanup;

    VariantInit(&var);
    hr = ADsEnumerateNext(pEnum, 1, &var, &lFetch);
    while( hr == S_OK && lFetch == 1)
    {
        //  Identify whether this is a class, attribute, or syntax.
        hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, 
                                             (void**) &pChild);
        if (FAILED(hr)) 
            goto cleanuploop;
        hr = pChild->get_Class(&bstrClass);
        if (FAILED(hr)) 
            goto cleanuploop;
        wprintf(L"%s", bstrClass );
        hr = pChild->get_Name(&bstrName);
        if (FAILED(hr)) 
            goto cleanuploop;
        wprintf(L",%s", bstrName);

        //  Retrieve data, depending on the type of schema element.
        if (_wcsicmp(L"Class", bstrClass)==0)
        {
            hr = pChild->QueryInterface(IID_IADsClass, 
                                        (void**) &pClass);
            if (FAILED(hr)) 
                goto cleanuploop;
            pClass->get_Abstract(&bAbstract);
            pClass->get_Auxiliary(&bAux);
            if (bAbstract)
                wprintf(L",Abstract");
            else if (bAux)
                wprintf(L",Auxiliary");
            else 
                wprintf(L",Structural");

            //  Retrieve the primary ADSI 
            //  interface to use with this class.
            pClass->get_PrimaryInterface(&bstrPI);
            if (_wcsicmp(L"{FD8256D0-FD15-11CE-ABC4-02608C9E7553}", 
                bstrPI)==0)
                wprintf(L",IID_IADS,%s", bstrPI);
            if (_wcsicmp(L"{B15160D0-1226-11CF-A985-00AA006BC149}", 
                bstrPI)==0)
                wprintf(L",IID_IADsPrintQueue,%s", bstrPI);
            if (_wcsicmp(L"{A2F733B8-EFFE-11CF-8ABC-00C04FD8D503}", 
                bstrPI)==0)
                wprintf(L",IID_IADsOU,%s", bstrPI);
            if (_wcsicmp(L"{A05E03A2-EFFE-11CF-8ABC-00C04FD8D503}", 
                bstrPI)==0)
                wprintf(L",IID_IADsLocality,%s", bstrPI);
            if (_wcsicmp(L"{3E37E320-17E2-11CF-ABC4-02608C9E7553}", 
                bstrPI)==0)
                wprintf(L",IID_IADsUser,%s", bstrPI);
            if (_wcsicmp(L"{27636B00-410F-11CF-B1FF-02608C9E7553}", 
                bstrPI)==0)
                wprintf(L",IID_IADsGroup,%s", bstrPI);
            if (_wcsicmp(L"{00E4C220-FD16-11CE-ABC4-02608C9E7553}", 
                bstrPI)==0)
                wprintf(L",IID_IADsDomain,%s", bstrPI);
            SysFreeString(bstrPI);
        }
        else if (_wcsicmp(L"Property",bstrClass)==0)
        {
            hr = pChild->QueryInterface(IID_IADsProperty, 
                (void**) &pProp);
            if (FAILED(hr)) 
                goto cleanuploop;
            pProp->get_MultiValued(&bMulti);
            wprintf(L",%s", bMulti ? L"Multi-Valued" : L"Single-Valued");
        }
        else if (_wcsicmp(L"Syntax", bstrClass)==0)
        {
            hr = pChild->QueryInterface(IID_IADsSyntax, 
                (void**) &pSyntax);
            if ( FAILED(hr) ) 
                goto cleanuploop;
            pSyntax->get_OleAutoDataType (&lVarType);
            wprintf(L",%u", lVarType);
        }
        else
            dwUnknownClass++;

cleanuploop:
        wprintf(L"\n");
        SysFreeString(bstrClass);
        SysFreeString(bstrName);
        pChild->Release();
        VariantClear(&var);
        if (SUCCEEDED(hr))
            hr = ADsEnumerateNext( pEnum, 1, &var, &lFetch );
    }

    wprintf(L"dwUnknownClass: %u\n", dwUnknownClass);
cleanup:
    if (pAbsSchema)
        pAbsSchema->Release();
    if (pEnum)
        pEnum->Release();
    VariantClear(&var);
    CoUninitialize();

    return hr;
}
```



 

 




