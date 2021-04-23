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
ms.openlocfilehash: 62b2062c747e38bc0b3a9b1b793a102006c11512
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487409"
---
# <a name="retrieving-deleted-objects"></a><span data-ttu-id="a016a-106">Получение удаленных объектов</span><span class="sxs-lookup"><span data-stu-id="a016a-106">Retrieving Deleted Objects</span></span>

<span data-ttu-id="a016a-107">Удаленные объекты хранятся в контейнере удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="a016a-107">Deleted objects are stored in the Deleted Objects container.</span></span> <span data-ttu-id="a016a-108">Контейнер удаленные объекты обычно не виден, но контейнер удаленные объекты может быть привязан к члену группы "Администраторы".</span><span class="sxs-lookup"><span data-stu-id="a016a-108">The Deleted Objects container is not normally visible, but the Deleted Objects container can be bound to by a member of the administrators group.</span></span> <span data-ttu-id="a016a-109">Содержимое контейнера удаленные объекты можно перечислить, а атрибуты отдельных удаленных объектов можно получить с помощью интерфейса [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) с параметром поиска **\_ \_ захоронения сеарчпреф** .</span><span class="sxs-lookup"><span data-stu-id="a016a-109">The contents of the Deleted Objects container can be enumerated and individual deleted object attributes can be obtained using the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface with the **ADS\_SEARCHPREF\_TOMBSTONE** search preference.</span></span>

<span data-ttu-id="a016a-110">Контейнер удаленных объектов можно получить, применив привязку к известному идентификатору **GUID \_ deleted \_ Objects \_** , определенному в NTDSAPI. h.</span><span class="sxs-lookup"><span data-stu-id="a016a-110">The Deleted Objects container can be obtained by binding to the well-known GUID **GUID\_DELETED\_OBJECTS\_CONTAINER** defined in Ntdsapi.h.</span></span> <span data-ttu-id="a016a-111">Дополнительные сведения о привязке к известным идентификаторам GUID см. [в разделе Привязка к Well-Known объектам с помощью вкгуид](binding-to-well-known-objects-using-wkguid.md).</span><span class="sxs-lookup"><span data-stu-id="a016a-111">For more information about binding to well-known GUIDs, see [Binding to Well-Known Objects Using WKGUID](binding-to-well-known-objects-using-wkguid.md).</span></span>

<span data-ttu-id="a016a-112">Укажите параметр **\_ быстрой \_ привязки ADS** при привязке к контейнеру удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="a016a-112">Specify the **ADS\_FAST\_BIND** option when binding to the Deleted Objects container.</span></span> <span data-ttu-id="a016a-113">Это означает, что интерфейсы ADSI, используемые для работы с объектом в службах домен Active Directory, таких как [**iAds**](/windows/desktop/api/iads/nn-iads-iads) и [**иадспропертилист**](/windows/desktop/api/iads/nn-iads-iadspropertylist), не могут использоваться в контейнере удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="a016a-113">This means that the ADSI interfaces used to work with an object in Active Directory Domain Services, such as [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), cannot be used on the Deleted Objects container.</span></span> <span data-ttu-id="a016a-114">Дополнительные сведения и пример кода, демонстрирующий способ привязки к контейнеру удаленных объектов, см. в примере функции Жетделетедобжектсконтаинер ниже.</span><span class="sxs-lookup"><span data-stu-id="a016a-114">For more information and a code example that shows how to bind to the Deleted Objects container, see the GetDeletedObjectsContainer example function below.</span></span>

