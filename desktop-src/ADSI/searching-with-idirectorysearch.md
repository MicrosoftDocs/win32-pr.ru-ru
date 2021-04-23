---
title: Поиск с помощью интерфейса IDirectorySearch
description: Интерфейс IDirectorySearch предоставляет высокоуровневые и недорогие интерфейсы для запроса данных каталога или глобального каталога.
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- Поиск с помощью интерфейса ADSI в интерфейсе IDirectorySearch
- Запросы к ADSI, интерфейсы запросов, IDirectorySearch
- ADSI ADSI, пример кода C/C++, поиск в каталоге с помощью IDirectorySearch
- IDirectorySearch ADSI, использование для поиска в каталоге
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2738e163f672fb0000275e2fb9d885442ae6693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103891093"
---
# <a name="searching-with-the-idirectorysearch-interface"></a><span data-ttu-id="b9569-107">Поиск с помощью интерфейса IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b9569-107">Searching with the IDirectorySearch Interface</span></span>

<span data-ttu-id="b9569-108">Интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) предоставляет высокоуровневые и недорогие интерфейсы для запроса данных каталога или глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="b9569-108">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provides a high-level and low-overhead interface for querying data of a directory or a global catalog.</span></span> <span data-ttu-id="b9569-109">COM-интерфейс **IDirectorySearch** может использоваться только с vtable, и поэтому недоступен для сред разработки на основе автоматизации.</span><span class="sxs-lookup"><span data-stu-id="b9569-109">The **IDirectorySearch** COM interface can be used only with a vtable, and thus, is not available to Automation-based development environments.</span></span>

<span data-ttu-id="b9569-110">**Выполнение поиска**</span><span class="sxs-lookup"><span data-stu-id="b9569-110">**To perform a search**</span></span>

