---
title: Чтение объектов attributeSchema и classSchema
description: В этом разделе приведены примеры кода и рекомендации для чтения непосредственно из объектов attributeSchema и classSchema в контейнере схемы.
ms.assetid: a60558e1-88a1-493c-9340-a90143b11f60
ms.tgt_platform: multiple
keywords:
- Чтение объектов attributeSchema и classSchema Active Directory
- объекты Active Directory, чтение объектов attributeSchema и classSchema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910d387809f7be8af22d494974021e5e6a47d0ab
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104133667"
---
# <a name="reading-attributeschema-and-classschema-objects"></a>Чтение объектов attributeSchema и classSchema

В этом разделе приведены примеры кода и рекомендации для чтения непосредственно из объектов **attributeSchema** и **classSchema** в контейнере схемы. Имейте в виду, что в большинстве случаев, когда необходимо прочитать данные об определении класса или атрибута, более эффективно считывать данные из абстрактной схемы, как описано в разделе [Чтение абстрактной схемы](reading-the-abstract-schema.md).

Интерфейсы и методы, используемые для чтения из контейнера схемы, используются для чтения любого объекта в службах домен Active Directory. Ниже приведены рекомендации.

-   Чтобы выполнить привязку к контейнеру схемы, получите его различающееся имя, которое можно получить путем привязки к rootDSE и считывания свойства **счеманамингконтекст** , как описано в разделе [Привязка бессерверных и RootDSE](serverless-binding-and-rootdse.md).
-   Используйте указатель [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) для контейнера схемы, чтобы перечислить объекты **attributeSchema** и **classSchema** .
-   Используйте интерфейс [**iAds**](/windows/desktop/api/iads/nn-iads-iads) или [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) для получения свойств объекта **attributeSchema** и **classSchema** .
-   Используйте функции [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) или [**адсжетобжект**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) для непосредственной привязки к объекту **attributeSchema** или **classSchema** .
-   При чтении нескольких объектов **attributeSchema** или **classSchema** производительность можно повысить путем привязки к указателю [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) в контейнере схемы и использования метода [**иадсконтаинер. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) для привязки к отдельным объектам класса и атрибута. Это более эффективно, чем повторные вызовы [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) или [**адсжетобжект**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) для привязки к отдельным объектам класса и атрибута. Используйте атрибут **CN** для создания относительного пути для вызова **иадсконтаинер. GetObject** (например, "CN = User" для объекта **classSchema** класса User).
-   Используйте указатель [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) для контейнера схемы, чтобы запросить схему для атрибутов или классов, соответствующих фильтру поиска.

Пример кода, демонстрирующий различные методы поиска объектов схемы, см. в разделе [пример кода для поиска объектов схемы](example-code-for-searching-for-schema-objects.md).

Следующий пример кода C++ привязывается к указателю [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) в контейнере схемы, а затем использует функции [**адсбуилденумератор**](/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator) и [**адсенумератенекст**](/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext) для перечисления содержимого. Имейте в виду, что перечисление включает все объекты **attributeSchema** и **classSchema** , а также один объект **подсхемы** , который является абстрактной схемой.

Для каждого перечислимого объекта в примере кода используется свойство [**iAds. class**](/windows/desktop/ADSI/iads-property-methods) , чтобы определить, является ли он объектом **attributeSchema** или **classSchema** . В примере кода показано, как считывать свойства, недоступные из абстрактной схемы.