-   [<span data-ttu-id="a016a-115">Перечисление удаленных объектов</span><span class="sxs-lookup"><span data-stu-id="a016a-115">Enumerating Deleted Objects</span></span>](#enumerating-deleted-objects)
-   [<span data-ttu-id="a016a-116">Поиск конкретного удаленного объекта</span><span class="sxs-lookup"><span data-stu-id="a016a-116">Finding a Specific Deleted Object</span></span>](#finding-a-specific-deleted-object)
    -   [<span data-ttu-id="a016a-117">жетделетедобжектсконтаинер</span><span class="sxs-lookup"><span data-stu-id="a016a-117">GetDeletedObjectsContainer</span></span>](#getdeletedobjectscontainer)
    -   [<span data-ttu-id="a016a-118">енумделетедобжектс</span><span class="sxs-lookup"><span data-stu-id="a016a-118">EnumDeletedObjects</span></span>](#enumdeletedobjects)
    -   [<span data-ttu-id="a016a-119">финдделетедобжектбигуид</span><span class="sxs-lookup"><span data-stu-id="a016a-119">FindDeletedObjectByGUID</span></span>](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a><span data-ttu-id="a016a-120">Перечисление удаленных объектов</span><span class="sxs-lookup"><span data-stu-id="a016a-120">Enumerating Deleted Objects</span></span>

<span data-ttu-id="a016a-121">Интерфейс [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) используется для поиска удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="a016a-121">The [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface is used to search for deleted objects.</span></span>

<span data-ttu-id="a016a-122">**Перечисление удаленных объектов**</span><span class="sxs-lookup"><span data-stu-id="a016a-122">**To enumerate deleted objects**</span></span>

1.  <span data-ttu-id="a016a-123">Получите интерфейс [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) для контейнера удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="a016a-123">Obtain the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface for the Deleted Objects container.</span></span> <span data-ttu-id="a016a-124">Это достигается путем привязки к контейнеру удаленных объектов и запроса интерфейса **IDirectorySearch** .</span><span class="sxs-lookup"><span data-stu-id="a016a-124">This is accomplished by binding to the Deleted Objects container and requesting the **IDirectorySearch** interface.</span></span> <span data-ttu-id="a016a-125">Дополнительные сведения и пример кода, демонстрирующий способ привязки к контейнеру удаленных объектов, см. в следующем примере функции **жетделетедобжектсконтаинер** .</span><span class="sxs-lookup"><span data-stu-id="a016a-125">For more information and a code example that shows how to bind to the Deleted Objects container, see the following **GetDeletedObjectsContainer** function example.</span></span>
2.  <span data-ttu-id="a016a-126">Задайте для параметра Поиск в **\_ \_ \_ области поиска ADS сеарчпреф** значение **\_ область ADS \_ одноуровневой** с помощью метода [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="a016a-126">Set the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** search preference to **ADS\_SCOPE\_ONELEVEL** using the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="a016a-127">Можно также использовать настройку **\_ \_ поддерева области объявлений** , но контейнер удаленных объектов имеет только один уровень, поэтому использование **\_ \_ поддерева области объявлений** является избыточным.</span><span class="sxs-lookup"><span data-stu-id="a016a-127">The **ADS\_SCOPE\_SUBTREE** preference can also be used, but the Deleted Objects container is only one level, so using **ADS\_SCOPE\_SUBTREE** is redundant.</span></span>
3.  <span data-ttu-id="a016a-128">Задайте для параметра поиска **\_ сеарчпреф \_ захоронения ADS** **значение true**.</span><span class="sxs-lookup"><span data-stu-id="a016a-128">Set the **ADS\_SEARCHPREF\_TOMBSTONE** search preference to **TRUE**.</span></span> <span data-ttu-id="a016a-129">В результате поиск будет включать удаленные объекты.</span><span class="sxs-lookup"><span data-stu-id="a016a-129">This causes the search to include deleted objects.</span></span>
4.  <span data-ttu-id="a016a-130">Задайте для параметра поиска **ADS \_ сеарчпреф \_ PAGESIZE** значение меньше или равное 1000.</span><span class="sxs-lookup"><span data-stu-id="a016a-130">Set the **ADS\_SEARCHPREF\_PAGESIZE** search preference to a value less than, or equal to, 1000.</span></span> <span data-ttu-id="a016a-131">Это необязательно, но если это не сделано, можно получить не более 1000 удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="a016a-131">This is optional, but if this is not done, no more than 1000 deleted objects can be retrieved.</span></span>
5.  <span data-ttu-id="a016a-132">Задайте фильтр поиска в вызове [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) , вызвав "(IsDeleted =**true**)".</span><span class="sxs-lookup"><span data-stu-id="a016a-132">Set the search filter in the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) call to "(isDeleted=**TRUE**)".</span></span> <span data-ttu-id="a016a-133">В результате Поиск получает только объекты с атрибутом **IsDeleted** , установленным в **значение true**.</span><span class="sxs-lookup"><span data-stu-id="a016a-133">This causes the search to only retrieve objects with the **isDeleted** attribute set to **TRUE**.</span></span>

<span data-ttu-id="a016a-134">Пример кода, в котором показано, как перечислить удаленные объекты, см. в следующем примере функции **енумделетедобжектс** .</span><span class="sxs-lookup"><span data-stu-id="a016a-134">For a code example code that shows how to enumerate deleted objects, see the following **EnumDeletedObjects** function example.</span></span>

<span data-ttu-id="a016a-135">Поиск можно уточнить дальше, добавив к фильтру поиска, как показано в [диалекте LDAP](/windows/desktop/ADSI/ldap-dialect).</span><span class="sxs-lookup"><span data-stu-id="a016a-135">The search can be refined further by adding to the search filter as shown in [LDAP Dialect](/windows/desktop/ADSI/ldap-dialect).</span></span> <span data-ttu-id="a016a-136">Например, чтобы найти все удаленные объекты с именем, начинающимся с "Джефф", фильтр поиска будет иметь значение "(& (IsDeleted =**true**) (CN = Джефф \* ))".</span><span class="sxs-lookup"><span data-stu-id="a016a-136">For example, to search for all of the deleted objects with a name that begins with "Jeff", the search filter would be set to "(&(isDeleted=**TRUE**)(cn=Jeff\*))".</span></span>

<span data-ttu-id="a016a-137">Поскольку удаленные объекты имеют большинство атрибутов, удаляемых при их удалении, невозможно выполнить привязку непосредственно к удаленному объекту.</span><span class="sxs-lookup"><span data-stu-id="a016a-137">Because deleted objects have most of their attributes removed when they are deleted, it is not possible to bind directly to a deleted object.</span></span> <span data-ttu-id="a016a-138">При привязке к удаленному объекту необходимо указать параметр **\_ быстрой \_ привязки ADS** .</span><span class="sxs-lookup"><span data-stu-id="a016a-138">The **ADS\_FAST\_BIND** option must be specified when binding to a deleted object.</span></span> <span data-ttu-id="a016a-139">Это означает, что интерфейсы ADSI, используемые для работы с объектом домен Active Directory Services, например [**iAds**](/windows/desktop/api/iads/nn-iads-iads) и [**иадспропертилист**](/windows/desktop/api/iads/nn-iads-iadspropertylist), не могут использоваться в контейнере удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="a016a-139">This means that the ADSI interfaces used to work with an Active Directory Domain Services object, such as [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), cannot be used on a deleted object container.</span></span>

## <a name="finding-a-specific-deleted-object"></a><span data-ttu-id="a016a-140">Поиск конкретного удаленного объекта</span><span class="sxs-lookup"><span data-stu-id="a016a-140">Finding a Specific Deleted Object</span></span>

<span data-ttu-id="a016a-141">Кроме того, можно найти конкретный удаленный объект.</span><span class="sxs-lookup"><span data-stu-id="a016a-141">It is also possible to find a specific deleted object.</span></span> <span data-ttu-id="a016a-142">Если известен **атрибут objectGUID** объекта, он может использоваться для поиска объекта с этим конкретным **objectGUID**.</span><span class="sxs-lookup"><span data-stu-id="a016a-142">If the **objectGUID** of the object is known, it can be used to search for the object with that specific **objectGUID**.</span></span> <span data-ttu-id="a016a-143">Дополнительные сведения и пример кода, в котором показано, как найти конкретный удаленный объект, см. в разделе **финдделетедобжектбигуид** ниже.</span><span class="sxs-lookup"><span data-stu-id="a016a-143">For more information and a code example that shows how to find a specific deleted object, see **FindDeletedObjectByGUID** below.</span></span>

### <a name="getdeletedobjectscontainer"></a><span data-ttu-id="a016a-144">жетделетедобжектсконтаинер</span><span class="sxs-lookup"><span data-stu-id="a016a-144">GetDeletedObjectsContainer</span></span>

<span data-ttu-id="a016a-145">В следующем примере кода C++ показано, как выполнить привязку к контейнеру удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="a016a-145">The following C++ code example shows how to bind to the Deleted Objects container.</span></span>


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



### <a name="enumdeletedobjects"></a><span data-ttu-id="a016a-146">енумделетедобжектс</span><span class="sxs-lookup"><span data-stu-id="a016a-146">EnumDeletedObjects</span></span>

<span data-ttu-id="a016a-147">В следующем примере кода C++ показано, как перечислить объекты в контейнере удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="a016a-147">The following C++ code example shows how to enumerate the objects in the Deleted Objects container.</span></span>


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



### <a name="finddeletedobjectbyguid"></a><span data-ttu-id="a016a-148">финдделетедобжектбигуид</span><span class="sxs-lookup"><span data-stu-id="a016a-148">FindDeletedObjectByGUID</span></span>

<span data-ttu-id="a016a-149">В следующем примере кода C++ показано, как найти конкретный удаленный объект из свойства **objectGUID** объекта.</span><span class="sxs-lookup"><span data-stu-id="a016a-149">The following C++ code example shows how to find a specific deleted object from the object's **objectGUID** property.</span></span>


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



 

 