1.  <span data-ttu-id="b9569-111">Привязка к объекту в каталоге.</span><span class="sxs-lookup"><span data-stu-id="b9569-111">Bind to an object in the directory.</span></span>
2.  <span data-ttu-id="b9569-112">Вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , чтобы получить указатель [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="b9569-112">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pointer.</span></span>
3.  <span data-ttu-id="b9569-113">Выполните поиск с помощью указателя [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="b9569-113">Run the search using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pointer.</span></span> <span data-ttu-id="b9569-114">Вызовите метод [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) и передайте фильтр поиска, запрошенные имена атрибутов и другие параметры.</span><span class="sxs-lookup"><span data-stu-id="b9569-114">Call the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method, and pass a search filter, the requested attribute names, and other parameters.</span></span>

<span data-ttu-id="b9569-115">Дополнительные сведения о синтаксисе фильтра поиска см. в разделе [синтаксис фильтра поиска](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="b9569-115">For more information about the search filter syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

<span data-ttu-id="b9569-116">Выполнение запроса зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="b9569-116">Query execution is provider-specific.</span></span> <span data-ttu-id="b9569-117">При использовании некоторых поставщиков фактическое выполнение запроса не происходит до вызова [**IDirectorySearch:: жетфирстров**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) или [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .</span><span class="sxs-lookup"><span data-stu-id="b9569-117">With some providers, the actual query execution does not occur until [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) is called.</span></span> <span data-ttu-id="b9569-118">Интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) работает с фильтрами поиска напрямую.</span><span class="sxs-lookup"><span data-stu-id="b9569-118">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface works with search filters directly.</span></span> <span data-ttu-id="b9569-119">Ни диалект SQL, ни диалект LDAP не требуются.</span><span class="sxs-lookup"><span data-stu-id="b9569-119">Neither the SQL dialect nor the LDAP dialect are required.</span></span>

<span data-ttu-id="b9569-120">Интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) предоставляет методы для перечисления результирующего набора по строкам.</span><span class="sxs-lookup"><span data-stu-id="b9569-120">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provides methods to enumerate the result set, row by row.</span></span> <span data-ttu-id="b9569-121">Метод [**IDirectorySearch:: жетфирстров**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) извлекает первую строку, а [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) перемещает вас на следующую строку из текущей строки.</span><span class="sxs-lookup"><span data-stu-id="b9569-121">The [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) method retrieves the first row and [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) moves you to the next row from the current row.</span></span> <span data-ttu-id="b9569-122">Когда вы достигли последней строки, вызов этих методов возвращает \_ код ошибки в ADS \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b9569-122">When you have reached the last row, calling these methods returns the S\_ADS\_NOMORE\_ROWS error code.</span></span> <span data-ttu-id="b9569-123">И наоборот, [**IDirectorySearch:: жетпревиаусров**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) перемещает вас назад на одну строку за раз.</span><span class="sxs-lookup"><span data-stu-id="b9569-123">Conversely, [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) moves you back one row at a time.</span></span> <span data-ttu-id="b9569-124">\_ \_ \_ Возвращаемое значение S ADS не показывает, что достигнута первая строка результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="b9569-124">An S\_ADS\_NOMORE\_ROWS return value indicates that you have reached the first row of the result set.</span></span> <span data-ttu-id="b9569-125">Эти методы работают с результирующим набором, резидентным в память, на клиенте.</span><span class="sxs-lookup"><span data-stu-id="b9569-125">These methods operate on the result set, resident in memory, on the client.</span></span> <span data-ttu-id="b9569-126">Таким образом, при выполнении страничного и асинхронного поиска, а также при отключенном \_ \_ параметре результатов кэширования Обратная прокрутка может привести к непредвиденным последствиям.</span><span class="sxs-lookup"><span data-stu-id="b9569-126">Thus, when paged and asynchronous searches are performed and the \_CACHE\_RESULTS option is turned off, backward scrolling can have unexpected consequences.</span></span>

<span data-ttu-id="b9569-127">После того как вы настроили соответствующую строку, вызовите [**IDirectorySearch:: DataColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) , чтобы получить элементы данных, столбец по столбцу.</span><span class="sxs-lookup"><span data-stu-id="b9569-127">When you have located the appropriate row, call [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) to obtain data items, column by column.</span></span> <span data-ttu-id="b9569-128">Для каждого вызова передается имя интересующего столбца.</span><span class="sxs-lookup"><span data-stu-id="b9569-128">For each call, you pass the name of the column of interest.</span></span> <span data-ttu-id="b9569-129">Возвращаемый элемент данных является указателем на структуру [**\_ \_ столбцов поиска баннеров**](/windows/desktop/api/Iads/ns-iads-ads_search_column) .</span><span class="sxs-lookup"><span data-stu-id="b9569-129">The data item returned is a pointer to an [**ADS\_SEARCH\_COLUMN**](/windows/desktop/api/Iads/ns-iads-ads_search_column) structure.</span></span> <span data-ttu-id="b9569-130">**DataColumn** выделяет эту структуру, но ее необходимо освободить с помощью [**фриколумн**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn).</span><span class="sxs-lookup"><span data-stu-id="b9569-130">**GetColumn** allocates this structure for you, but you must free it using [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn).</span></span> <span data-ttu-id="b9569-131">Вызовите [**клосесеарчхандле**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) для завершения операции поиска.</span><span class="sxs-lookup"><span data-stu-id="b9569-131">Call [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) to complete the search operation.</span></span>

<span data-ttu-id="b9569-132">**Выполнение поиска в каталоге**</span><span class="sxs-lookup"><span data-stu-id="b9569-132">**To perform a directory search**</span></span>

1.  <span data-ttu-id="b9569-133">Привязка к поставщику LDAP.</span><span class="sxs-lookup"><span data-stu-id="b9569-133">Bind to an LDAP provider.</span></span> <span data-ttu-id="b9569-134">Это может быть контроллер домена или поставщик глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="b9569-134">It may be a domain controller or a global catalog provider.</span></span>
2.  <span data-ttu-id="b9569-135">Получение COM-интерфейса [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) с вызовом [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); Эта операция могла быть выполнена на шаге 1 во время начальной привязки.</span><span class="sxs-lookup"><span data-stu-id="b9569-135">Retrieve the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) COM Interface with a call to [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); this operation may have been done in Step 1 during the initial binding.</span></span>

    <span data-ttu-id="b9569-136">При необходимости вызовите [**сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) , чтобы выбрать параметры для обработки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="b9569-136">Optionally, call [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) to select options for handling the results of your search.</span></span>

3.  <span data-ttu-id="b9569-137">Вызовите [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).</span><span class="sxs-lookup"><span data-stu-id="b9569-137">Call [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).</span></span> <span data-ttu-id="b9569-138">В зависимости от параметров, заданных в [**сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) , это может быть, или нет, начать выполнение запроса.</span><span class="sxs-lookup"><span data-stu-id="b9569-138">Depending on the options set in [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) this may, or may not, begin query execution.</span></span>
4.  <span data-ttu-id="b9569-139">Вызовите [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) , чтобы переместить индекс строки (от внутреннего к [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) в первую строку.</span><span class="sxs-lookup"><span data-stu-id="b9569-139">Call [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) to move the row index (internal to [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) to the first row.</span></span>
5.  <span data-ttu-id="b9569-140">Прочтите данные из строки с помощью метода [**DataColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn), а затем вызовите [**фриколумн**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) , чтобы освободить память, выделенную методом **DataColumn**.</span><span class="sxs-lookup"><span data-stu-id="b9569-140">Read the data from the row using [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn), then call [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) to release the memory allocated by **GetColumn**.</span></span>
6.  <span data-ttu-id="b9569-141">Повторяйте шаг 5, пока не будут получены все данные из результата поиска, или пока [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) не вернет \_ строки в ADS \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b9569-141">Repeat Step 5 until all data is retrieved from the search result, or until [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) returns S\_ADS\_NOMORE\_ROWS.</span></span>
7.  <span data-ttu-id="b9569-142">По завершении вызовите [**абандонсеарч**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) и [**клосесеарчхандле**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) .</span><span class="sxs-lookup"><span data-stu-id="b9569-142">Call [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) and [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) when complete.</span></span>

<span data-ttu-id="b9569-143">Этот сценарий показан в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="b9569-143">The following code example shows this scenario.</span></span> <span data-ttu-id="b9569-144">Чтобы начать привязку к ADSI, вызовите функцию [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="b9569-144">To start binding to ADSI, call the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>


```C++
HRESULT hr = S_OK; // COM result variable
ADS_SEARCH_COLUMN col;  // COL for iterations
LPWSTR szUsername = NULL; // user name
LPWSTR szPassword = NULL; // password
 
// Interface Pointers.
IDirectorySearch     *pDSSearch    =NULL;
 
// Initialize COM.
CoInitialize(0);

// Add code to securely retrieve the user name and password or
// leave both as NULL to use the default security context.
 
// Open a connection with server.
hr = ADsOpenObject(L"LDAP://coho.salmon.Fabrikam.com", 
szUsername,
szPassword,
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



<span data-ttu-id="b9569-145">Это предоставляет указатель на интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="b9569-145">This provides a pointer to the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

<span data-ttu-id="b9569-146">Теперь, когда имеется COM-интерфейс для экземпляра Идиректоринтерфаце, вызовите [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).</span><span class="sxs-lookup"><span data-stu-id="b9569-146">Now that there is a COM interface for an IDirectoryInterface instance, call [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).</span></span>

<span data-ttu-id="b9569-147">Создайте массив имен атрибутов, чтобы подготовиться к вызову функции [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="b9569-147">Build an array of attribute names to prepare to call the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) function.</span></span> <span data-ttu-id="b9569-148">Имена атрибутов определяются в схеме Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b9569-148">The attribute names are defined within the schema of Active Directory.</span></span> <span data-ttu-id="b9569-149">Дополнительные сведения об определении схемы см. в разделе [модель схемы ADSI](adsi-schema-model.md).</span><span class="sxs-lookup"><span data-stu-id="b9569-149">For more information about the schema definition, see [ADSI Schema Model](adsi-schema-model.md).</span></span> <span data-ttu-id="b9569-150">Перечисленные имена атрибутов возвращаются, если они поддерживаются объектом в качестве результирующего набора поиска.</span><span class="sxs-lookup"><span data-stu-id="b9569-150">The attribute names listed are returned, if supported by the object, as the result set of the search.</span></span>


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



<span data-ttu-id="b9569-151">Теперь вызовите функцию [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="b9569-151">Now, call the [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) function.</span></span> <span data-ttu-id="b9569-152">Поиск не выполняется до тех пор, пока не будет вызван метод [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .</span><span class="sxs-lookup"><span data-stu-id="b9569-152">The search does not run until you call the [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) method.</span></span>


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



<span data-ttu-id="b9569-153">Вызовите [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) для итерации строк в результате.</span><span class="sxs-lookup"><span data-stu-id="b9569-153">Call [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) to iterate rows in the result.</span></span> <span data-ttu-id="b9569-154">Затем каждая строка запрашивается для атрибута "Description".</span><span class="sxs-lookup"><span data-stu-id="b9569-154">Each row is then queried for the "description" attribute.</span></span> <span data-ttu-id="b9569-155">Если атрибут найден, он отображается.</span><span class="sxs-lookup"><span data-stu-id="b9569-155">If the attribute is found, it is displayed.</span></span>


```C++
LPWSTR pszColumn;
    while( pDSSearch->GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
    {
        // Get the property.
        hr = pDSSearch->GetColumn( hSearch, L"description", &col );
 
        // If this object supports this attribute, display it.
        if ( SUCCEEDED(hr) )
        { 
           if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
              wprintf(L"The description property:%s\r\n", col.pADsValues->CaseIgnoreString); 
           pDSSearch->FreeColumn( &col );
        }
        else
            puts("description property NOT available");
        puts("------------------------------------------------");
        dwCount++;
    }
    pDSSearch->CloseSearchHandle(hSearch);
    pDSSearch->Release();
```



<span data-ttu-id="b9569-156">Чтобы завершить поиск, вызовите метод [**абандонсеарч**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) .</span><span class="sxs-lookup"><span data-stu-id="b9569-156">To end the search, call the [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) method.</span></span>

<span data-ttu-id="b9569-157">Имейте в виду, что если размер страницы не задан, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) блокируется до тех пор, пока не будет возвращен весь результирующий набор клиенту.</span><span class="sxs-lookup"><span data-stu-id="b9569-157">Be aware that if a page size is not set, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) blocks until the entire result set is returned to the client.</span></span> <span data-ttu-id="b9569-158">Если задан размер страницы, то **GetNextRow** блокируется до тех пор, пока не будет возвращена первая страница (размер страницы = количество строк на странице).</span><span class="sxs-lookup"><span data-stu-id="b9569-158">If page size is set, then **GetNextRow** blocks until the first page (page size = number of rows in a page) is returned.</span></span> <span data-ttu-id="b9569-159">Если задан размер страницы и запрос должен быть отсортирован, а поиск по крайней мере одного индексированного атрибута не выполняется, то значение размера страницы игнорируется, а сервер вычисляет весь результирующий набор перед возвратом данных.</span><span class="sxs-lookup"><span data-stu-id="b9569-159">If page size is set and the query is to be sorted and you are not searching on at least one indexed attribute, then the page size value is ignored, and the server calculates the entire result set prior to returning the data.</span></span> <span data-ttu-id="b9569-160">Это влияет на **GetNextRow** блокировку до завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="b9569-160">This has the effect of **GetNextRow** blocking until the query completes.</span></span>

> [!Note]  
> <span data-ttu-id="b9569-161">Чтобы изменить этот запрос в поиске по каталогу на глобальный поиск каталога, вызов [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) изменится.</span><span class="sxs-lookup"><span data-stu-id="b9569-161">To change this query from a directory search to a global catalog search, the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) call is changed.</span></span>

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 