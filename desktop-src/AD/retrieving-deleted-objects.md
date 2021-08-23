---
title: Получение удаленных объектов
description: Удаленные объекты хранятся в контейнере удаленных объектов.
ms.assetid: dc9a6466-204b-4a78-b0f3-9c03c13a374b
ms.tgt_platform: multiple
keywords:
- Извлечение удаленных объектов Active Directory
- объект Active Directory, извлечение удаленных объектов
- Active Directory, использование, извлечение удаленных объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b033a992599fecfc372bf578c1bade54867fd8332c3e114103a69264f736b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025092"
---
# <a name="retrieving-deleted-objects"></a>Получение удаленных объектов

Удаленные объекты хранятся в контейнере удаленных объектов. Контейнер удаленные объекты обычно не виден, но контейнер удаленные объекты может быть привязан к члену группы "Администраторы". Содержимое контейнера удаленные объекты можно перечислить, а атрибуты отдельных удаленных объектов можно получить с помощью интерфейса [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) с параметром поиска **\_ \_ захоронения сеарчпреф** .

Контейнер удаленных объектов можно получить, применив привязку к известному идентификатору **GUID \_ deleted \_ Objects \_** , определенному в NTDSAPI. h. Дополнительные сведения о привязке к известным идентификаторам GUID см. [в разделе Привязка к Well-Known объектам с помощью вкгуид](binding-to-well-known-objects-using-wkguid.md).

укажите параметр **\_ FAST \_ привязки ADS** при привязке к контейнеру удаленных объектов. Это означает, что интерфейсы ADSI, используемые для работы с объектом в службах домен Active Directory, таких как [**iAds**](/windows/desktop/api/iads/nn-iads-iads) и [**иадспропертилист**](/windows/desktop/api/iads/nn-iads-iadspropertylist), не могут использоваться в контейнере удаленных объектов. Дополнительные сведения и пример кода, демонстрирующий способ привязки к контейнеру удаленных объектов, см. в примере функции Жетделетедобжектсконтаинер ниже.

