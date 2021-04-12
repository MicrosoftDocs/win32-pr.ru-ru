---
description: 'Для запроса индекса можно использовать интерфейс Исеарчкуерихелпер. Этот интерфейс реализуется как вспомогательный класс для Исеарчкаталогманажер (и ISearchCatalogManager2) и получается путем вызова Исеарчкаталогманажер:: Жеткуерихелпер.'
ms.assetid: 6e567c09-8763-4866-bf02-ad6651b454db
title: Запрос индекса с помощью Исеарчкуерихелпер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b9d970a1e3f416081d3b7fd3e9d6c2af0a2bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262942"
---
# <a name="querying-the-index-with-isearchqueryhelper"></a><span data-ttu-id="d66b4-104">Запрос индекса с помощью Исеарчкуерихелпер</span><span class="sxs-lookup"><span data-stu-id="d66b4-104">Querying the Index with ISearchQueryHelper</span></span>

<span data-ttu-id="d66b4-105">Для запроса индекса можно использовать интерфейс [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .</span><span class="sxs-lookup"><span data-stu-id="d66b4-105">You can use the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface to query the index.</span></span> <span data-ttu-id="d66b4-106">Этот интерфейс реализуется как вспомогательный класс для [**исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (и [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) и получается путем вызова [**исеарчкаталогманажер:: жеткуерихелпер**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="d66b4-106">This interface is implemented as a helper class to [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (and [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)), and is obtained by calling [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span></span> <span data-ttu-id="d66b4-107">Этот интерфейс позволяет выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="d66b4-107">This interface permits you to:</span></span>

-   <span data-ttu-id="d66b4-108">Получите строку подключения OLE DB для подключения к базе данных Windows Search.</span><span class="sxs-lookup"><span data-stu-id="d66b4-108">Obtain an OLE DB connection string to connect to the Windows Search database.</span></span>
-   <span data-ttu-id="d66b4-109">Преобразуйте запросы пользователей расширенного синтаксиса запросов (АКС) в Windows Search язык SQL (SQL).</span><span class="sxs-lookup"><span data-stu-id="d66b4-109">Convert Advanced Query Syntax (AQS) user queries to Windows Search Structured Query Language (SQL).</span></span>
-   <span data-ttu-id="d66b4-110">Укажите ограничения запросов, которые могут быть выражены в SQL, но не в АКС.</span><span class="sxs-lookup"><span data-stu-id="d66b4-110">Specify query restrictions that can be expressed in SQL, but not in AQS.</span></span>

<span data-ttu-id="d66b4-111">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d66b4-111">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="d66b4-112">начало работы с Исеарчкуерихелпер</span><span class="sxs-lookup"><span data-stu-id="d66b4-112">Getting Started with ISearchQueryHelper</span></span>](#getting-started-with-isearchqueryhelper)
-   [<span data-ttu-id="d66b4-113">Использование метода Женератесклфромусеркуери</span><span class="sxs-lookup"><span data-stu-id="d66b4-113">Using the GenerateSqlFromUserQuery Method</span></span>](#using-the-generatesqlfromuserquery-method)
-   [<span data-ttu-id="d66b4-114">Работа с идентификаторами языковых стандартов</span><span class="sxs-lookup"><span data-stu-id="d66b4-114">Working with Locale Identifiers</span></span>](#working-with-locale-identifiers)
-   [<span data-ttu-id="d66b4-115">Работа со свойствами и столбцами</span><span class="sxs-lookup"><span data-stu-id="d66b4-115">Working with Properties and Columns</span></span>](#working-with-properties-and-columns)
-   [<span data-ttu-id="d66b4-116">Работа с расширением термина запроса</span><span class="sxs-lookup"><span data-stu-id="d66b4-116">Working with Query Term Expansion</span></span>](#working-with-query-term-expansion)
-   [<span data-ttu-id="d66b4-117">Работа с другими методами Исеарчкуерихелпер</span><span class="sxs-lookup"><span data-stu-id="d66b4-117">Working with Other ISearchQueryHelper Methods</span></span>](#working-with-other-isearchqueryhelper-methods)
-   [<span data-ttu-id="d66b4-118">См. также</span><span class="sxs-lookup"><span data-stu-id="d66b4-118">Related topics</span></span>](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a><span data-ttu-id="d66b4-119">начало работы с Исеарчкуерихелпер</span><span class="sxs-lookup"><span data-stu-id="d66b4-119">Getting Started with ISearchQueryHelper</span></span>

<span data-ttu-id="d66b4-120">Существует несколько ключевых интерфейсов и методов, которые следует учитывать перед запуском программных запросов к поиску Windows с помощью интерфейса [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .</span><span class="sxs-lookup"><span data-stu-id="d66b4-120">There are a few key interfaces and methods you should be aware of before you can start programmatically querying Windows Search using the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface.</span></span> <span data-ttu-id="d66b4-121">На высоком уровне необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d66b4-121">At a high level, you need to follow these steps:</span></span>

1.  <span data-ttu-id="d66b4-122">Создайте экземпляр [**исеарчманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .</span><span class="sxs-lookup"><span data-stu-id="d66b4-122">Instantiate an [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) instance.</span></span>
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  <span data-ttu-id="d66b4-123">Получите экземпляр [**исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) с помощью [**Исеарчманажер:: catalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog).</span><span class="sxs-lookup"><span data-stu-id="d66b4-123">Obtain an instance of [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) using [**ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog).</span></span> <span data-ttu-id="d66b4-124">Имя системного каталога для поиска Windows — `SYSTEMINDEX` .</span><span class="sxs-lookup"><span data-stu-id="d66b4-124">The name of the system catalog for Windows Search is `SYSTEMINDEX`.</span></span>
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  <span data-ttu-id="d66b4-125">Получите экземпляр [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) с помощью [**Исеарчкаталогманажер:: жеткуерихелпер**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="d66b4-125">Obtain an instance of [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) using [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span></span>
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  <span data-ttu-id="d66b4-126">После создания экземпляра [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)можно получить строку подключения, используемую для подключения к соединителю поиска Windows OLE DB Connector.</span><span class="sxs-lookup"><span data-stu-id="d66b4-126">After you have an instance of [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), you can then get the connection string used to connect to the Windows Search index OLE DB connector.</span></span>
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a><span data-ttu-id="d66b4-127">Использование метода Женератесклфромусеркуери</span><span class="sxs-lookup"><span data-stu-id="d66b4-127">Using the GenerateSqlFromUserQuery Method</span></span>

<span data-ttu-id="d66b4-128">Метод [**исеарчкуерихелпер:: женератесклфромусеркуери**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) преобразовывает введенные пользователем данные в строку запроса SQL, которую затем можно отправить поставщику OLE DB для поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="d66b4-128">The [**ISearchQueryHelper::GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) method transforms user input into a SQL query string, which can then be submitted to the OLE DB provider for Windows Search.</span></span> <span data-ttu-id="d66b4-129">Этот метод преобразует запрос [синтаксиса расширенных запросов](-search-3x-advancedquerysyntax.md) (АКС) или синтаксиса естественного запроса (НКС), введенный пользователем в SQL, и позволяет добавлять другие фрагменты SQL по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="d66b4-129">This method translates the [Advanced Query Syntax](-search-3x-advancedquerysyntax.md) (AQS) or Natural Query Syntax (NQS) query entered by the user into SQL, and lets you add other SQL fragments as needed.</span></span>

<span data-ttu-id="d66b4-130">Строка SQL-запроса возвращается в следующей форме:</span><span class="sxs-lookup"><span data-stu-id="d66b4-130">The SQL query string is returned in the following form:</span></span>


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



<span data-ttu-id="d66b4-131">Ниже приведен пример строки SQL, возвращаемой из вызова `GenerateSQLFromUserQuery("comput")` .</span><span class="sxs-lookup"><span data-stu-id="d66b4-131">The following is an example of the SQL string returned from the call `GenerateSQLFromUserQuery("comput")`:</span></span>


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> <span data-ttu-id="d66b4-132">Метод создает предикаты FREETEXT и CONTAINS, поскольку содержит только один из них не создает осмысленный ранг.</span><span class="sxs-lookup"><span data-stu-id="d66b4-132">The method generates both the FREETEXT and the CONTAINS predicates because CONTAINS alone does not generate meaningful ranking.</span></span>

 

## <a name="working-with-locale-identifiers"></a><span data-ttu-id="d66b4-133">Работа с идентификаторами языковых стандартов</span><span class="sxs-lookup"><span data-stu-id="d66b4-133">Working with Locale Identifiers</span></span>



| <span data-ttu-id="d66b4-134">Метод</span><span class="sxs-lookup"><span data-stu-id="d66b4-134">Method</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="d66b4-135">Описание</span><span class="sxs-lookup"><span data-stu-id="d66b4-135">Description</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d66b4-136">[**Исеарчкуерихелпер:: Get \_ куериконтентлокале**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/</span><span class="sxs-lookup"><span data-stu-id="d66b4-136">[**ISearchQueryHelper::get\_QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/</span></span><br/> [<span data-ttu-id="d66b4-137">**Исеарчкуерихелпер::p UT \_ куериконтентлокале**</span><span class="sxs-lookup"><span data-stu-id="d66b4-137">**ISearchQueryHelper::put\_QueryContentLocale**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | <span data-ttu-id="d66b4-138">Возвращает или задает код языка (LCID) запроса.</span><span class="sxs-lookup"><span data-stu-id="d66b4-138">Gets/Puts the language code identifier (LCID) of the query.</span></span> <span data-ttu-id="d66b4-139">Это помогает получить правильное средство разбиения на слова и парадигматические модули для сравнения терминов запроса с каталогом или инвертированным индексом.</span><span class="sxs-lookup"><span data-stu-id="d66b4-139">This helps get the correct wordbreaker and stemmer to compare query terms against the catalog/inverted index.</span></span> <span data-ttu-id="d66b4-140">По умолчанию используется текущий языковой стандарт ввода.</span><span class="sxs-lookup"><span data-stu-id="d66b4-140">The default is the current input locale.</span></span> |
| <span data-ttu-id="d66b4-141">[**Исеарчкуерихелпер:: Get \_ куерикэйвордлокале**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/</span><span class="sxs-lookup"><span data-stu-id="d66b4-141">[**ISearchQueryHelper::get\_QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/</span></span><br/> [<span data-ttu-id="d66b4-142">**Исеарчкуерихелпер::p UT \_ куерикэйвордлокале**</span><span class="sxs-lookup"><span data-stu-id="d66b4-142">**ISearchQueryHelper::put\_QueryKeywordLocale**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | <span data-ttu-id="d66b4-143">Возвращает или задает LCID для языка, используемого при синтаксическом анализе ключевых слов синтаксиса расширенных запросов (АКС).</span><span class="sxs-lookup"><span data-stu-id="d66b4-143">Gets/Puts the LCID for the language to use when parsing Advanced Query Syntax (AQS) keywords.</span></span> <span data-ttu-id="d66b4-144">По умолчанию используется языковой стандарт пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d66b4-144">The default is the default user locale.</span></span>                                                                              |



 

<span data-ttu-id="d66b4-145">Языковой стандарт **содержимого** и **ключевое слово locale** являются идентификаторами языкового стандарта (LCID), которые помогают поисковой подсистеме использовать правильные средства разбиения по словам, определяя язык терминов запроса и ключевые слова языка АКС.</span><span class="sxs-lookup"><span data-stu-id="d66b4-145">The **content locale** and **keyword locale** are locale identifiers (LCID) that help the search engine use the correct word breakers by identifying the language of the query terms and the language the AQS keywords.</span></span> <span data-ttu-id="d66b4-146">Они не всегда являются одинаковыми LCID, так как поиск Windows предлагается в нескольких международных версиях, а также включает пакеты многоязыкового интерфейса пользователя (MUI) для других языков.</span><span class="sxs-lookup"><span data-stu-id="d66b4-146">These are not always the same LCIDs because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="d66b4-147">Языковой стандарт содержимого определяет код языка, на котором пользователи выполняют поисковый запрос в, а язык ключевых слов определяет код языка, используемый поисковой системой при анализе ключевых слов синтаксиса расширенных запросов (АКС).</span><span class="sxs-lookup"><span data-stu-id="d66b4-147">The content locale identifies the LCID for the language users input their search query in, while the keyword locale identifies the LCID the search engine uses when parsing Advanced Query Syntax (AQS) keywords.</span></span>

<span data-ttu-id="d66b4-148">Например, при наличии английской версии (без пакетов MUI) языковой стандарт содержимого и ключевое слово keyword имеют значение 1033.</span><span class="sxs-lookup"><span data-stu-id="d66b4-148">For example, if you have the English-US version with no MUI packs, both the content locale and keyword locale are 1033.</span></span> <span data-ttu-id="d66b4-149">Если у вас установлена немецкая версия без пакетов MUI, то языковой стандарт содержимого и ключевое слово locale имеют значение 1031 (GR-GR).</span><span class="sxs-lookup"><span data-stu-id="d66b4-149">If you have the German version with no MUI packs, then both the content locale and keyword locale are 1031 (gr-gr).</span></span> <span data-ttu-id="d66b4-150">Однако если у вас установлена английская версия с пакетом MUI для румынского языка, то язык содержимого — 2072 (ro), а ключевое слово locale — 1033 (EN-US).</span><span class="sxs-lookup"><span data-stu-id="d66b4-150">However, if you have the English version with the Romanian MUI pack, the content locale is 2072 (ro) and the keyword locale is 1033 (en-us).</span></span>

## <a name="working-with-properties-and-columns"></a><span data-ttu-id="d66b4-151">Работа со свойствами и столбцами</span><span class="sxs-lookup"><span data-stu-id="d66b4-151">Working with Properties and Columns</span></span>



| <span data-ttu-id="d66b4-152">Методы</span><span class="sxs-lookup"><span data-stu-id="d66b4-152">Methods</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="d66b4-153">Описание</span><span class="sxs-lookup"><span data-stu-id="d66b4-153">Description</span></span>                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d66b4-154">[**Исеарчкуерихелпер:: Get \_ куериконтентпропертиес**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/</span><span class="sxs-lookup"><span data-stu-id="d66b4-154">[**ISearchQueryHelper::get\_QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/</span></span><br/> [<span data-ttu-id="d66b4-155">**Исеарчкуерихелпер::p UT \_ куериконтентпропертиес**</span><span class="sxs-lookup"><span data-stu-id="d66b4-155">**ISearchQueryHelper::put\_QueryContentProperties**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | <span data-ttu-id="d66b4-156">Возвращает или задает свойства содержимого для поиска (столбец свойств, указанный в предложениях CONTAINS или FREETEXT).</span><span class="sxs-lookup"><span data-stu-id="d66b4-156">Gets/Sets the content properties for the search (property column listed in the CONTAINS or FREETEXT clauses).</span></span>                                   |
| <span data-ttu-id="d66b4-157">[**Исеарчкуерихелпер:: Get \_ куериселектколумнс**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/</span><span class="sxs-lookup"><span data-stu-id="d66b4-157">[**ISearchQueryHelper::get\_QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/</span></span><br/> [<span data-ttu-id="d66b4-158">**Исеарчкуерихелпер::p UT \_ куериселектколумнс**</span><span class="sxs-lookup"><span data-stu-id="d66b4-158">**ISearchQueryHelper::put\_QuerySelectColumns**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | <span data-ttu-id="d66b4-159">Возвращает или задает столбцы (или свойства), запрошенные в инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="d66b4-159">Gets/Sets the columns (or properties) requested in the SELECT statement.</span></span> <span data-ttu-id="d66b4-160">Значение по умолчанию — System. Итемурл и свойства, используемые в предложении WHERE.</span><span class="sxs-lookup"><span data-stu-id="d66b4-160">The default is System.ItemUrl and properties used in the WHERE clause.</span></span> |



 

<span data-ttu-id="d66b4-161">Элементы представлены в хранилище свойств в виде строки.</span><span class="sxs-lookup"><span data-stu-id="d66b4-161">Items are represented in the property store as a row.</span></span> <span data-ttu-id="d66b4-162">Каждая строка содержит ряд столбцов, представляющих свойства этого элемента.</span><span class="sxs-lookup"><span data-stu-id="d66b4-162">Each row contains a number of columns that represent properties for that item.</span></span> <span data-ttu-id="d66b4-163">Не все элементы будут иметь значение для заданного свойства.</span><span class="sxs-lookup"><span data-stu-id="d66b4-163">Not all items will have a value for a given property.</span></span> <span data-ttu-id="d66b4-164">Например, звуковой файл обычно не содержит значение свойства System. Property. Фромнаме, но может содержать сведения о System. Music. исполнителя.</span><span class="sxs-lookup"><span data-stu-id="d66b4-164">For example, an audio file would typically not contain a value for the System.Property.FromName property but may contain information regarding the System.Music.Artist.</span></span>

<span data-ttu-id="d66b4-165">С помощью этих методов вы получите доступ к свойству или измените его с помощью строки в Юникоде с разделителями-запятыми, заканчивающейся нулем, которая указывает одно или несколько имен столбцов в хранилище свойств: "System.Docумент. Автор, System.Docумент. Title ".</span><span class="sxs-lookup"><span data-stu-id="d66b4-165">With these methods, you access or modify the property with a comma delimited, null-terminated, Unicode string that specifies one or more column names of the property store: "System.Document.Author, System.Document.Title".</span></span>

## <a name="working-with-query-term-expansion"></a><span data-ttu-id="d66b4-166">Работа с расширением термина запроса</span><span class="sxs-lookup"><span data-stu-id="d66b4-166">Working with Query Term Expansion</span></span>



| <span data-ttu-id="d66b4-167">Методы</span><span class="sxs-lookup"><span data-stu-id="d66b4-167">Methods</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="d66b4-168">Описание</span><span class="sxs-lookup"><span data-stu-id="d66b4-168">Description</span></span>                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="d66b4-169">**Исеарчкуерихелпер:: Get \_ куеритермекспансион**</span><span class="sxs-lookup"><span data-stu-id="d66b4-169">**ISearchQueryHelper::get\_QueryTermExpansion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [<span data-ttu-id="d66b4-170">**Исеарчкуерихелпер::p UT \_ куеритермекспансион**</span><span class="sxs-lookup"><span data-stu-id="d66b4-170">**ISearchQueryHelper::put\_QueryTermExpansion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | <span data-ttu-id="d66b4-171">Возвращает или задает флаг расширения критерия поиска.</span><span class="sxs-lookup"><span data-stu-id="d66b4-171">Gets/Sets the search term expansion flag.</span></span> |



 

<span data-ttu-id="d66b4-172">Этот метод позволяет раскрытие некоторых терминов запроса с подстановочными знаками, аналогично расширению регулярных выражений.</span><span class="sxs-lookup"><span data-stu-id="d66b4-172">This method enables the expansion of some query terms with wild card characters, similar to regular expression expansion.</span></span> <span data-ttu-id="d66b4-173">Расширение префикса ищет слова с одинаковым префиксом (Fun/воронка).</span><span class="sxs-lookup"><span data-stu-id="d66b4-173">Prefix expansion searches for words with the same prefix (fun/funnel).</span></span> <span data-ttu-id="d66b4-174">Если параметр не задан, по умолчанию используется \_ значение \_ префикс условия поиска \_ .</span><span class="sxs-lookup"><span data-stu-id="d66b4-174">If not set, the default value is SEARCH\_TERM\_PREFIX\_ALL.</span></span> <span data-ttu-id="d66b4-175">Ниже приведены поддерживаемые значения перечисления [**для \_ \_ расширения условий поиска**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) .</span><span class="sxs-lookup"><span data-stu-id="d66b4-175">The supported values of the [**SEARCH\_TERM\_EXPANSION**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) enumeration are as follows:</span></span>

-   <span data-ttu-id="d66b4-176">Поиск \_ по \_ префиксу слова \_ ALL — развернуты все условия поиска</span><span class="sxs-lookup"><span data-stu-id="d66b4-176">SEARCH\_TERM\_PREFIX\_ALL - All search terms are expanded</span></span>
-   <span data-ttu-id="d66b4-177">Поиск \_ слова \_ без \_ расширения — условия поиска не развернуты</span><span class="sxs-lookup"><span data-stu-id="d66b4-177">SEARCH\_TERM\_NO\_EXPANSION - No search terms are expanded</span></span>

## <a name="working-with-other-isearchqueryhelper-methods"></a><span data-ttu-id="d66b4-178">Работа с другими методами Исеарчкуерихелпер</span><span class="sxs-lookup"><span data-stu-id="d66b4-178">Working with Other ISearchQueryHelper Methods</span></span>

<span data-ttu-id="d66b4-179">Многие методы в интерфейсе [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) используются для задания аргументов запроса или определения возвращаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="d66b4-179">Many of the methods in the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface are used to set query arguments or define the properties returned.</span></span>



| <span data-ttu-id="d66b4-180">Методы</span><span class="sxs-lookup"><span data-stu-id="d66b4-180">Methods</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="d66b4-181">Описание</span><span class="sxs-lookup"><span data-stu-id="d66b4-181">Description</span></span>                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d66b4-182">**Исеарчкуерихелпер:: Get \_ ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="d66b4-182">**ISearchQueryHelper::get\_ConnectionString**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | <span data-ttu-id="d66b4-183">Возвращает строку подключения OLE DB.</span><span class="sxs-lookup"><span data-stu-id="d66b4-183">Returns the OLE DB connection string.</span></span> <span data-ttu-id="d66b4-184">Это предпочтительный метод получения правильно отформатированной и правильной строки подключения.</span><span class="sxs-lookup"><span data-stu-id="d66b4-184">This is the preferred method of getting a properly formatted and correct connection string.</span></span>                                  |
| [<span data-ttu-id="d66b4-185">**Исеарчкуерихелпер:: Get \_ куеримаксресултс**</span><span class="sxs-lookup"><span data-stu-id="d66b4-185">**ISearchQueryHelper::get\_QueryMaxResults**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [<span data-ttu-id="d66b4-186">**Исеарчкуерихелпер::p UT \_ куеримаксресултс**</span><span class="sxs-lookup"><span data-stu-id="d66b4-186">**ISearchQueryHelper::put\_QueryMaxResults**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | <span data-ttu-id="d66b4-187">Возвращает или задает максимальное число результатов, возвращаемых запросом (то есть выберите TOP n).</span><span class="sxs-lookup"><span data-stu-id="d66b4-187">Gets/Sets the maximum number of results to be returned by a query (that is, SELECT TOP n).</span></span> <span data-ttu-id="d66b4-188">Значение по умолчанию равно-1, то есть предложение максимального результата не создается.</span><span class="sxs-lookup"><span data-stu-id="d66b4-188">The default is -1, meaning that no maximum results clause is generated.</span></span> |
| [<span data-ttu-id="d66b4-189">**Исеарчкуерихелпер:: Get \_ куерисортинг**</span><span class="sxs-lookup"><span data-stu-id="d66b4-189">**ISearchQueryHelper::get\_QuerySorting**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [<span data-ttu-id="d66b4-190">**Исеарчкуерихелпер::p UT \_ куерисортинг**</span><span class="sxs-lookup"><span data-stu-id="d66b4-190">**ISearchQueryHelper::put\_QuerySorting**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | <span data-ttu-id="d66b4-191">Возвращает или задает порядок сортировки для результирующего набора запроса (ORDER BY).</span><span class="sxs-lookup"><span data-stu-id="d66b4-191">Gets/Sets the sort order for the query result set (ORDER BY).</span></span> <span data-ttu-id="d66b4-192">Если предложение ORDER BY не существует, результаты возвращаются в недетерминированном порядке.</span><span class="sxs-lookup"><span data-stu-id="d66b4-192">If no ORDER BY clause exists, the results are returned in non-deterministic order.</span></span>                   |
| [<span data-ttu-id="d66b4-193">**Исеарчкуерихелпер:: Get \_ куерисинтакс**</span><span class="sxs-lookup"><span data-stu-id="d66b4-193">**ISearchQueryHelper::get\_QuerySyntax**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [<span data-ttu-id="d66b4-194">**Исеарчкуерихелпер::p UT \_ куерисинтакс**</span><span class="sxs-lookup"><span data-stu-id="d66b4-194">**ISearchQueryHelper::put\_QuerySyntax**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | <span data-ttu-id="d66b4-195">Возвращает или задает синтаксис запроса: расширенный синтаксис запроса или синтаксис естественного запроса.</span><span class="sxs-lookup"><span data-stu-id="d66b4-195">Gets/Sets the syntax of the query: Advanced Query Syntax or Natural Query Syntax.</span></span>                                                                                  |
| [<span data-ttu-id="d66b4-196">**Исеарчкуерихелпер:: Get \_ куеривхеререстриктионс**</span><span class="sxs-lookup"><span data-stu-id="d66b4-196">**ISearchQueryHelper::get\_QueryWhereRestrictions**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [<span data-ttu-id="d66b4-197">**Исеарчкуерихелпер::p UT \_ куеривхеререстриктионс**</span><span class="sxs-lookup"><span data-stu-id="d66b4-197">**ISearchQueryHelper::put\_QueryWhereRestrictions**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | <span data-ttu-id="d66b4-198">Возвращает или задает ограничения, добавляемые с помощью предложения WHERE.</span><span class="sxs-lookup"><span data-stu-id="d66b4-198">Gets/Sets the restrictions appended via WHERE clauses.</span></span>                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="d66b4-199">См. также</span><span class="sxs-lookup"><span data-stu-id="d66b4-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d66b4-200">Отправка программных запросов к индексу</span><span class="sxs-lookup"><span data-stu-id="d66b4-200">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="d66b4-201">Использование методов SQL и АКС для запроса индекса</span><span class="sxs-lookup"><span data-stu-id="d66b4-201">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="d66b4-202">Запрос индекса с помощью протокола Search-MS</span><span class="sxs-lookup"><span data-stu-id="d66b4-202">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="d66b4-203">Запрос к индексу с помощью синтаксиса SQL для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="d66b4-203">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="d66b4-204">Использование расширенного синтаксиса запросов программными средствами</span><span class="sxs-lookup"><span data-stu-id="d66b4-204">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