```C++
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <windows.h>
#include <stdio.h>
#include <ole2.h>
#include <activeds.h>
#include <atlbase.h>

//  Forward declarations.
void ProcessAttribute(IADs *pChild);
void ProcessClass(IADs *pChild);

//  Entry point for the application.
int wmain(int argc, WCHAR* argv[])
{
    HRESULT hr;

    hr = CoInitialize(NULL);
    if(SUCCEEDED(hr))
    {
        CComBSTR sbstrDSPath;
        CComVariant svar;
        IADs *pRootDSE = NULL;
        IADsContainer *pSchema = NULL;  
        IEnumVARIANT *pEnum = NULL;
        ULONG lFetch;
        CComBSTR sbstrClass; 
        DWORD dwClasses = 0, dwAttributes = 0, dwUnknownClass = 0;

        //  Bind to rootDSE to get the schemaNamingContext property.
        hr = ADsGetObject(L"LDAP://rootDSE", IID_IADs, (void**)&pRootDSE);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsGetObject failed: 0x%x\n", hr);
            goto cleanup;
        }

        hr = pRootDSE->Get(CComBSTR("schemaNamingContext"), &svar);
        sbstrDSPath = "LDAP://";
        sbstrDSPath += svar.bstrVal;

        //  Bind to the actual schema container.
        wprintf(L"Binding to %s\n", sbstrDSPath);
        hr = ADsGetObject(sbstrDSPath, IID_IADsContainer, (void**) &pSchema);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsGetObject to schema failed: 0x%x\n", hr);
            goto cleanup;
        }

        //  Enumerate the attribute and class objects in the schema container.
        hr = ADsBuildEnumerator(pSchema, &pEnum);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsBuildEnumerator failed: 0x%x\n", hr);
            goto cleanup;
        }

        hr = ADsEnumerateNext(pEnum, 1, &svar, &lFetch);
        while(S_OK == hr && 1 == lFetch)
        {
            IADs *pChild = NULL;

            //  Get an IADs pointer on the child object.
            hr = V_DISPATCH(&svar)->QueryInterface(IID_IADs, (void**) &pChild);
            if (SUCCEEDED(hr)) 
            {
                //  Verify that this is a class, attribute, or subSchema object.
                hr = pChild->get_Class(&sbstrClass);
                if (SUCCEEDED(hr)) 
                {
                    //  Get data. This depends on type of schema element.
                    if (_wcsicmp(L"classSchema", sbstrClass) == 0)
                    {
                        dwClasses++;
                        wprintf(L"%s\n", sbstrClass);
                        ProcessClass(pChild);
                        wprintf(L"\n");
                    }
                    else if (_wcsicmp(L"attributeSchema", sbstrClass) == 0)
                    {
                        dwAttributes++;
                        wprintf(L"%s\n", sbstrClass);
                        ProcessAttribute(pChild);
                        wprintf(L"\n");
                    }
                    else if (_wcsicmp(L"subSchema", sbstrClass) == 0) 
                    {
                        wprintf(L"abstract schema");
                        wprintf(L"\n");
                    }
                    else
                    {
                        dwUnknownClass++;
                    }
                }

                pChild->Release();
            }

            hr = ADsEnumerateNext(pEnum, 1, &svar, &lFetch);
        }

        wprintf(L"Classes: %u\nAttributes: %u\nUnknown: %u\n", dwClasses, dwAttributes, dwUnknownClass);

cleanup:
        if (pRootDSE)
        {
            pRootDSE->Release();
        }

        if (pEnum)
        {
            ADsFreeEnumerator(pEnum);
        }

        if (pSchema)
        {
            pSchema->Release();
        }

    }    

    CoUninitialize();

    return 0;
}


//  PrintGUIDFromVariant
//  Prints a GUID in string format.
void PrintGUIDFromVariant(VARIANT varGUID)
{
    HRESULT hr;
    void HUGEP *pArray;
    WCHAR szGUID[40];
    LPGUID pGUID;

    DWORD dwLen = sizeof(GUID);

    hr = SafeArrayAccessData(V_ARRAY(&varGUID), &pArray);
    if(SUCCEEDED(hr))
    {
        pGUID = (LPGUID)pArray;

        //  Convert GUID to string.
        StringFromGUID2(*pGUID, szGUID, 40); 

        //  Print GUID.
        wprintf(L",%s",szGUID);

        SafeArrayUnaccessData(V_ARRAY(&varGUID));
    }
}


// PrintADSPropertyValue
void PrintADSPropertyValue(VARIANT var, BSTR bstrPropName, HRESULT hr) 
{
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if (FAILED(hr))
    {
        wprintf(L"get %s failed: 0x%x\n", bstrPropName, hr);
    }
    else 
    {
        switch (var.vt) 
        {
        case VT_BSTR:
            wprintf(L"%s\n", var.bstrVal);
            break;

        case VT_I4:
            wprintf(L"%u\n", var.iVal);
            break;

        case VT_BOOL:
            wprintf(L"%s\n", var.boolVal ? L"TRUE" : L"FALSE");
            break;

        default:
            wprintf(L"-- ??? --\n");
        }
    }
}

//  ProcessAttribute
//  Gets information about an attributeClass object.
void ProcessAttribute(IADs *pChild)
{
    HRESULT hr;
    CComVariant svar;
    CComBSTR sbstrPropName;

    //  Get the attribute Common-Name (cn) property. 
    sbstrPropName = "cn";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute lDAPDisplayName.
    sbstrPropName = "lDAPDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class linkID. 
    sbstrPropName = "linkID";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute schemaIDGUID. 
    sbstrPropName = "schemaIDGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if(SUCCEEDED(hr))
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the attribute attributeSecurityGUID. 
    sbstrPropName = "attributeSecurityGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if (SUCCEEDED(hr))
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the attribute attributeSyntax property. 
    sbstrPropName = "attributeSyntax";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute's oMSyntax property. 
    sbstrPropName = "oMSyntax";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);
}


//  ProcessClass
//  Gets information about a schema class.
void ProcessClass(IADs *pChild)
{
    HRESULT hr;
    CComVariant svar;
    CComBSTR sbstrPropName;

    //  Get the class cn.
    sbstrPropName = "cn";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class lDAPDisplayName.
    sbstrPropName = "lDAPDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class schemaIDGUID. 
    sbstrPropName = "schemaIDGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (FAILED(hr))
    {
        wprintf(L",get schemaIDGUID failed: 0x%x", hr);
    }
    else 
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the class adminDescription property. 
    sbstrPropName = "adminDescription";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class adminDisplayName property. 
    sbstrPropName = "adminDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class rDNAttID. 
    sbstrPropName = "rDNAttID";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultHidingValue. 
    sbstrPropName = "defaultHidingValue";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultObjectCategory. 
    sbstrPropName = "defaultObjectCategory";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class systemOnly value.
    sbstrPropName = "systemOnly";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultSecurityDescriptor.
    sbstrPropName = "defaultSecurityDescriptor";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);
}
```



 

 