-   [Перечисление удаленных объектов](#enumerating-deleted-objects)
-   [Поиск конкретного удаленного объекта](#finding-a-specific-deleted-object)
    -   [жетделетедобжектсконтаинер](#getdeletedobjectscontainer)
    -   [енумделетедобжектс](#enumdeletedobjects)
    -   [финдделетедобжектбигуид](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a>Перечисление удаленных объектов

Интерфейс [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) используется для поиска удаленных объектов.

**Перечисление удаленных объектов**

1.  Получите интерфейс [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) для контейнера удаленных объектов. Это достигается путем привязки к контейнеру удаленных объектов и запроса интерфейса **IDirectorySearch** . Дополнительные сведения и пример кода, демонстрирующий способ привязки к контейнеру удаленных объектов, см. в следующем примере функции **жетделетедобжектсконтаинер** .
2.  Задайте для параметра Поиск в **\_ \_ \_ области поиска ADS сеарчпреф** значение **\_ область ADS \_ одноуровневой** с помощью метода [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) . Можно также использовать настройку **\_ \_ поддерева области объявлений** , но контейнер удаленных объектов имеет только один уровень, поэтому использование **\_ \_ поддерева области объявлений** является избыточным.
3.  Задайте для параметра поиска **\_ сеарчпреф \_ захоронения ADS** **значение true**. В результате поиск будет включать удаленные объекты.
4.  Задайте для параметра поиска **ADS \_ сеарчпреф \_ PAGESIZE** значение меньше или равное 1000. Это необязательно, но если это не сделано, можно получить не более 1000 удаленных объектов.
5.  Задайте фильтр поиска в вызове [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) , вызвав "(IsDeleted =**true**)". В результате Поиск получает только объекты с атрибутом **IsDeleted** , установленным в **значение true**.

Пример кода, в котором показано, как перечислить удаленные объекты, см. в следующем примере функции **енумделетедобжектс** .

Поиск можно уточнить дальше, добавив к фильтру поиска, как показано в [диалекте LDAP](/windows/desktop/ADSI/ldap-dialect). Например, чтобы найти все удаленные объекты с именем, начинающимся с "Джефф", фильтр поиска будет иметь значение "(& (IsDeleted =**true**) (CN = Джефф \* ))".

Поскольку удаленные объекты имеют большинство атрибутов, удаляемых при их удалении, невозможно выполнить привязку непосредственно к удаленному объекту. при привязке к удаленному объекту необходимо указать параметр **\_ \_ привязки FAST связывания** . Это означает, что интерфейсы ADSI, используемые для работы с объектом домен Active Directory Services, например [**iAds**](/windows/desktop/api/iads/nn-iads-iads) и [**иадспропертилист**](/windows/desktop/api/iads/nn-iads-iadspropertylist), не могут использоваться в контейнере удаленных объектов.

## <a name="finding-a-specific-deleted-object"></a>Поиск конкретного удаленного объекта

Кроме того, можно найти конкретный удаленный объект. Если известен **атрибут objectGUID** объекта, он может использоваться для поиска объекта с этим конкретным **objectGUID**. Дополнительные сведения и пример кода, в котором показано, как найти конкретный удаленный объект, см. в разделе **финдделетедобжектбигуид** ниже.

### <a name="getdeletedobjectscontainer"></a>жетделетедобжектсконтаинер

В следующем примере кода C++ показано, как выполнить привязку к контейнеру удаленных объектов.


```C++
//***************************************************************************
//
//  GetDeletedObjectsContainer()
//
//  Binds to the Deleted Object container.
//
//***************************************************************************

HRESULT GetDeletedObjectsContainer(IADsContainer **ppContainer)
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

            pwszPath = new WCHAR[wcslen(pwszFormat) + wcslen(GUID_DELETED_OBJECTS_CONTAINER_W) + wcslen(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, pwszFormat, GUID_DELETED_OBJECTS_CONTAINER_W, var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_FAST_BIND | ADS_SECURE_AUTHENTICATION,
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



### <a name="enumdeletedobjects"></a>енумделетедобжектс

В следующем примере кода C++ показано, как перечислить объекты в контейнере удаленных объектов.


```C++
//***************************************************************************
//
//  EnumDeletedObjects()
//
//  Enumerates all of the objects in the Deleted Objects container.
//
//***************************************************************************

HRESULT EnumDeletedObjects()
{
    HRESULT hr;
    IADsContainer *pDeletedObjectsCont = NULL;
    IDirectorySearch *pSearch = NULL;

    hr = GetDeletedObjectsContainer(&pDeletedObjectsCont);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    hr = pDeletedObjectsCont->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Only search for direct child objects of the container.
    ADS_SEARCHPREF_INFO rgSearchPrefs[3];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_ONELEVEL;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the page size.
    rgSearchPrefs[2].dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
    rgSearchPrefs[2].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[2].vValue.Integer = 1000;

    // Set the search preference
    hr = pSearch->SetSearchPreference(rgSearchPrefs, ARRAYSIZE(rgSearchPrefs));
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    LPWSTR pszSearch = L"(cn=*)";

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search
    hr = pSearch->ExecuteSearch(    pszSearch,
                                    rgAttributes,
                                    ARRAYSIZE(rgAttributes),
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;
                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pDeletedObjectsCont)
    {
        pDeletedObjectsCont->Release();
    }

    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}

```



### <a name="finddeletedobjectbyguid"></a>финдделетедобжектбигуид

В следующем примере кода C++ показано, как найти конкретный удаленный объект из свойства **objectGUID** объекта.


```C++
HRESULT FindDeletedObjectByGUID(IADs *padsDomain, GUID *pguid)
{
    HRESULT hr;
    IDirectorySearch *pSearch = NULL;
    LPWSTR pwszGuid = NULL;

    hr = padsDomain->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Search the entire tree.
    ADS_SEARCHPREF_INFO rgSearchPrefs[2];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_SUBTREE;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the search preference.
    hr = pSearch->SetSearchPreference(rgSearchPrefs, 2);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    LPWSTR pwszFormat = L"(objectGUID=%s)";

    LPWSTR pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
    if(NULL == pwszSearch)
    {
        goto cleanup;
    }
    
    swprintf_s(pwszSearch, pwszFormat, pwszGuid);
    
    FreeADsMem(pwszGuid);

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search.
    hr = pSearch->ExecuteSearch(    pwszSearch,
                                    rgAttributes,
                                    3,
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data.
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                GUID guid;
                                LPBYTE pb = col.pADsValues[x].OctetString.lpValue;
                                WCHAR wszGUID[MAX_PATH];

                                // Convert the octet string into a GUID.
                                guid.Data1 = *((long*)pb);
                                pb += sizeof(guid.Data1);
                                guid.Data2 = *((short*)pb);
                                pb += sizeof(guid.Data2);
                                guid.Data3 = *((short*)pb);
                                pb += sizeof(guid.Data3);
                                CopyMemory(&guid.Data4, pb, sizeof(guid.Data4));

                                // Convert the GUID into a string.
                                StringFromGUID2(guid, wszGUID, MAX_PATH);
                                wprintf(wszGUID);

                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                                OutputDebugStringW(wszGUID);
                                OutputDebugStringW(L"\n");

                                {
                                    DWORD a;

                                    for(a = 0, *wszGUID = 0; a < col.pADsValues[x].OctetString.dwLength; a++)
                                    {
                                        swprintf_s(wszGUID + lstrlenW(wszGUID), L"%02X", *(LPBYTE)(col.pADsValues[x].OctetString.lpValue + a));
                                    }

                                    OutputDebugStringW(wszGUID);
                                    OutputDebugStringW(L"\n");
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pwszSearch)
    {
        delete pwszSearch;
    }
    
    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}
```



 

 